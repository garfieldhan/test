# ControllerGunBridge / Controllable 输入兼容性排查交接文档

> 目的：交给另一个 AI / Java 模组开发者，直接阅读 Controllable
> 0.26.2（Minecraft 26.3 NeoForge）源码，定位并修复 Xbox
> 手柄无法控制枪械模组的问题。
>
> 当前状态：**根因尚未确认；不要把"鼠标状态未模拟"或"Controllable
> 缺陷"当成既定事实。** 本文区分已验证事实与待验证假设。

## 1. 目标环境

  组件                当前版本 / 配置
  ------------------- ----------------------------------------------
  操作系统            macOS（MacBook Air）
  启动器              HMCL
  Minecraft           26.3
  Mod Loader          NeoForge 26.3.0.102
  本地多人            Local Multiplayer 1.2.0
  手柄支持            Controllable 0.26.2（NeoForge 26.3）
  Controllable 依赖   Framework 0.13.27
  性能模组            FerriteCore 9.0.0、Sodium 0.9.3-beta4+mc26.3
  玩家布局            P1 = 键盘；P2 = Xbox；P3 = Xbox

Local Multiplayer 在游戏中明确要求 Controllable；移除 Controllable
会阻止启动/进入本地多人模式。因此修复方案不能简单卸载
Controllable，也不应以替换成另一套控制器模组作为默认方案。

## 2. 已观察到的故障

两款不同枪械模组均出现同样问题：

-   Remnants: Ballistics 0.6.0
-   Just Enough Guns New（JEGN，用户测试版本）

表现： - 键盘鼠标左键可以正常射击。 - 鼠标右键可以正常瞄准。 - Xbox RT
可以进行 Minecraft 原版普通攻击。 - Xbox LT 可以进行 Minecraft 原版 Use
操作（例如使用/放置物品）。 - 但拿枪时，Xbox RT
无法射击，且没有射击动画。 - Xbox LT 无法瞄准。 - P2、P3 两个 Xbox
都失败。 - 进一步把 Xbox 作为 P1 主玩家测试，仍然不能用 RT/LT 控制
JEGN。

因此，当前证据**不支持"只有 Local Multiplayer Guest
输入转发出错"这一单一解释**。问题在 P1 主玩家下也存在。

## 3. 已完成的排查

1.  验证键鼠对 Remnants：Ballistics 可以正常射击和瞄准。
2.  验证 Xbox 手柄可以进行原版普通攻击。
3.  验证 Xbox LT 可以执行原版 Use。
4.  验证两个 Xbox 手柄均有相同问题。
5.  验证枪械没有射击动画，不只是弹药没有消耗。
6.  在 Controls → Key Binds 中，Remnants 分类只出现：
    -   Inspect Weapon
    -   Reload
    -   Switch Fire Mode 没有独立 Shoot / Fire
        按键。这与该模组将射击、瞄准绑定到原版 Attack / Use
        的操作说明相符。
7.  尝试 Controllable Advanced Options 中的 Raw Input；无改善。
8.  尝试隔离/精简模组组合；无改善。
9.  更换另一款枪械模组 JEGN；症状相同。
10. P1 Xbox 主玩家测试；仍失败。

## 4. 目前可以得出的结论

### 已有证据支持

-   Xbox 控制器连接与基本按键输入可用。
-   Controllable 至少能使 Xbox 输入触发 Minecraft 原版 Attack 和 Use。
-   枪械模组的键鼠操作正常。
-   故障跨两个枪械模组复现。
-   故障不仅发生于 Guest 玩家，P1 Xbox 也失败。

### 尚未证实的假设

1.  枪械模组可能直接查询 GLFW / Minecraft MouseHandler
    的鼠标按钮状态，而不是只监听 `KeyMapping` 或原版 Attack/Use 逻辑。
2.  Controllable
    可能只触发逻辑按键，没有为枪械模组提供它期待的鼠标按钮按下/释放状态。
3.  Controllable 26.3 的 SDL3 输入迁移可能引入或暴露了输入路径差异。
4.  可能还涉及 Minecraft 26.3
    的输入事件时序、焦点、窗口状态、鼠标捕获状态，或模组自己的射击实现。
5.  也可能是枪械模组在控制器输入场景下存在独立 Bug。

**不要在没有源码证据前就直接实现"RT/LT 转发为全局鼠标事件"。**
这可能造成双重触发、输入状态卡住、错误玩家收到事件，或破坏键鼠玩家 P1
的输入。

## 5. 官方源码与版本

-   Controllable 官方仓库： https://github.com/MrCrayfish/Controllable
-   Controllable 0.26.2 + MC 26.3 Release：
    https://github.com/MrCrayfish/Controllable/releases/tag/v0.26.2%2B26.3
-   Issues： https://github.com/MrCrayfish/Controllable/issues
-   CurseForge 26.3 NeoForge 文件：
    https://www.curseforge.com/minecraft/mc-mods/controllable/files/9054893

Release 页面记录： - Minecraft 26.3 更新。 - Raw Input 默认关闭，可在
Advanced Options 重新启用。 - 26.3 版本迁移使用 SDL3（Minecraft
自带的库）。

源码分析应以 **Release Tag `v0.26.2+26.3` 对应的确切源码**
为准，而不是直接假定仓库默认分支或 `multiloader/26.2` 分支与已安装 JAR
完全一致。

## 6. 建议 AI 按这个顺序阅读源码

### A. 确认输入数据流

追踪： 1. SDL3 初始化与控制器枚举。 2. Xbox 按键/轴输入读取。 3. RT、LT
的映射定义与状态更新。 4. Controllable
的按键绑定（Attack、Use）如何触发。 5. 按下与释放状态是否分别处理。 6.
输入是否在每帧更新，是否依赖窗口焦点或鼠标捕获状态。

### B. 对比两类输入路径

重点确认 Controllable 对 RT/LT 做的是哪一种：

-   调用 Minecraft `KeyMapping` / 设置逻辑按键状态；
-   注入 Minecraft 的 mouse button callback / event；
-   修改 `MouseHandler` 内部状态；
-   仅在 Controllable 自己的输入层消费事件。

再检查 Minecraft 26.3 中： - `KeyMapping` 的按下状态和 click count； -
`MouseHandler` 的按钮状态； - GLFW mouse button callback； -
鼠标按钮查询 API； - 输入事件派发与游戏 tick 的先后关系。

不要只看按键名称相同就认为两条路径等价。

### C. 检查枪械模组如何读取输入

对 Remnants 和 JEGN 分别检查： - 射击触发点； - 瞄准触发点； -
是否监听原版 Attack/Use； - 是否直接查询鼠标左/右键状态； - 是否在客户端
tick、渲染 tick 或事件回调中查询； -
是否检查玩家是否为本地玩家、窗口是否聚焦、鼠标是否被捕获。

如果两者使用不同的输入机制却同样失败，需继续查公共输入层；不能未经验证就认定它们采用相同鼠标轮询方式。

## 7. 推荐的诊断实验 / Instrumentation

在 Controllable 源码中临时加入日志（不要先做正式补丁）：

-   SDL3 收到的控制器实例 ID、按钮 ID、按下/释放值。
-   映射后的逻辑动作（Attack / Use）。
-   Controllable 每帧保存的按键状态。
-   Minecraft `KeyMapping` 对应状态。
-   鼠标左键/右键的 Minecraft 内部状态（如可访问）。
-   当前玩家身份/本地玩家上下文。
-   窗口 focus、mouse grabbed/captured 状态。

在同一时刻比较： 1. Xbox RT 按下； 2. 键盘/鼠标左键按下； 3. Xbox LT
按下； 4. 鼠标右键按下。

日志应包含按下与释放，避免只记录边沿事件而遗漏持续状态。

还应做一个最小复现： - 只保留 NeoForge、Controllable、Framework、Local
Multiplayer（如测试需要）和一个枪械模组。 - 首先单人/主玩家 Xbox
测试，之后再测 Guest。 - P1 键盘不动，分别测试 P2/P3。 -
如果可行，创建一个只读取 `KeyMapping` 和 MouseHandler 状态的测试
Mod，避免依赖枪械模组来推断输入状态。

## 8. 修复设计目标

期望实现一个独立兼容层（暂名
`ControllerGunBridge`），但只有在源码确认缺口后才决定实现方式。

要求： - NeoForge 26.3。 - 与 Controllable 0.26.2、Framework
0.13.27、Local Multiplayer 1.2.0 共存。 - P1 键盘与 P2/P3 Xbox
同时工作。 - RT 对应射击，LT 对应瞄准（具体映射可配置）。 - 正确处理
press/release，不得卡键。 - 不得将 P2/P3 的输入误发给 P1 或另一个
Guest。 - 不得重复触发 Attack/Use，避免一次按键触发两次射击/交互。 -
不应全局伪造鼠标事件，除非已确认枪械模组确实依赖该状态，并且能保证正确玩家上下文。 -
优先通过 Controllable 提供的 API / 事件或 NeoForge
可用机制实现；必要时再考虑 Mixin。 - 不修改用户现有原始 JAR；通过独立
Mod 或可维护的 fork 实现。 - 增加诊断日志开关，默认关闭。

## 9. 验收标准

  场景                     预期
  ------------------------ -----------------------------------------
  P1 键盘鼠标              原有射击、瞄准正常
  P2 Xbox                  RT 射击、LT 瞄准正常
  P3 Xbox                  RT 射击、LT 瞄准正常
  P2/P3 同时射击           两人都能射击，不串输入
  按住 RT                  行为符合枪械模组原有自动/半自动射击规则
  松开 RT                  射击输入状态立即释放
  按住/松开 LT             瞄准状态正确进入/退出
  切换窗口焦点、暂停菜单   不出现卡住的鼠标/射击状态
  不拿枪时使用 RT/LT       Minecraft 原版 Attack/Use 仍正常
  键鼠与手柄同时操作       不互相覆盖或重复触发

## 10. 交给代码 AI 的具体任务

请先读取 `v0.26.2+26.3` 的 Controllable 完整源码，重点分析 SDL3 →
Controllable input mapping → Minecraft KeyMapping / MouseHandler
的调用链。

不要先假定根因，也不要直接写补丁。先输出： 1. RT、LT
在当前版本中的真实处理路径（文件、类、方法）。 2. Attack/Use
与鼠标左/右键状态是否走同一条路径。 3. 哪些源码证据能解释"原版攻击/Use
正常，但两款枪械模组都不响应"。 4. 最小诊断日志应加在哪里。 5.
可能的修复点及副作用。 6. 如何保证 P1/P2/P3 输入隔离。

完成源码分析后，再提出最小修复方案和测试计划。若证据不足，应明确指出还需要哪些日志或复现信息，不要编造类名、方法名或
API。

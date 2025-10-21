                                                                                                                                                                     
┌──(root㉿kali)-[/usr/src/rtl8852bu]
└─# grep -R "8832" -n .  
./README.md:11:The driver supports rtl8832bu/rtl8852bu chipsets.
./README.md:16:* Realtek Demo Board with USB ID 0bda:8832
./phl/rtw_general_def.h:61:     RTL8832BR,
./phl/hal_g6/hal_init.c:1025:   else if(ic_id == RTL8832BR)
./phl/hal_g6/hal_init.c:1026:           chip_id = CHIP_WIFI6_8832BR;
./phl/hal_g6/hal.mk:97:ifneq ($(filter y,$(CONFIG_RTL8832BR) $(CONFIG_RTL8192XB)),)
./phl/hal_g6/hal_general_def.h:45:      CHIP_WIFI6_8832BR,
./phl/hal_g6/hal_def.h:958:    defined(CONFIG_RTL8192XB) || defined(CONFIG_RTL8832BR))
./phl/hal_g6/mac/mac.mk:163:ifneq ($(filter y,$(CONFIG_RTL8852C) $(CONFIG_RTL8832BRH)),)
./phl/hal_g6/mac/mac.mk:199:# 8832BR/8192XB Support
./phl/hal_g6/mac/mac.mk:200:ifneq ($(filter y,$(CONFIG_RTL8832BR) $(CONFIG_RTL8192XB)),)
./phl/hal_g6/mac/chip_cfg.h:37:#if defined(CONFIG_RTL8852C) || defined(CONFIG_RTL8832BRH)
./phl/hal_g6/mac/chip_cfg.h:44:#if defined(CONFIG_RTL8192XB) || defined(CONFIG_RTL8832BR)
./phl/hal_g6/mac/chip_cfg.h:52:#define MAC_AX_8832BR_SUPPORT    1
./phl/hal_g6/mac/chip_cfg.h:56:#define MAC_AX_8832BR_SUPPORT    0
./phl/hal_g6/mac/chip_cfg.h:122:#define MAC_AX_8832BR_SUPPORT   1
./phl/hal_g6/mac/chip_cfg.h:139:#define MAC_AX_8832BR_SUPPORT   0
./phl/hal_g6/phy/bb/halbb_init.c:273:   } else if (hal_i->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/bb/halbb_init.c:275:           bb->ic_sub_type = BB_IC_SUB_TYPE_8192XB_8832BR;
./phl/hal_g6/phy/bb/halbb_cfg_ic.h:41:#if defined(CONFIG_RTL8192XB) || defined(CONFIG_RTL8832BR)
./phl/hal_g6/phy/bb/halbb_ic_hw_info.h:53:      BB_IC_SUB_TYPE_8192XB_8832BR,
./phl/hal_g6/phy/bb/halbb_ic_hw_info.h:54:      BB_IC_SUB_TYPE_8192XB_8832BR_VT
./phl/hal_g6/phy/bb/bb.mk:107:ifeq ($(CONFIG_RTL8832BR), y)
./phl/hal_g6/phy/rf/rf.mk:94:ifeq ($(CONFIG_RTL8832BR), y)
./phl/hal_g6/phy/rf/rf.mk:95:rf_ic := 8832br
./phl/hal_g6/phy/rf/rf.mk:98:path_halrf_8832br := $(path_halrf_d1)/halrf_$(rf_ic)
./phl/hal_g6/phy/rf/rf.mk:100:halrf-y += $(path_halrf_8832br)/halrf_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:101:                  $(path_halrf_8832br)/halrf_8832br_api.o \
./phl/hal_g6/phy/rf/rf.mk:102:                  $(path_halrf_8832br)/halrf_hwimg_8832br.o\
./phl/hal_g6/phy/rf/rf.mk:103:                  $(path_halrf_8832br)/halrf_iqk_8832br.o\
./phl/hal_g6/phy/rf/rf.mk:104:                  $(path_halrf_8832br)/halrf_reg_cfg_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:105:                  $(path_halrf_8832br)/halrf_set_pwr_table_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:106:                  $(path_halrf_8832br)/halrf_dack_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:107:                  $(path_halrf_8832br)/halrf_dpk_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:108:                  $(path_halrf_8832br)/halrf_efuse_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:109:                  $(path_halrf_8832br)/halrf_txgapk_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:110:                  $(path_halrf_8832br)/halrf_tssi_8832br.o \
./phl/hal_g6/phy/rf/rf.mk:111:                  $(path_halrf_8832br)/halrf_kfree_8832br.o\
./phl/hal_g6/phy/rf/rf.mk:112:                  $(path_halrf_8832br)/halrf_psd_8832br.o
./phl/hal_g6/phy/rf/halrf_ic_hw_info.h:33:      RF_RTL8832BR    =       BIT(4),
./phl/hal_g6/phy/rf/halrf_ic_hw_info.h:40:      RF_RTL8832CR_VU =       BIT(11),
./phl/hal_g6/phy/rf/halrf_ic_hw_info.h:41:      RF_RTL8832BR_VT =       BIT(12),
./phl/hal_g6/phy/rf/halrf_ic_hw_info.h:45:      RF_SUBDID_RTL8832CRVU = 0xc832,
./phl/hal_g6/phy/rf/halrf_ic_hw_info.h:46:      RF_SUBDID_RTL8832BRVT = 0xb83b,
./phl/hal_g6/phy/rf/halrf_ic_hw_info.h:61:                               RF_RTL8832BR | RF_RTL8192XB | RF_RTL8852BP)
./phl/hal_g6/phy/rf/halrf_ic_hw_info.h:90:       defined(RF_8852C_SUPPORT) || defined(RF_8832BR_SUPPORT) ||\
./phl/hal_g6/phy/rf/halrf_precomp.h:42:#ifdef CONFIG_RTL8832BR
./phl/hal_g6/phy/rf/halrf_precomp.h:43:    #define RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_precomp.h:58:#ifdef CONFIG_RTL8832CRVU
./phl/hal_g6/phy/rf/halrf_precomp.h:59:    #define RF_8832CRVU_SUPPORT
./phl/hal_g6/phy/rf/halrf_precomp.h:62:#ifdef CONFIG_RTL8832BRVT
./phl/hal_g6/phy/rf/halrf_precomp.h:63:    #define RF_8832BRVT_SUPPORT
./phl/hal_g6/phy/rf/halrf_precomp.h:129:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_precomp.h:130:#include "halrf_8832br/halrf_dack_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:131:#include "halrf_8832br/halrf_hwimg_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:132:#include "halrf_8832br/halrf_kfree_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:207:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_precomp.h:208:        #include "halrf_8832br/halrf_efuse_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:209:        #include "halrf_8832br/halrf_reg_cfg_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:210:        #include "halrf_8832br/halrf_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:211:        #include "halrf_8832br/halrf_8832br_api.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:212://      #include "halrf_8832br/halrf_8832br_api_ex.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:213:        #include "halrf_8832br/halrf_iqk_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:214:        #include "halrf_8832br/halrf_dpk_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:215:        #include "halrf_8832br/halrf_txgapk_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:216:        #include "halrf_8832br/halrf_version_rtl8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:217:        #include "halrf_8832br/halrf_set_pwr_table_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:218:        #include "halrf_8832br/halrf_tssi_8832br.h"
./phl/hal_g6/phy/rf/halrf_precomp.h:219:        #include "halrf_8832br/halrf_psd_8832br.h"
./phl/hal_g6/phy/rf/halrf_init.c:30:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_init.c:31:    if (hal_i->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf_init.c:32:            rf->ic_type = RF_RTL8832BR;
./phl/hal_g6/phy/rf/halrf_init.c:92:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_init.c:93:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_init.c:94:            rf->rfk_iqk_info = &rf_iqk_hwspec_8832br;
./phl/hal_g6/phy/rf/halrf_init.c:220:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_init.c:221:   case RF_RTL8832BR:
./phl/hal_g6/phy/rf/halrf_init.c:402:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_init.c:403:   case RF_RTL8832BR:
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:49:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:50:  if (rf->ic_type == RF_RTL8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:51:          halrf_config_8832br_nctl_reg(rf);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:104:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:105: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:106:         halrf_config_8832br_radio_a_reg(rf, 0);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:161:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:162: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:163:         halrf_config_8832br_radio_b_reg(rf, 0);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:207:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:208: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:209:         halrf_config_8832br_store_power_by_rate(rf, 0);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:270:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:271: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:272:         halrf_config_8832br_store_power_limit(rf, 0);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:329:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:330: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:331:         halrf_config_8832br_store_power_limit_ru(rf, 0);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:386:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:387: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:388:         halrf_config_8832br_store_pwr_track(rf, 0);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:490:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:491: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:492:         halrf_config_8832br_radio_a_reg(rf, phy);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:493:         halrf_config_8832br_radio_b_reg(rf, phy);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:549:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:550: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:551:         halrf_config_8832br_store_power_by_rate(rf, phy);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:606:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:607: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:608:         halrf_config_8832br_store_power_limit(rf, phy);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:658:#ifdef RF_8832CRVU_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:659: case RF_RTL8832CR_VU:
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:660:         halrf_config_8832crvu_store_power_limit_6g(rf, phy);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:696:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:697: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:698:         halrf_config_8832br_store_power_limit_ru(rf, phy);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:747:#ifdef RF_8832CRVU_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:748: case RF_RTL8832CR_VU:
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:749:         halrf_config_8832crvu_store_power_limit_ru_6g(rf, phy);
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:784:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:785: if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_hw_cfg.c:786:         halrf_config_8832br_store_pwr_track(rf, phy);
./phl/hal_g6/phy/rf/halrf_dbg.c:350:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:351:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:352:            ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:353:            dpk_ver = DPK_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:488:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:489:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:490:            ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:533:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:534:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:535:            ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:576:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:577:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:578:            ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:738:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:739:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:740:            ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:741:            rxdck_ver = RXDCK_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:1087:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:1088:   case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:1089:           ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:1090:           tssi_ver = TSSI_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:1318:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:1319:   case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:1320:           ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:1922:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:1923:   case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:1924:           ic_name = "8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:1925:           txgapk_ver = TXGAPK_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:2396:   #ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:2397:           case RF_RTL8832BR:
./phl/hal_g6/phy/rf/halrf_dbg.c:2398:                   ic_name = "RF_RTL8832BR";
./phl/hal_g6/phy/rf/halrf_dbg.c:2399:                   dack_ver = DACK_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:2400:                   rxdck_ver =  RXDCK_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:2401:                   txgapk_ver = TXGAPK_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:2402:                   tssi_ver = TSSI_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:2403:                   dpk_ver = DPK_VER_8832BR;
./phl/hal_g6/phy/rf/halrf_dbg.c:2426:   #ifdef RF_8832CRVU_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:2427:           case RF_RTL8832CR_VU:
./phl/hal_g6/phy/rf/halrf_dbg.c:2428:                   ic_name = "RF_RTL8832CR_VU";
./phl/hal_g6/phy/rf/halrf_dbg.c:2429:                   dack_ver = DACK_VER_8832CRVU;
./phl/hal_g6/phy/rf/halrf_dbg.c:2430:                   rxdck_ver =  RXDCK_VER_8832CRVU;
./phl/hal_g6/phy/rf/halrf_dbg.c:2431:                   txgapk_ver = TXGAPK_VER_8832CRVU;
./phl/hal_g6/phy/rf/halrf_dbg.c:2432:                   tssi_ver = TSSI_VER_8832CRVU;
./phl/hal_g6/phy/rf/halrf_dbg.c:2433:                   dpk_ver = DPK_VER_8832CRVU;
./phl/hal_g6/phy/rf/halrf_dbg.c:2436:   #ifdef RF_8832BRVT_SUPPORT
./phl/hal_g6/phy/rf/halrf_dbg.c:2437:           case RF_RTL8832BR_VT:
./phl/hal_g6/phy/rf/halrf_dbg.c:2438:                   ic_name = "RF_RTL8832BR_VT";
./phl/hal_g6/phy/rf/halrf_dbg.c:2439:                   dack_ver = DACK_VER_8832BRVT;
./phl/hal_g6/phy/rf/halrf_dbg.c:2440:                   rxdck_ver =  RXDCK_VER_8832BRVT;
./phl/hal_g6/phy/rf/halrf_dbg.c:2441:                   txgapk_ver = TXGAPK_VER_8832BRVT;
./phl/hal_g6/phy/rf/halrf_dbg.c:2442:                   tssi_ver = TSSI_VER_8832BRVT;
./phl/hal_g6/phy/rf/halrf_dbg.c:2443:                   dpk_ver = DPK_VER_8832BRVT;
./phl/hal_g6/phy/rf/halrf.c:192:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:193:                case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:194:                halrf_dac_cal_8832br(rf, force);
./phl/hal_g6/phy/rf/halrf.c:289:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:290:        case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:291:                halrf_rx_dck_8832br(rf, phy_idx, false);
./phl/hal_g6/phy/rf/halrf.c:499:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:500:        case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:501:                halrf_lck_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:545:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:546:        case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:547:                halrf_lck_tracking_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:584:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:585:                case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:586:                        halrf_op5k_trigger_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:619:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:620:                case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:621:                        halrf_op5k_trigger_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:651:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:652:                case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:653:                        halrf_op5k_tracking_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:721:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:722:        case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:723:                halrf_dpk_8832br(rf, phy_idx, force);
./phl/hal_g6/phy/rf/halrf.c:797:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:798:        case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:799:                halrf_dpk_track_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:904:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:905:                case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:906:                        halrf_tssi_ant_open_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:984:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:985:                        case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:986:                                halrf_tssi_disable_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:1036:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1037:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1038:                       halrf_do_tssi_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:1111:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1112:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1113:               halrf_do_tssi_scan_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:1196:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1197:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1198:               halrf_tssi_default_txagc_8832br(rf, phy_idx, enable);
./phl/hal_g6/phy/rf/halrf.c:1257:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1258:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1259:               halrf_tssi_set_efuse_to_de_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:1319:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1320:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1321:               halrf_tssi_scan_ch_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf.c:1383:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1384:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1385:               halrf_tssi_scan_ch_setting_8832br(rf, phy_idx, path);
./phl/hal_g6/phy/rf/halrf.c:1451:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1452:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1453:               halrf_tssi_hw_tx_8832br(rf, HW_PHY_0, path, cnt, dbm, HT_MF_FMT, 0, enable);
./phl/hal_g6/phy/rf/halrf.c:1509:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1510:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1511:               halrf_kfree_get_info_8832br(rf, input, _used,
./phl/hal_g6/phy/rf/halrf.c:1565:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1566:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1567:               halrf_txgapk_init_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:1640:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1641:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1642:               halrf_do_txgapk_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:1712:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1713:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1714:               //halrf_txgapk_enable_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:1765:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1766:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1767:               halrf_txgapk_write_table_default_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:1824:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1825:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1827:                       halrf_rck_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf.c:1944:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:1945:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:1946:                       halrf_iqk_onoff_8832br(rf, is_enable);
./phl/hal_g6/phy/rf/halrf.c:2018:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2019:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2021:                       halrf_dpk_onoff_8832br(rf, path, false);
./phl/hal_g6/phy/rf/halrf.c:2161:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2162:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2163:               halrf_rx_dck_onoff_8832br(rf, is_enable);
./phl/hal_g6/phy/rf/halrf.c:2287:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2288:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:2289:               return halrf_get_thermal_8832br(rf, rf_path);
./phl/hal_g6/phy/rf/halrf.c:2344:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2345:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2346:                       tmp = halrf_get_online_tssi_de_8832br(rf, phy_idx, path, dbm, puot);
./phl/hal_g6/phy/rf/halrf.c:2398:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2399:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2400:                       halrf_tssi_enable_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:2451:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2452:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2453:                       halrf_tssi_disable_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:2492:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2493:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2494:                       halrf_tssi_slope_onoff_8832br(rf, tssi_slope_type);
./phl/hal_g6/phy/rf/halrf.c:2522:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2523:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2524:                       halrf_tssi_do_slope_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:2552:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2553:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2554:                       return halrf_tssi_get_cw_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf.c:2590:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2591:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2592:                       halrf_tssi_slope_apply_8832br(rf,
./phl/hal_g6/phy/rf/halrf.c:2628:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2629:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2630:                       halrf_tssi_current_slope_apply_8832br(rf,
./phl/hal_g6/phy/rf/halrf.c:2660:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2661:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2662:                       halrf_tssi_finish_slope_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:2754:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2755:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2756:                       halrf_set_tssi_de_for_tx_verify_8832br(rf, phy_idx, tssi_de, path);
./phl/hal_g6/phy/rf/halrf.c:2823:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2824:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2825:                       return halrf_tssi_get_final_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf.c:2878:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:2879:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:2880:                       halrf_set_tssi_de_offset_8832br(rf, phy_idx, tssi_de_offset, path);
./phl/hal_g6/phy/rf/halrf.c:3018:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3019:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3020:                       halrf_tssi_get_efuse_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:3078:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3079:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3080:                       return halrf_tssi_check_efuse_data_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:3132:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3133:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3134:                       halrf_set_ref_power_to_struct_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:3205:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3206:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3207:                       halrf_bf_config_rf_8832br(rf);
./phl/hal_g6/phy/rf/halrf.c:3240:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3241:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:3242:               return halrf_get_efuse_info_8832br(rf, efuse_map, id, value, length,
./phl/hal_g6/phy/rf/halrf.c:3301:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3302:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:3303:               halrf_get_efuse_trim_8832br(rf, phy_idx);
./phl/hal_g6/phy/rf/halrf.c:3606:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3607:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:3608:               halrf_psd_init_8832br(rf, phy, path, iq_path, avg, fft);
./phl/hal_g6/phy/rf/halrf.c:3653:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3654:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:3655:               halrf_psd_restore_8832br(rf, phy);
./phl/hal_g6/phy/rf/halrf.c:3700:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3701:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:3702:               return halrf_psd_get_point_data_8832br(rf, phy, point);
./phl/hal_g6/phy/rf/halrf.c:3749:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3750:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:3751:               halrf_psd_query_8832br(rf, phy, point, start_point, stop_point, outbuf);
./phl/hal_g6/phy/rf/halrf.c:3808:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3809:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3810:                       halrf_set_fix_power_to_struct_8832br(rf, phy, dbm);
./phl/hal_g6/phy/rf/halrf.c:3866:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3867:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3868:                       halrf_pwr_by_rate_info_8832br(rf, input, &used,
./phl/hal_g6/phy/rf/halrf.c:3931:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3932:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3933:                       halrf_pwr_limit_info_8832br(rf, input, &used,
./phl/hal_g6/phy/rf/halrf.c:3996:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:3997:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:3998:                       halrf_pwr_limit_ru_info_8832br(rf, input, &used,
./phl/hal_g6/phy/rf/halrf.c:4056:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4057:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:4058:                       halrf_get_tssi_info_8832br(rf, input, _used,
./phl/hal_g6/phy/rf/halrf.c:4147:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4148:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:4149:                       halrf_set_tx_shape_8832br(rf, tx_shape_idx);
./phl/hal_g6/phy/rf/halrf.c:4192:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4193:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:4194:                               halrf_ctrl_bw_8832br(rf, phy, bw);
./phl/hal_g6/phy/rf/halrf.c:4237:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4238:               case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:4239:                       halrf_ctrl_ch_8832br(rf, phy, central_ch, band);
./phl/hal_g6/phy/rf/halrf.c:4293:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4294:       case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf.c:4295:               halrf_rxbb_bw_8832br(rf, phy, bw);
./phl/hal_g6/phy/rf/halrf.c:4588:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4589:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:4590:               halrf_set_regulation_from_driver_8832br(rf, regulation_idx);
./phl/hal_g6/phy/rf/halrf.c:4618:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4619:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:4620:               return halrf_get_8832br_nctl_reg_ver();
./phl/hal_g6/phy/rf/halrf.c:4677:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4678:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:4712:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4713:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:4714:               halrf_config_8832br_nctl_reg(rf);
./phl/hal_g6/phy/rf/halrf.c:4785:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4786:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:4787:               result = halrf_mac_set_pwr_reg_8832br(rf, phy, addr, mask, val);
./phl/hal_g6/phy/rf/halrf.c:4832:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:4833:       if (hal_com->chip_id == CHIP_WIFI6_8832BR)
./phl/hal_g6/phy/rf/halrf.c:4834:               return halrf_mac_get_pwr_reg_8832br(rf, phy, addr, mask);
./phl/hal_g6/phy/rf/halrf.c:5025:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5026:       if (rf->ic_type == RF_RTL8832BR)
./phl/hal_g6/phy/rf/halrf.c:5040:#ifdef RF_8832CRVU_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5041:       if (rf->ic_type == RF_RTL8832CR_VU)
./phl/hal_g6/phy/rf/halrf.c:5045:#ifdef RF_8832BRVT_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5046:       if (rf->ic_type == RF_RTL8832BR_VT)
./phl/hal_g6/phy/rf/halrf.c:5054:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5055:       if (rf->ic_type == RF_RTL8832BR)
./phl/hal_g6/phy/rf/halrf.c:5069:#ifdef RF_8832CRVU_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5070:       if (rf->ic_type == RF_RTL8832CR_VU)
./phl/hal_g6/phy/rf/halrf.c:5074:#ifdef RF_8832BRVT_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5075:       if (rf->ic_type == RF_RTL8832BR_VT)
./phl/hal_g6/phy/rf/halrf.c:5083:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5084:       if (rf->ic_type == RF_RTL8832BR)
./phl/hal_g6/phy/rf/halrf.c:5098:#ifdef RF_8832CRVU_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5099:       if (rf->ic_type == RF_RTL8832CR_VU)
./phl/hal_g6/phy/rf/halrf.c:5103:#ifdef RF_8832BRVT_SUPPORT
./phl/hal_g6/phy/rf/halrf.c:5104:       if (rf->ic_type == RF_RTL8832BR_VT)
./phl/hal_g6/phy/rf/halrf_pwr_table.c:2213:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_pwr_table.c:2214:     if (hal_com->chip_id == CHIP_WIFI6_8832BR) {
./phl/hal_g6/phy/rf/halrf_pwr_table.c:2215:             halrf_set_power_8832br(rf, phy, pwr_table);
./phl/hal_g6/phy/rf/halrf_iqk.c:241:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:242:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:243:            iqk_init_8832br(rf);
./phl/hal_g6/phy/rf/halrf_iqk.c:540:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:541:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:542:            tmp =halrf_get_iqk_ver_8832br();
./phl/hal_g6/phy/rf/halrf_iqk.c:578:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:579:            case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:580:                    halrf_iqk_toneleakage_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf_iqk.c:617:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:618:            case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:619:                    halrf_iqk_tx_bypass_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf_iqk.c:662:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:663:            case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:664:                    halrf_iqk_rx_bypass_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf_iqk.c:705:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:706:            case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:707:                    halrf_iqk_lok_bypass_8832br(rf, path);
./phl/hal_g6/phy/rf/halrf_iqk.c:748:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:749:            case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:750:                    halrf_nbiqk_enable_8832br(rf, iqk_nbiqk_en);
./phl/hal_g6/phy/rf/halrf_iqk.c:791:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:792:            case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:793:                    halrf_iqk_xym_enable_8832br(rf, iqk_xym_en);
./phl/hal_g6/phy/rf/halrf_iqk.c:861:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:862:    case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:863:            halrf_iqk_cfir_enable_8832br(rf, iqk_cfir_en);
./phl/hal_g6/phy/rf/halrf_iqk.c:899:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:900:            case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:901:                    halrf_iqk_sram_enable_8832br(rf, iqk_sram_en);
./phl/hal_g6/phy/rf/halrf_iqk.c:1091:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:1092:   case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:1093:           rxevm = halrf_iqk_get_rxevm_8832br(rf);
./phl/hal_g6/phy/rf/halrf_iqk.c:1131:#ifdef RF_8832BR_SUPPORT
./phl/hal_g6/phy/rf/halrf_iqk.c:1132:           case CHIP_WIFI6_8832BR:
./phl/hal_g6/phy/rf/halrf_iqk.c:1133:                   rximr = halrf_iqk_get_rximr_8832br(rf, path, idx);
./phl/hal_g6/hal_config.h:98:#if defined(CONFIG_RTL8192XB) || defined(CONFIG_RTL8832BR)
./phl/phl_init.c:2803:  case CHIP_WIFI6_8832BR:
./phl/phl_init.c:2804:          ic_id = RTL8832BR;
                                                                                                                                                                       
┌──(root㉿kali)-[/usr/src/rtl8852bu]
└─# grep -R "0x8832" -n .
                                                                                                                                                                       
┌──(root㉿kali)-[/usr/src/rtl8852bu]
└─# 

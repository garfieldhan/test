/* DID_USB_v916_20130116 */
static struct usb_device_id rtw_usb_id_tbl[] = {
#ifdef CONFIG_RTL8188E
	/*=== Realtek demoboard ===*/
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x8179), .driver_info = RTL8188E}, /* 8188EUS */
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x0179), .driver_info = RTL8188E}, /* 8188ETV */
	/*=== Customer ID ===*/
	/****** 8188EUS ********/
	{USB_DEVICE(0x07B8, 0x8179), .driver_info = RTL8188E}, /* Abocom - Abocom */
#endif

#ifdef CONFIG_RTL8812A
	/*=== Realtek demoboard ===*/
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x8812), .driver_info = RTL8812}, /* Default ID */
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x881A), .driver_info = RTL8812}, /* Default ID */
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x881B), .driver_info = RTL8812}, /* Default ID */
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x881C), .driver_info = RTL8812}, /* Default ID */
	/*=== Customer ID ===*/
	{USB_DEVICE(0x050D, 0x1106), .driver_info = RTL8812}, /* Belkin - sercomm */
	{USB_DEVICE(0x2001, 0x330E), .driver_info = RTL8812}, /* D-Link - ALPHA */
	{USB_DEVICE(0x7392, 0xA822), .driver_info = RTL8812}, /* Edimax - Edimax */
	{USB_DEVICE(0x0DF6, 0x0074), .driver_info = RTL8812}, /* Sitecom - Edimax */
	{USB_DEVICE(0x04BB, 0x0952), .driver_info = RTL8812}, /* I-O DATA - Edimax */
	{USB_DEVICE(0x0789, 0x016E), .driver_info = RTL8812}, /* Logitec - Edimax */
	{USB_DEVICE(0x0409, 0x0408), .driver_info = RTL8812}, /* NEC - */
	{USB_DEVICE(0x0B05, 0x17D2), .driver_info = RTL8812}, /* ASUS - Edimax */
	{USB_DEVICE(0x0E66, 0x0022), .driver_info = RTL8812}, /* HAWKING - Edimax */
	{USB_DEVICE(0x0586, 0x3426), .driver_info = RTL8812}, /* ZyXEL - */
	{USB_DEVICE(0x2001, 0x3313), .driver_info = RTL8812}, /* D-Link - ALPHA */
	{USB_DEVICE(0x1058, 0x0632), .driver_info = RTL8812}, /* WD - Cybertan*/
	{USB_DEVICE(0x1740, 0x0100), .driver_info = RTL8812}, /* EnGenius - EnGenius */
	{USB_DEVICE(0x2019, 0xAB30), .driver_info = RTL8812}, /* Planex - Abocom */
	{USB_DEVICE(0x07B8, 0x8812), .driver_info = RTL8812}, /* Abocom - Abocom */
	{USB_DEVICE(0x2001, 0x3315), .driver_info = RTL8812}, /* D-Link - Cameo */
	{USB_DEVICE(0x2001, 0x3316), .driver_info = RTL8812}, /* D-Link - Cameo */
#endif

#ifdef CONFIG_RTL8821A
	/*=== Realtek demoboard ===*/
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x0811), .driver_info = RTL8821}, /* Default ID */
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x0821), .driver_info = RTL8821}, /* Default ID */
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x8822), .driver_info = RTL8821}, /* Default ID */
	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0xA811) , .driver_info = RTL8821},/* Default ID */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0x0820, 0xff, 0xff, 0xff), .driver_info = RTL8821}, /* 8821AU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0x0823, 0xff, 0xff, 0xff), .driver_info = RTL8821}, /* 8821AU */
	/*=== Customer ID ===*/
	{USB_DEVICE(0x7392, 0xA811), .driver_info = RTL8821}, /* Edimax - Edimax */
	{USB_DEVICE(0x04BB, 0x0953), .driver_info = RTL8821}, /* I-O DATA - Edimax */
	{USB_DEVICE(0x2001, 0x3314), .driver_info = RTL8821}, /* D-Link - Cameo */
	{USB_DEVICE(0x2001, 0x3318), .driver_info = RTL8821}, /* D-Link - Cameo */
	{USB_DEVICE(0x0E66, 0x0023), .driver_info = RTL8821}, /* HAWKING - Edimax */
	{USB_DEVICE(0x056E, 0x400E) , .driver_info = RTL8821}, /* ELECOM -  ELECOM */
	{USB_DEVICE(0x056E, 0x400F) , .driver_info = RTL8821}, /* ELECOM -  ELECOM */
	{USB_DEVICE(0x20f4, 0x804b), .driver_info = RTL8821}, /* TRENDnet  */
#endif

#ifdef CONFIG_RTL8192E
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0x818B, 0xff, 0xff, 0xff), .driver_info = RTL8192E}, /* Default ID */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0x818C, 0xff, 0xff, 0xff), .driver_info = RTL8192E}, /* Default ID */
#endif

#ifdef CONFIG_RTL8723B
	/* === Realtek demoboard === */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB720, 0xff, 0xff, 0xff), .driver_info = RTL8723B}, /* 8723BU 1*1 */
	/* {USB_DEVICE(USB_VENDER_ID_REALTEK, 0xB720),.driver_info = RTL8723B},  8723BU */
#endif

#ifdef CONFIG_RTL8703B
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB703, 0xff, 0xff, 0xff), .driver_info = RTL8703B}, /* 8723CU 1*1 */
	/* {USB_DEVICE(USB_VENDER_ID_REALTEK, 0xB703), .driver_info = RTL723C}, */ /* 8723CU 1*1 */
#endif /* CONFIG_RTL8703B */

#ifdef CONFIG_RTL8814A

	{USB_DEVICE(USB_VENDER_ID_REALTEK, 0x8813), .driver_info = RTL8814A},
	{USB_DEVICE(0x2001, 0x331a), .driver_info = RTL8814A}, /* D-Link - D-Link */
	{USB_DEVICE(0x0b05, 0x1817), .driver_info = RTL8814A}, /* ASUS - ASUSTeK */
	{USB_DEVICE(0x056E, 0x400B), .driver_info = RTL8814A}, /* ELECOM - ELECOM */
	{USB_DEVICE(0x056E, 0x400D), .driver_info = RTL8814A}, /* ELECOM - ELECOM */
	{USB_DEVICE(0x7392, 0xA834), .driver_info = RTL8814A}, /* Edimax - Edimax */
#endif /* CONFIG_RTL8814A */

#ifdef CONFIG_RTL8188F
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xF179, 0xff, 0xff, 0xff), .driver_info = RTL8188F}, /* 8188FU 1*1 */
#endif

#ifdef CONFIG_RTL8188GTV
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0x018C, 0xff, 0xff, 0xff), .driver_info = RTL8188GTV}, /* 8188GTV 1*1 */
#endif

#ifdef CONFIG_RTL8822B
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB812, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Default ID for USB Single-function, WiFi only */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB81A, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Default ID */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB82C, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Default ID for USB multi-function */
	/*=== Customer ID ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(0x04CA, 0x8602, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* LiteOn */
	{USB_DEVICE_AND_INTERFACE_INFO(0x056E, 0x4011, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Elecom */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0846, 0x9055, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Netgear A6150 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0B05, 0x1841, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* ASUS AC1300 USB-AC55 B1 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0B05, 0x184C, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* ASUS U2 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0B05, 0x1870, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* ASUS */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0B05, 0x1874, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* ASUS */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0B05, 0x19AA, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* ASUS - USB-AC58 rev A1 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0BDA, 0x2102, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* CCNC */
	{USB_DEVICE_AND_INTERFACE_INFO(0x0E66, 0x0025, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Hawking HW12ACU */
	{USB_DEVICE_AND_INTERFACE_INFO(0x13B1, 0x0043, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Alpha - Linksys */
	{USB_DEVICE_AND_INTERFACE_INFO(0x13B1, 0x0045, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Linksys WUSB3600 v2 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2001, 0x331C, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Dlink - DWA-182 - D1 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2001, 0x331E, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Dlink - DWA-181 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2001, 0x331F, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Dlink - DWA-183 - D */
	{USB_DEVICE_AND_INTERFACE_INFO(0x20F4, 0x805A, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TRENDnet TEW-805UBH */
	{USB_DEVICE_AND_INTERFACE_INFO(0x20F4, 0x808A, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TRENDnet TEW-808UBM */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2357, 0x0115, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TP-Link Archer T4U V3 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2357, 0x0116, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TP-LINK */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2357, 0x0117, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TP-LINK */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2357, 0x012D, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TP-Link Archer T3U v1 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2357, 0x012E, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TP-LINK */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2357, 0x0138, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* TP-Link Archer T3U Plus v1 */
	{USB_DEVICE_AND_INTERFACE_INFO(0x2C4E, 0x0107, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Mercusys MA30H */
	{USB_DEVICE_AND_INTERFACE_INFO(0x7392, 0xB822, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Edimax */
	{USB_DEVICE_AND_INTERFACE_INFO(0x7392, 0xC822, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Edimax */
	{USB_DEVICE_AND_INTERFACE_INFO(0x7392, 0xD822, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Edimax */
	{USB_DEVICE_AND_INTERFACE_INFO(0x7392, 0xE822, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Edimax */
	{USB_DEVICE_AND_INTERFACE_INFO(0x7392, 0xF822, 0xff, 0xff, 0xff), .driver_info = RTL8822B}, /* Edimax */
#endif /* CONFIG_RTL8822B */

#ifdef CONFIG_RTL8723D
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xD723, 0xff, 0xff, 0xff), .driver_info = RTL8723D}, /* 8723DU 1*1 */
#endif

#ifdef CONFIG_RTL8192F
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xF192, 0xff, 0xff, 0xff), .driver_info = RTL8192F}, /* 8192FU 2*2 */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xA725, 0xff, 0xff, 0xff), .driver_info = RTL8192F}, /* 8725AU 2*2 */
#endif

#ifdef CONFIG_RTL8821C
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xb82b, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8821CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xb820, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8821CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC821, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8821CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC820, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8821CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC82A, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8821CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC82B, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8821CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC811, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8811CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0x8811, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8811CU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0x8731, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8731AU */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC80C, 0xff, 0xff, 0xff), .driver_info = RTL8821C}, /* 8821CUH */
	/*=== Customer ID ===*/
#endif

#ifdef CONFIG_RTL8710B
	/*=== Realtek dongle ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB711, 0xff, 0xff, 0xff), .driver_info = RTL8710B}, /* 8710B = 8188GU 1*1 */
#endif

#ifdef CONFIG_RTL8822C
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC82C, 0xff, 0xff, 0xff), .driver_info = RTL8822C}, /* Default ID for USB multi-function */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC82E, 0xff, 0xff, 0xff), .driver_info = RTL8822C}, /* Default ID for USB multi-function */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xC812, 0xff, 0xff, 0xff), .driver_info = RTL8822C}, /* Default ID for USB Single-function, WiFi only */
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xD820, 0xff, 0xff, 0xff), .driver_info = RTL8822C}, /* 21D USB multi-fuction*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xD82B, 0xff, 0xff, 0xff), .driver_info = RTL8822C}, /* 21D USB Single-fuction, WiFi only*/
	/*=== Customer ID ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(0x13b1, 0x0043, 0xff, 0xff, 0xff), .driver_info = RTL8822C}, /* Alpha - Alpha*/
#endif /* CONFIG_RTL8822C */

#ifdef CONFIG_RTL8814B
	/*=== Realtek demoboard ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB814, 0xff, 0xff, 0xff), .driver_info = RTL8814B}, /* Default ID for USB multi-function */
#endif /* CONFIG_RTL8814B */
#ifdef CONFIG_RTL8723F
	/*=== Realtek IC ===*/
	{USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB733, 0xff, 0xff, 0xff), .driver_info = RTL8723F}, 
#endif

	{}	/* Terminating entry */
};

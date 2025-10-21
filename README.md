static struct usb_device_id rtw_usb_id_tbl[] = {
#ifdef CONFIG_RTL8852B
        /*=== Realtek demoboard ===*/
        {USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB832, 0xff, 0xff, 0xff), .driver_info = RTL8852B},
        {USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB83A, 0xff, 0xff, 0xff), .driver_info = RTL8852B},
        {USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB852, 0xff, 0xff, 0xff), .driver_info = RTL8852B},
        {USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xB85A, 0xff, 0xff, 0xff), .driver_info = RTL8852B},
        {USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xA85B, 0xff, 0xff, 0xff), .driver_info = RTL8852B},

        /*=== ASUS USB-AX55 =======*/
        {USB_DEVICE_AND_INTERFACE_INFO(USB_VENDOR_ID_ASUS, 0x1a62, 0xff, 0xff, 0xff), .driver_info = RTL8852B},
#endif /* CONFIG_RTL8852B */
#ifdef CONFIG_RTL8852BP
        /*=== Realtek demoboard ===*/
        {USB_DEVICE_AND_INTERFACE_INFO(USB_VENDER_ID_REALTEK, 0xA85C, 0xff, 0xff, 0xff), .driver_info = RTL8852BP},
#endif /* CONFIG_RTL8852BP */

        {}      /* Terminating entry */
};
        {.idVendor = USB_VENDER_ID_REALTEK, .idProduct = 0x8177, .flags = SPEC_DEV_ID_DISABLE_HT}, /* 8188cu 1*1 dongole, (b/g mode only) */
        {.idVendor = USB_VENDER_ID_REALTEK, .idProduct = 0x817E, .flags = SPEC_DEV_ID_DISABLE_HT}, /* 8188CE-VAU USB minCard (b/g mode only) */
        {.idVendor = 0x0b05,tic struct usb_device_id rtw_usb_id_tbl[] = {
#ifdef .idProduct = 0x1791, .flags = SPEC_DEV_ID_DISABLE_HT},
        {.idVendor = 0x13D3, .idProduct = 0x3311, .flags = SPEC_DEV_ID_DISABLE_HT},
        {.idVendor = 0x13D3, .idProduct = 0x3359, .flags = SPEC_DEV_ID_DISABLE_HT}, /* Russian customer -Azwave (8188CE-VAU  g mode) */
#ifdef RTK_DMP_PLATFORM

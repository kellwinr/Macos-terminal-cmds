### ADB Commands for Android Devices (USB DEBUG) 

#### Open, locate file via the Terminal
`cd ~/Desktop/platform-tools`

#### List detected ADB Devices
`adb devices`

#### Reboot connected/detected ADB device
`adb reboot`

#### Reboot connected/detected ADB device to bootloader
`adb reboot bootloader`

#### Reboot connected/detected ADB device's fastboot 
`fastboot reboot`

#### Flashing recovery file to connected ADB device while on fastboot mode
`fastboot flash recovery your_recovery_image_name.img`

#### ADB Guide/Help
`adb help`

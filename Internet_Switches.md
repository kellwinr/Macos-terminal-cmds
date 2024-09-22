## Internet Switches
### Turn off/on the WIFI (usually en0 for WIFI)

OFF `sudo ifconfig en0 down`

ON `sudo ifconfig en0 up`

**or (Only if the above command did not work)**

OFF ` sudo networksetup -setairportpower en0 off `

ON ` sudo networksetup -setairportpower en0 on `

### Flushing DNS
`sudo killall -HUP mDNSResponder`

`sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder`

### Disable IPv6
OFF `networksetup -setv6off Wi-Fi`

ON `networksetup -setv6automatic Wi-Fi`

.........

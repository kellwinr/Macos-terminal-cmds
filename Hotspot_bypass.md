## Bypassing Hotspot detection on modern macOS versions (tested on macOS 15.0)

1. Download the file from <a href="https://github.com/felikcat/unlimited-hotspot.git">this Github Repository</a>

2. After extracted, open the "unlimited-hotspot-main" folder, open the "macOS" folder.

3. **Open Terminal**

4. Run command with superuser (root) privileges.

`sudo -i`

5. cp *drag the set-ios-tcp-stack.sh file in, press Space, type in* /var/root

`cp {file} /var/root`

6. cp *drag the felikcat.set.ios.tcpstack.plist file in, press Space, type in* /Library/LaunchDaemons

`cp {file} /Library/LaunchDaemons`

7. This permission enables the file to be run as a program or script.

`chmod +x /var/root/set-ios-tcp-stack.sh`

8. This Ensures that it is enabled to run automatically in the future.

`launchctl load -w /Library/LaunchDaemons/felikcat.set.ios.tcpstack.plist`

9. Now we need to add three Packet Filter rules and enable PF.

`nano /etc/pf.conf`

10. Add the following three lines **before nat-anchor**:

`scrub in min-ttl 65`

`scrub out min-ttl 65 random-id`

`scrub reassemble tcp`

11. Reloads the Packet Filter (PF) firewall rules from the /etc/pf.conf file, applying any changes made to the configuration.

`pfctl -f /etc/pf.conf` 

12. Enables the Packet Filter (PF) firewall, making it start enforcing the configured rules

`pfctl -e`
_________________________________________________________________________________________________________________________________

### Routine Command
Run these 2 command after every sleep or restarts
1. Set outgoing IPv4 Packets to 65 (default value=64 on macOS)

`sudo sysctl -w net.inet.ip.ttl=65`

3. Set Hop Limit to 65 (default value=64 on macOS)

`sudo sysctl -w net.inet6.ip6.hlim=65`

--------------------------------------------------------------------------
## References
1. https://github.com/felikcat/unlimited-hotspot.git
2. http://noahdavids.org/self_published/TTL_values.html

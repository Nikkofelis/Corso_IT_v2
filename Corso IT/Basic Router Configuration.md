# Configuration Verification Commands

| Commands | Description |
| ------------- | ------- |
| `show ip interface brief` | The output displays all interfaces, their IP addresses, and their current status. The configured and connected interfaces should display a Status of “up” and Protocol of “up”. Anything else would indicate a problem with either the configuration or the cabling. |
| `show ip route` | Displays the contents of the IP routing tables stored in RAM. |
| `show interfaces` | Displays statistics for all interfaces on the device. However, this command will only display the IPv4 addressing information. |
| `show ip interfaces` | Displays the IPv4 statistics for all interfaces on a router. |

Every command with `ip` can use `ipv6` instead.

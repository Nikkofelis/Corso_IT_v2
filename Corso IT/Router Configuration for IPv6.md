First, the IPv6 must be enabled.

`Router(config-if)# ipv6 enable`: initialise an IPv6 LLA on the device

Then the same must be done for the unicast routing.

`Router(config)# ipv6 unicast-routing`: enable unicast routing

Configure all the interested interfaces the same way of the [IPv4](Switch%20and%20Router%20Configuration.md#Router%20Configuration).

`Router(config-if)# ipv6 address x::/prefix` : Assigning a GUA IPv6
`Router(config-if)# ipv6 address x:: link-local` : Assigning a LLA IPv6

DAD: Duplicate Address Detection, works similarly to the DHCP for IPv4 with the protocol (NDP).
This is similar to a public IPv4 address. These are ==globally unique, internet-routable addresses==. GUAs can be configured statically or assigned dynamically.

***

The hosts addresses are 2000:: /3

==001==0 0000 0000 0000::
LuH -> ==001==1 1111 1111 1111:ffff:ffff:ffff:ffff:ffff:ffff:ffff

2000::
3fff:ffff:ffff:ffff:ffff:ffff:ffff:ffff

***

# Address Parts

|        48 bits        |  16 bits  |   64 bits    |
|:---------------------:|:---------:|:------------:|
| Global Routing Prefix | Subnet ID | Interface ID |

- **Global Routing Prefix**: is the prefix, or network, portion of the address that is ==assigned by the provider==.
- **Subnet ID**: is used by an organisation to identify subnets within its site.
- **Interface ID**: is equivalent to the host portion of an IPv4 address. is used because a single host may have multiple interfaces, each having oIt ne or more IPv6 addresses.
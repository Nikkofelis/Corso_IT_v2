This is required for every IPv6-enabled device. Used to communicate with other devices ==on the same local link==. LLAs are confined to a single link. Their ==uniqueness must only be confirmed on that link (network)== because they are not routable beyond the link. In other words, routers will not forward packets with a link-local source or destination address.

***

fe80:: /10

f = 1111
e = 1110
8 = 1000
0 = 0000

==1111 1110 10==00 0000 -> Prefix Length

Network Address -> 1111 1110 1000 0000::
Last Usable Host -> 1111 1110 1000 0000:ffff:ffff:ffff:ffff:ffff:ffff:ffff

15 14 8 0::
15 14 11 15:ffff:ffff:ffff:ffff:ffff:ffff:ffff

fe80::
febf:ffff:ffff:ffff:ffff:ffff:ffff:ffff

64 - 10 = 54
2^54 - 1 Usable hosts

***

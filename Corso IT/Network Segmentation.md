#theory #practise

# Problems with Large Broadcast Domains

Hosts can generate excessive broadcasts and negatively affect the network by slowing down the network and confuse about the source of messages.

# Assign Sub-networks

Using a prefix length of /24 can allow to divide multiple device into sub-networks based on the needed parameters.

```ad-example
- **By Location**: A different subnet for each building floor
- **By Function**: A different subnet for each role or group
- **By Device type**: A different subnet for each type of device
```

## FLSM Method

If I need to create 256 subnets for the address 192.168.0.0 /16:

2^n >= 256

n must be the closest greater number than the desired subnets.

n = 8 variable bits are borrowed from the variable part (the most at the left) of the network address to create subnets.

192.168.==00000000==.00000000

Each new subnet will have an address as:

192.168.x.0 /16 + 8 = /24 = 255.255.255.0

The 3rd byte in the IP Address is called **subnet counter**.

0) 192.168.0.0 /24
1) 192.168.1.0 /24
...
64) 192.168.64.0 /24
...
255) 192.168.255.0 /24

***

10.0.0.0 /8 (100 subnets)

2^n >= 100

2^7 (128) >= 100

10.==0000000==0.00000000.00000000

10.x0.0.0 /8+7 = /15 = 255.254.0.0

1) 10.==0000000==0.00000000.00000000	10.0.0.0 /15
2) 10.==0000001==0.					10.2.0.0 /15
3) 10.==0000010==0.					10.4.0.0 /15
4) 10.==0000011==0.					10.6.0.0 /15
...
64) 10.==1000000==0.						10.128.0.0 /15
...

***

192.168.0.0 /24 (6 subnet)

2^n <= 6

n = 3

/24 + 3 = 255.255.255.11100000 = 255.255.255.224

0) 192.168.0.==000==00000	192.168.0.0 /27
1) 192.168.0.==001==00000	192.168.0.32 /27
2) 192.168.0.==010==00000	192.168.0.64 /27
3) 192.168.0.==011==00000	192.168.0.96 /27
4) 192.168.0.==100==00000	192.168.0.128 /27
5) 192.168.0.==101==00000	192.168.0.160 /27
6) 192.168.0.==110==00000	192.168.0.192 /27
7) 192.168.0.==111==00000	192.168.0.224 /27

2^5 (32) - 2 = 30 IP addresses assignable to hosts per subnet.

## VLSM Method

Usually used for public network. Allows to assign, in a more efficient way, IP Addresses.

17.16.0.0 /16
Subnet A: 64 hosts
Subnet B: 128 hosts
Subnet C: 10 hosts

***

Start from the most numerous subnet

B: IP = 128 + 2 = 130 IP Addresses

2^n >= 130 -> 2^8 -> /32 - 8 -> /24 -> 255.255.255.0

B: 17.16.0.0 - 17.16.0.255

***

Continue with the next most numerous subnet. But Start the available IP Address counting from the previous subnet address.

Next available IP: 17.16.1.==0==

A: IP = 64 + 2 = 66

2^n >= 66 -> 2^7 -> /32 - 7 -> /25 -> 255.255.255.10000000 -> 255.255.255.128

A: 17.16.1.0==0000000== = 17.16.1.0 - 17.16.1.127

***

Repeat for every other subnet.

Next available IP: 17.16.1.==128==

C: IP = 10 + 2 = 12

2^n >= 12 -> 2^4 -> /32 - 4 -> /28 -> 255.255.255.11110000 -> 255.255.255.240

C: 17.16.1.1000==0000== = 17.16.1.128 - 17.16.1.143

# [Network Segmentation Exercises](Network%20Segmentation%20Exercises.md)

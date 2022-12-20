# Rule 1: Omit Leading Zeros

To help reduce the notation of IPv6 addresses is to omit any leading 0s (zeros) in any hextet.

- 01ab -> 1ab
- 09f0 -> 9f0
- 0000 -> 0
- etc

# Rule 2: Double Column

A single double column (::) can replace any single, contiguous string of one or more 16-bit hextets consisting of all zeros.

2001:db8:0000:abcd:0000:0000:1234 can be written as:

- 2001:db8::abcd:0000:0000:1234
- 2001:db8:0000:abcd::1234

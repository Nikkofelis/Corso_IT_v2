UDP doesn't implement an error correction protocol, because this function is implemented into the higher layers

When the data are receiver, there are no confirmation response from the receiver.

More used in real time transmission.

# Header

8 bytes

|    Source Port (16)    | Destination Port (16)  |
|:----------------------:|:----------------------:|
|      Length (16)       |     Checksum (16)      |
| Application Layer Data | Application Layer Data |

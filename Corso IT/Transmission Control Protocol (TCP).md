Protocol connection oriented: 

Creation of a **session**

```ad-note
title: Session

Virtual protected environment between server-client, where the messages fragments are numbered and labelled
```

Part of the transmission is sent.
The receiver responds with a confirmation of arrival, and is now on waiting for the rest of the transmission.
If the response doesn't come through, the sender transmits again the non-received files, until a confirmation is received.

# Connection Establishment

three-way handshake process

1. SYN: the sender generate a random number (SEQ) to establish its own '0'
2. SYN and ACK: the sender acknowledges the sent '0' and expect the next message will be SEQ + 1 (ACK), then sends its own '0' (SEQ)
3. ACK: the sender acknowledges the receiver SEQ + 1 and sends the SEQ + 1 (ACK)

# Session Termination

1. FIN: the sender sends the to close its side of the session (half closed)
2. ACK: the receiver sends its ACK
3. FIN: the receiver sends its FIN
4. ACK: 

Flow control -> window size
Maximum Segment Size (MSS) -> Max size of data payload
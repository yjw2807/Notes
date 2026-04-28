| IPv4 header component      |       Size | What it means                                              |
| -------------------------- | ---------: | ---------------------------------------------------------- |
| **Version**                |     4 bits | IP version. For IPv4, this value is `4`.                   |
| **IHL / Header Length**    |     4 bits | Length of the IPv4 header. Minimum is 20 bytes.            |
| **DSCP / Type of Service** |     6 bits | Used for traffic priority and quality of service.          |
| **ECN**                    |     2 bits | Used for congestion notification without dropping packets. |
| **Total Length**           |    16 bits | Total size of the IPv4 packet, including header and data.  |


| **Identification**         |    16 bits | Helps identify fragments of the same original packet.      |
| **Flags**                  |     3 bits | Controls fragmentation, such as “don’t fragment.”          |
| **Fragment Offset**        |    13 bits | Shows where this fragment belongs in the original packet.  |
| **TTL**                    |     8 bits | Time To Live. Limits how many hops the packet can travel.  |
| **Protocol**               |     8 bits | Shows the next-layer protocol, such as TCP, UDP, or ICMP.  |
| **Header Checksum**        |    16 bits | Error-checking value for the IPv4 header only.             |
| **Source IP Address**      |    32 bits | Sender’s IPv4 address.                                     |
| **Destination IP Address** |    32 bits | Receiver’s IPv4 address.                                   |


| **Options**                | 0–40 bytes | Optional extra control information. Rarely used today.     |
| **Padding**                |   Variable | Fills the header so its length is a multiple of 32 bits.   |

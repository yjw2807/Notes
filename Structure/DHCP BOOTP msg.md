| Field          |      Size | Meaning                                                                             |
| -------------- | --------: | ----------------------------------------------------------------------------------- |
| `op`           |    1 byte | Message operation. `1` = request, `2` = reply.                                      |
| `htype`        |    1 byte | Hardware type. Ethernet is usually `1`.                                             |
| `hlen`         |    1 byte | Hardware address length. Ethernet MAC is `6`.                                       |
| `hops`         |    1 byte | Used by relay agents. Client usually sets this to `0`.                              |
| `xid`          |   4 bytes | Transaction ID used to match requests and replies.                                  |
| `secs`         |   2 bytes | Seconds elapsed since the client started trying to get an address.                  |
| `flags`        |   2 bytes | Includes the broadcast flag.                                                        |
| `ciaddr`       |   4 bytes | Client IP address, if the client already has one.                                   |
| `yiaddr`       |   4 bytes | “Your” IP address; the address offered or assigned to the client.                   |
| `siaddr`       |   4 bytes | Server IP address, often used for next server in boot process.                      |
| `giaddr`       |   4 bytes | Gateway/relay agent IP address.                                                     |
| `chaddr`       |  16 bytes | Client hardware address. For Ethernet, first 6 bytes are the MAC, rest are padding. |
| `sname`        |  64 bytes | Optional server host name.                                                          |
| `file`         | 128 bytes | Boot file name, used more in BOOTP/PXE boot.                                        |
| `magic cookie` |   4 bytes | Identifies DHCP options. Value is usually `63 82 53 63`.                            |
| `options`      |  Variable | DHCP options such as message type, subnet mask, router, DNS, lease time, etc.       |

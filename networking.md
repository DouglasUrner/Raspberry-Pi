# Raspberry Pi Networking

## MAC Address – Finding a Pi on your network

All Raspberry Pi MAC addresses start with `B8:27:EB`, you can find them with ARP:

```bash
arp -an | grep -i 'B8:27:EB'
```

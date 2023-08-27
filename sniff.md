# Packet sniffer
```
Usage: sniff [OPTIONS]
    -h      print this help message
    -1 IP       specify first IP address
    -2 IP       specify second IP address
    -o FILE     write output to FILE
    -i IFACE    which interface to listen on
    -m MODE     what mode to use for mitm (default is arp)
```

## How it works
The script uses the tool `ettercap` to sniff the packets between the two specified hosts. It's basically a wrapper to ease the use of the tool and requires the tho IP addresses (with options `-1` and `-2`) to both be specified.

The default network interface is `wlo1` and the default output file in pcap format is `output.pcap`. Both can be overridden with the `-i` and `-o` options respectively.

The script also allows to specify the mode to use for the mitm attack with the `-m` option. The default is `arp`, but it can be changed to any mode understood by `ettercap`, such as `dhcp` or `icmp`.
# Network scanner
## Usage
The script has the following usage:
```
Usage: scan [OPTIONS]
    -u          perform udp scan
    -a          perform attack with default scripts
    -t          perform tcp scan
    -f          full scans
    -d          discovery mode (only -i and -o relevant)
    -v          scan for OS version
    -o FILENAME redirect output to FILENAME
    -i IP       scan specified IP
    -m MODE     tcp scan mode
```

## How it works
The script uses the `nmap` tool to perform the scans. The script is written in such a way that it can be used to perform:
- a TCP scan
- a UDP scan
- a TCP scan with OS and version detection
- test the open ports of the target host
- discover and list hosts on the network

Moreover we can specify the scan mode for the TCP scan, which must be one of the ones accepted by `nmap`. The default behavior is to perform a scan only on the 1000 most common ports, but it can be changed to perform a full scan by using the `-f` option.

The default behavior of the script is to save the output of the commands in a file called `output` in the current directory. This can be changed by using the `-o` option. The script also accepts the `-i` option to specify the IP address of the target host, or of the network to scan in discovery mode, and it's always required. In discovery mode it is only possible to specify the IP of the network and the optional name of the output file, all other options are ignored.
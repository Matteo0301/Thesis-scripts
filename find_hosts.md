# Host finder
## Usage
```
Usage: find_hosts [OPTIONS]
    -h      print this help message
    -f FILE get old IP addresses from FILE
    -i IP   scan specified IP
```

## How it works
The script requires `nmap` to be installed and uses it to perform a ping scan on the network. The script then compares the results of the scan with the IP addresses that were previously found. If a new IP it is printed to the user. The script waits for the user to press enter between the two scans, so there is the time to connect the new devices o the network. If the user already has a list with the IP addresses of the devices on the network (in a file with one address per line), it can be passed to the script with the `-f` option. The script will then compare the results of the scan with the IP addresses in the file and print the new ones.
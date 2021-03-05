# server-investigator
This program is used to get you information about domains and servers. There are some components that search for exploits that should be fixed.

There are two included scripts:
1. runIPBlockScan.sh
2. runServerScan.sh
3. Small Scripts
    1. Check if an input IP is in a valid format
    2. Validate that a domain is real
    3. Make a bash array

runServerScan.sh - This automated ip scoping tool is used to investigate a target's external network.
This is a Black Box Scan, so we are looking for what we can from the outside.

runIPBlockScan.sh - This automated ip scoping tool is used to investigate a target's internet accessable servers.
This script will look for the physical location of the server, pull ip blocks that belong to that company. 

Everything is output to a txt file in the same directory that it was run for later viewing.

## Features
These scripts run a variety of commands using multiple tools. Information you will gather includes
1. Physical location of the server
2. IP Addresses of a domain
3. Domain Scoping
4. Subdomain Scoping
5. Host Information
6. Open Port Scanning
7. Investigate for Firewalls
8. DNS Investigation including checking for recursion. 

## Dependencies
runServerScan.sh requires the following:
```
sudo apt-get update
sudo apt-get install dnsrecon
sudo apt-get install dnsmap
sudo apt-get install nmap
sudo apt-get install whois
```

runIPBlockScan.sh
```
sudo apt-get install geoip-bin
wget https://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz
gunzip GeoLiteCity.dat.gz
sudo cp GeoLiteCity.dat /usr/share/GeoIP/
sudo apt-get installnmap
sudo apt-get installwhois
sudo apt-get installdnsmap
```

## Usage: 
```sudo bash runServerScan.sh```

```sudo bash runIPBlockScan.sh```

This script is interactive and is given variables in the program. 
Server Investigator runs best on Kali Linux. You can run this on other linux, but most parts of this script will not run.




## FINDINGS

## Scan Results summury 
*Total Hosts Scanned*: [256 (192.168.1.0/24 subnet)]
*Hosts with Open Ports*: [2]
*Total Open Ports*: [5]
*High Risk Servies*: [3 (FTP, HTTP, HTTPS)]

## High Risk Servies:
PORT           STATE             SERVICE             RISK
21             FTP               192.168.1.1         Unencrypted, vulnerable to brute-force
80             HTTP              192.168.1.1         Unencrypted, susceptible to sniffing
443            HTTPS             192.168.1.1         Potential for SSL/TLS vulnerabilities

##Open Port Services:
PORT          STATE             SERVICES        
21/tcp        Open              FTP
53/tcp        Open              DNS 
80/tcp        Open              HTTP
443/tcp       Open              HTTPS

->The host for all of the ports will be same 192.168.1.1

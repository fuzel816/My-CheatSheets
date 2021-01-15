# nmap commands #

## Suchen und Filtern ##

- Suchen nach offenen Telnet Ports, Filtern der Information nach der IP Adresse -> `nmap --open -p 23 10.1.13.0-255 -oG - | grep "/open" | awk '{ print $2 }'`

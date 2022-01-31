satip-client [![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)
============
Based on https://code.google.com/p/satip/

SAT>IP Client

Supported options in /etc/vtuners.conf:
- tcpdata:1 - uses TCP instead of UDP for the connection with the satip server
- force_plts:1 - forces sending plts=on as part of the satip request
- fe:X - send fe=X as part of the satip request to force a specific adapter (useful on multiple satellite connections on different adapters)
- ipaddr - the ip address of the satip server
- port - the port of the satip server

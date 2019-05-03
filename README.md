# ddns-update-formula

This project is designed to allow a Saltstack-enabled system to initiate an appropriate Dynamic DNS (DDNS) update request. It is intended to work in generic DDNS environments and environments that use the DNS-Integrated Active Directory service for DNS.

Pillar data will be used to govern the which underlying DDNS modules are used (see: [pillar.examples](pillar.examples] file). The contents of Pillar, in addition to defining which DDNS modules to use, will attempt to facilitate the use of any extensions (e.g., TSIG) required for the selected method's use against the target DNS servers. Initial support targets are:

- AD-integrated DNS &ndash; with initial Linxux support via [PBIS](https://github.com/BeyondTrust/pbis-open)
- ISC-compliant DNS (e.g., BIND) &ndash; with initial Linux support via bind-utils:
    - Generic (anonymous) DDNS
    - DDNS+TSIG

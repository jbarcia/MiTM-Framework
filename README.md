# MiTM-Framework
MiTM Framework
http://blog.barcia.me/2015/09/mitm-attack-script-updated/

The MiTM Attack Script has been updated. I removed and replaced ettercap with bettercap. I also added some new attack vectors including the following:

Captive Portal - Log In Creds / Reverse Shell
  Cisco
  Microsoft Forefront
  Sophos
  SQUID
  TrendMicro
  Fortigate\Fortinet
  Flash Updater
  Forttinet - Old Style
  Custom
Captive Portal - Log In Creds / Reverse Shell with DNS Spoof
  Same as above, except with DNS Spoofing
SMB - Hash Grab
  Inject a UNC path (in web pages) to the attackers SMB server to capture NetNTLM
SMB - Hash Relay
  Inject UNC path (in web pages) to the attackers SMB and relay/replay it to a victim
Web - Beef Hook
  Inject a beef hook into web traffic and starts beef
Web - SSL Strip and Capture Traffic
  Creates and stores a packet capture
Web - BDFproxy/BDFfactory
  Inject malicious code into exe download files
Web - Hamster/Ferret
  Intercept web cookies for stealing sessions

Original Blog Post:
https://github.com/CroweCybersecurity/MiTM-CaptivePortal


Some other options also include adding SSLstrip to all attacks and for picky gateways half duplex.

SSLstrip
  SSLStrip is a type of MITM attack that forces a victim's browser into communicating with an adversary in plain-text over HTTP, and the adversary proxies the modified content from an HTTPS server. To do this, SSLStrip is "stripping"  https:// URLs and turning them into http:// URLs.

Half Duplex
  Half duplex only sends arp poisoning to one target, this would be used when full poisoning is unachievable because the gateway/router would send another request to the real IP of the target asking it again for its mac address, invalidating the ARP cache of the target and fixing it. The --half-duplex command doesn’t send the second ARP packet, not spoofing the router, thus it won't be able to detect the ARP MITM and fix the targets ARP cache.

Since we (still) don't have active inspection/manipulation on a packet level, we don't really need full duplex, so that'll do the trick if you have issues with ARP poisoning on your network.”

Customizable
  Completely customizable options makes portability easy
  The encoder is a customer script and should be updated to fit your needs

-------------------------------------------------------------------------------------------------------------

Please let me know if something isn’t working correctly, this has been tested on a custom Kali 2.0 build.

# Proxies and VPN
## Why?
* IP Addresses can reveal your physical location
* View constricted content
* Bypass network blocks

## Proxy and VPN: Whats the diff? 
* $(diff proxy vpn)
* Proxy allows you to access a service via another machine
* **Limitations of Proxy**
  * Usually operate on the application level
  * Encryption? YMMV
  * DNS queries are not proxied by default
  * some proxies will still reveal yoru originating IP address
* WebRTC can reveal location
* Essentially route traffic through another machine
  * Proxy owners exert a lot of control over their proxy server
* **VPN**
  * A VPN will tunnel your traffic

## DNS
* Domain Name Servers
* Telephone books of internet
* translate IP address to human readable 
  * resolvers
  * Tier 1 - Authoritative server. Authority for the zone
  * Tier 2 - Second level server
  * Local resolvers - caches of IP (local network admin)

# VPN
* [Podcast](https://slate.com/technology/2019/03/vpn-use-and-trust-what-you-should-know.html "Slate podcast")
* Notable providers
  * **commercial**
  * Vypr
  * Private Internet Access
  * Mullvad
  * IVPN
  * Tunnelbear
  * **Non profit**
  * Riseup
  * Calyx Institute
  * Psiphon
  * **Self hosted**
  * Algo
  * Outline
* Questions to consider when picking vpn
  * Will it be accessible when/ where you need it?
  * Whats its stance towards logging and privacy?
  * Is it leaking DNS? IPv6?
  * Does it use robust encryption?

## Legal status of VPN
* Not illegal anywwhere
* > VPNs aren't illegal. Activity on vpn could be.
* [Deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection "Wikipedia article")

## Other
* [James Marshall](https://www.jmarshall.com/ "Marshall personal website")
  * CGIProxy
* [Lantern](https://en.wikipedia.org/wiki/Lantern_(software) "Wikipedia article") - P2P proxy
* [Iranian expats launch own telegram](https://www.rferl.org/a/iranian-expats-launch-own-telegram-with-built-in-proxy-to-counter-filtering-at-home-/29204673.html "Radio Free Europe")
* [Psiphon](https://psiphon.ca/en/download.html "Psiphon website")
  * Funded by US, Sweden, France
  * Storage located in Canada
  * 70% of Iran's traffic is routed through Psiphon
* [Proxy-chain](https://github.com/apifytech/proxy-chain "Github repo")
* Common local IP addresses
  * 192.168.x.x
  * 10.20.x.xc
* IPv6
  * uses hexadecimals
  * running out of IPv4 addresses 
* [Circumvention Central](https://cc.greatfire.org/en "chinese cyberfreedom group") - Chinese cyber freedom group
* OpenWrt||DD-WRT
* ![Datagram Image][http://bucarotechelp.com/networking/standards/images/IPv4dg.png]
* TCP/ UDP
  * Transmission Control Protocol - Lossless protocol
  * User Datagram Protocol - Lossy protocol
* Network Admins commonly block UDP VPN's due to bad reputation providers and torrent
  * Circumvent by enabling TCP on VPN provider
  * Run on ports 80||443 common HTTP/HTTPS ports

## Protocols
* [PPTP](https://en.wikipedia.org/wiki/Point-to-Point_Tunneling_Protocol "Wiki article") (Point-to-Point Tunneling Protocol)
* [L2TP/IPsec](https://en.wikipedia.org/wiki/Layer_2_Tunneling_Protocol "Wiki article") (Layer 2 Tunneling Protocol) 
  * Industry standard
* [OpenVPN](https://en.wikipedia.org/wiki/OpenVPN "Wiki article")
* [Wireguard](https://en.wikipedia.org/wiki/WireGuard "Wiki Article") - Newest VPN protocol

## Algo VPN
* [Github Repo](https://github.com/trailofbits/algo "github repository")
* change user config file
* wireguard protocol\*
* install wireshark
* `dumpcap --list-interfaces` = wireshark utility 
* `dumpcap -i <interface> -B <buffersize e.g. 2MiB> -w <filename_>
* Wireshark GUI
  * Preferences > add column > date
  * Source, destination
  * TCP default color is purple
  * Follow stream collates data packets
  * File > export objects > http
  * Endpoints
  * [Max mind geolite2](https://dev.maxmind.com/geoip/geoip2/geolite2/ "max mind website")
    * Wireshark utility that looks up geolocation


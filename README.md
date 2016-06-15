# network
Zusammenfassung unserer Netze

## ipv4

Beantragt bei https://github.com/freifunk/icvpn-meta/
* 10.68.0.0/18
* Adresse: 10.68.0.0
* Netzmaske: 255.255.192.0 = 18
* Netzwerk: 10.68.0.0/18
* HostMin: 10.68.0.1
* HostMax: 10.68.63.254

### Aufteilung

#### Gateways ...
* 10.68.0.0 / 24 ist den GWs und den damit verbundenen Diensten vorbehalten

* 10.68.0.1 ist das gw falterturm (gw01)
* (02 - 10 Platz, ggf. VRRP für GW01)
* 10.68.0.11 wird eventuell irgendwann gw deustertor (gw02)
* (12 - 20 Platz, ggf. VRRP für GW02)
* 10.68.0.21 wird eventuell irgendwann gw schwanberg (gw03)
* (22 - 30 Platz, ggf. VRRP für GW03)

* 10.68.0.200 ist für next_node in der Firmware belegt.
 
#### Richtfunkstrecken, Dienste, feste lokale IPv4-Adressen
* 10.68.1.0 / 24 - Richtfunkstrecken ohne Gluon-FW und ggf. Controller, nur Assigned nach Absprechen etc...
* 10.68.2.0 / 24 - Reserve
* 10.68.3.0 / 24 - Router/Switche, die ohne Gluon-FW besser laufen, nur Assigned nach Absprechen etc...
* 10.68.4.0 / 24 - Reseve
* 10.68.5.0 / 24 - VPN-Router, die private Netzwerke durch das Freufunk-Mesh leiten, nur Assigned nach Absprechen etc...
* 10.68.6.0 / 24 - Reserve
* 10.68.7.0 / 24 - Dinge, worauf die Community Lust hat; Frei zur statischen Verwendung für Server etc, die im Netz zur Verfügung stehen sollen...
* 10.68.8.0/24 bis 10.68.15.0/24 - Reserveblöcke

#### DHCP-Bereiche

* 10.68.16.0 / 20 - DHCP-Bereich mit 4096 Hosts
* 10.68.32.0 / 20 - DHCP-Bereich für 2tes GW in Zukunft
* 10.68.48.0 / 20 - DHCP-Bereich für 3tes GW in Zukunft

##ipv6

### lokaler Bereich
lokaler Bereich beantragt bei https://github.com/freifunk/icvpn-meta/
fdef:ffc0:8fff::/48

### HE-Tunnel
2001:470:6d:83::/64 (Tunnel)
2001:470:5035::/48 


# Secure Home Network

## Subnet Definitions

Let's start with some subnets definitions:

 * VPN subnet
    * For indidivual users
    * B2B (or rather Home-2-Home) networks will use individual subnets.
 * WiFi
    * `guest`
    * `kids`
    * `main`
 * Docker/VMs
    * For any kind of VMs, Kubernetes, etc.
 * Infrastruktura
    * Switches, routers, APs, management interfaces of NAS, anything else fitting this category (e.g. Docker mgmt)
    * LDAP, Kerberos, Keycloak
 * Home network
    * Most likely the same thing as the `main` Wi-Fi network.

### VPN

TBD.

### Infrastructure

TBD.

### Home Network

TBD.

## Daemons & Technologies

Just a list of things
 * NTP
 * FreeIPA
   * de-facto standard for LDAP & Kerberos
 * DHCP
   * Can be integrated with FreeIPA
   * [FreeIPA DHCP Integration Design](https://www.freeipa.org/page/DHCP_Integration_Design)
 * DNS
   * dns-over-https support would be cool
   * pi-hole integration (filter out all the ads and nastyness)
   * Cloudflare DNS servers could be used as well (for both IPv4 and IPv6)
   * Needs to be integrated with FreeIPA
 * Keycloak
   * SSO, social network accounts & registration, ...
 * Docker (or any better kind of conteiners support)
   * Or `podman` perhaps, as it's more supported by RedHat/CentOS
   * See https://thenewstack.io/check-out-podman-red-hats-daemon-less-docker-alternative/ for more information
 * SMTP
   * What's the recommended SMTP server these days?
 * Wireguard
   * As it's a modern VPN solution, with IPv6 support, native Linux implementation, etc.
 * Proper bastion- (jump-) server
   * So that all the management accesses are properly routed through a single place
   * SSH Stepstone
 * nginx & haproxy
   * most likely, as some of the services will be HTTPS based
 * let's encrypt agent
   * as we need certificates
 * Log management
   * syslog (rsyslog, syslog-ng)
   * ELK/Splunk/Graylog
 * Monitoring
   * grafana
   * prometheus
   * icinga(?)
 * Network IDS
   * Suricata/Bro
   * **Question**: routing vs mirroring on switches? Both possible, different purposes
 * Anything from the HomelabOS project
   * PlexTV
   * Hosted mail app
   * Wiki

Also:

```
  fvechecker
  proxmox -- VM hypervisor 
  pi-hole
  octopi
  diskstation,ds
  TV
  NIDSSensor
```


# AS 4242421964 / SPF-NET
I operate [AS 4242421964](https://explorer.burble.com/?#/4242421964) in DN42. The ranges `172.23.24.32/27` and `fd4f:b934:7802::/48` have been reserved for this purpose. At the moment, a full mesh is in use to avoid split-horizon issues in iBGP.

## Nodes
Quick overview of the available nodes:
| Hostname                  | Location       | Bandwidth    | OS              | Supported protocols |
|---------------------------|----------------|--------------|-----------------|---------------------|
| nl1.dn42.southparkfan.org | Netherlands 🇳🇱 | >= 1000 Mbit | Debian Buster   | WireGuard           |
| nl2.dn42.southparkfan.org | Netherlands 🇳🇱 | >= 1000 Mbit | Debian Bullseye | WireGuard           |
| fr1.dn42.southparkfan.org | France 🇫🇷      | >= 100 Mbit  | VyOS 1.4        | OpenVPN, WireGuard  |

### nl1.dn42.southparkfan.org
- Status: being decommissioned 🚧
- In use since: January 2022
- Physical location: Alblasserdam, Netherlands
- ISP: RamNode
- Clearnet IPv4: 176.56.237.46/32
- Clearnet IPv6: 2a00:d880:11::396/128
- DN42 IPv4: 172.23.24.33/32
- DN42 IPv6: fd4f:b934:7802::1/128
- Link-local IPv6: fe80::ade0
- Port: 4 + \<last four digits of your AS number\> (only if your AS number starts with `424242`)
- Multi-protocol BGP: supported ✔
- Supported protocols: WireGuard
- WireGuard public key: `OBpyD/rruK4pOCgRVrWVoexBNHZadtn4qwPmrEjt0gY=`
- Routing daemon: Bird 2.0

### nl2.dn42.southparkfan.org
- Status: online ✔
- In use since: July 2022
- Physical location: Amsterdam, Netherlands
- ISP: Vultr
- Clearnet IPv4: 95.179.143.233/32
- Clearnet IPv6: 2001:19f0:5001:1f9a:5400:4ff:fe0d:d8f1/64
- DN42 IPv4: 172.23.24.35/32
- DN42 IPv6: fd4f:b934:7802::3/128
- Link-local IPv6: fe80::ade0
- Port: 4 + \<last four digits of your AS number\> (only if your AS number starts with `424242`)
- Multi-protocol BGP: supported ✔
- Supported protocols: WireGuard
- WireGuard public key: `GsmcrWbFTcje5e+hmc0D6qonrkTpHksGZuk0cLBjDmY=`
- Routing daemon: Bird 2.0

### fr1.dn42.southparkfan.org
- Status: being decommissioned 🚧
- In use since: May 2022
- Physical location: Paris, France
- ISP: Vultr
- Clearnet IPv4: 95.179.219.72/32
- Clearnet IPv6: 2a05:f480:1c00:f7b:5400:3ff:fefd:4756/128
- DN42 IPv4: 172.23.24.34/32
- DN42 IPv6: fd4f:b934:7802::2/128
- Link-local IPv6: fe80::ade0
- Port: 4 + \<last four digits of your AS number\> (only if your AS number starts with `424242`)
- Multi-protocol BGP: supported ✔
- Supported protocols: OpenVPN, WireGuard
- WireGuard public key: `DHKTSvfaIhXdT07udajvVGtIt0NGMAqTjztrdVKGQzQ=`
- Routing daemon: FRRouting

## Peering with me
Welcome! I have set the following standards:
- Only export routes with valid ROAs (and no clearnet routes, of course). I'll drop routes that are not valid.
- WireGuard is preferred for connecting with my nodes, but OpenVPN may be used if my node supports it.
- Multi-protocol BGP is preferred, but not required. Let me know if you need separate sessions for IPv4 and IPv6.
- I prefer to peer over IPv6 link-local, although it's not mandatory.
- Even though transit traffic is fine, please be considerate. The nodes do not have unlimited traffic. 

You can contact me via [Libera Chat](ircs://irc.libera.chat:6697) or [hackint](ircs://irc.hackint.org:6697) (my name is `southparkfan`). The template below may be used for reference:
```
* Name and email address:
* DN42 AS number:
* Your clearnet endpoint (<IPv4/IPv6/FQDN>:<port>):
* Protocol (usually WireGuard):
* WireGuard public key (if applicable):
* Session type (IPv4/IPv6 separate or multi-protocol BGP):
* NIC IP addresses (usually DN42 IPv4 + link-local IPv6: 
* BGP peering IP(s) (usually link-local IPv6):
```

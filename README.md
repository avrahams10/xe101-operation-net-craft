# XE101 — Operation Net Craft

**Historical Home-Network Mapping and Introductory Public-Information Research**  
**Original student project | Avraham Thomas**

## Overview

XE101 is my **original student network-documentation project**, completed during cybersecurity training. I recorded a historical household LAN inventory, classified wired and wireless endpoints, described the gateway's addressing roles, and explained **DHCP, DNS, ARP, routing, and NAT**. A second part introduced publicly available information through **Shodan and WHOIS**.

This is a **retrospective, sanitized case study**—not a current description of my home network, a live vulnerability scan, a penetration test, or evidence that router hardening was performed.

## Documented asset inventory

| Recorded role | Quantity | Connectivity |
| --- | ---: | --- |
| Desktop PCs | **2** | Ethernet |
| Printer | **1** | Ethernet |
| Laptops | **3** | Wi-Fi |
| Tablet | **1** | Wi-Fi |
| Default gateway / router | **1** | Infrastructure |

The historical source contains **seven endpoints plus one gateway**: **three wired** and **four wireless** endpoint devices. The report also recorded DHCP/DNS information and a **/24** IPv4 subnet mask; those entries describe configuration, **not additional devices**.

### Conceptual topology (roles only)

```text
                    Internet / ISP
                          |
                    Router / gateway
                   DHCP / DNS endpoint
                          |
                  +-------+-------+
                  |               |
               Ethernet         Wi-Fi
                  |               |
          2 PCs + printer   3 laptops + tablet
```

This reconstruction uses **generic device roles**, not addresses, MAC prefixes, exact router settings, or the historical household drawing. It is not a current network diagram or a verified access-control map.

## Network services and interpretation

| Concept | What was documented | Evidence limit |
| --- | --- | --- |
| **DHCP** | Address-configuration roles and Discover–Offer–Request–Acknowledge | No preserved lease export or packet-level exchange |
| **DNS** | Router configured as the DNS endpoint; name-resolution explanation | Does not prove a separate DNS server or a specific printer record |
| **ARP** | Local IPv4 next-hop to link-layer resolution | Explained, not demonstrated by a packet capture |
| **Gateway / ISP / NAT** | Off-subnet forwarding and typical home IPv4 translation | No independently verified live route or NAT state table |

The recorded inventory and the explanatory protocol examples must not be confused with live packet-level evidence or an independently revalidated device discovery run.

## Introductory external-information research

**Shodan:** The historical report states that a search returned **no results**, but the exact query, response capture, and timestamp were not retained. A no-result claim **does not prove** security, absence of exposed services, or invisibility on the internet.

**WHOIS:** The project preserved a historical **domain-registration record** and a separate **IP-range registration record**. The latter was not demonstrated to be connected to the household's actual WAN address. Registration data alone does not establish an exposed port, an exploitable system, or the household's live network configuration.

No fresh Shodan or WHOIS searches were performed as part of this publication-candidate preparation.

## Skills, provenance and limitations

The project demonstrates device classification, Ethernet/Wi-Fi topology documentation, introductory network reasoning, and cautious interpretation of public information. The original inventory and external-information study were **student work**. Later portfolio preparation reorganized and sanitized that historical material; it did **not** produce a new investigation or validated hardening outcomes.

Recommendations such as reviewing Wi-Fi settings, router administration, and firmware are **future security practices**, not actions proven by the original report.

## Repository contents

This repository contains a **documentation-only case study**. It does not include the original school PDF or topology drawing, router screenshots, household IP/MAC addresses, ISP identifiers, WHOIS contact information, or private case-study evidence. Future figures or exhibits require separate privacy and ownership review.

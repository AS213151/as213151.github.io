---
layout: page
title: Peering Policy
permalink: /policy/
---

AS213151 maintains an open peering policy, signed formal agreements are not required.

## Interfaces

Only remote peerings via WireGuard tunnels are currently available.

## Costs

Peerings with AS213151 is cost-neutral for both parties.

## Routing & Filtering
- Incoming routes are filtered against IRR (RIPE, APNIC, RADB, etc.)
- Peers must not announce private address space (RFC1918, RFC4193)
- Peers must not announce private ASNs
- Peers must not configure static or default routes to our routers
- Peers may only send traffic to destinations announced by AS213151
- Peers may only send traffic originating from their own or customer networks
- Peers must operate a NOC which is reachable by phone or email
- Peers should cooperate in any case of abuse

## Prefixes
AS213151 originates the following prefixes:
- 2a06:e881:7300::/40
- 2001:678:1e8::/48

## SLA
No explicit SLA is guaranteed. This network operates on a best-effort basis.

## Want to peer?
Great! Send a mail to peering@as213151.net.
Include your ASN, your prefix limit count and your preferred peering location.


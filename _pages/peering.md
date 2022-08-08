---
layout: page
title: Peering
permalink: /peering/
---

## Policy

AS213151 practices an open peering policy which means that we peer with everyone who wants to peer with us. While we do not require any kind of written contract, you must follow these rules:

- Peers may only send traffic from their own and downstream networks to us.
- Peers may only send traffic to destinations announced by AS213151.
- Peers must not configure static or default routes to our routers.
- Peers must operate a Network Operations Center (NOC) reachable by email.
- Peers must keep their IRR and registry data up to date at any time.
- Peers shall enforce a strict routing policy to avoid route leaks.
- Peers shall aggregate their routes to avoid routing table inflation.
- Peers should cooperate in any case of abuse.

## Interfaces

Peerings are possible at the following points of presence:
- [DE-CIX Frankfurt - Frankfurt, DE](https://www.peeringdb.com/ix/31)
- [KleyRex - Frankfurt, DE](https://www.peeringdb.com/ix/123)
- [LocIX - Frankfurt, DE](https://www.peeringdb.com/ix/2084)

## Costs

Peering with AS213151 is cost-neutral for both parties.

## Routing & Filtering

Please note the following preferences and technical information before entering a peering with us:

- Prefixes are filtered against IRR (RIPE, APNIC, RADB, etc.) and RPKI.
- Prefixes shorter than a /24 (IPv4) or /48 (IPv6) will be filtered.
- Prefixes with private or other invalid ASNs in AS_PATH will be filtered.
- Prefixes with private address space (RFC1918, RFC4193) will be filtered.
- Prefixes pointing to well-known bogon addresses will be filtered.
- Prefixes with invalid NEXT_HOP attribute will be filtered.
- We strongly encourage MD5 authentication for additional security.
- We support usage of the GRACEFUL_SHUTDOWN community.
- We configure an individual prefix limit for all peering sessions.

### Mutually Agreed Norms for Routing Security (MANRS)

[![Logo of MANRS](https://as213151.net/images/MANRS.png)](http://www.manrs.org/)

In our efforts to improve Internet routing security, we have joined [MANRS](http://www.manrs.org/), which is a global initiative, supported by the Internet Society, that provides essential fixes to reduce the most common routing threats.

As part of our membership with MANRS, AS213151 commits to adhere to four concrete actions to reduce routing threats:

- Filtering
- Anti-Spoofing
- Coordination
- Global Validation

### Resource Public Key Infrastructure (RPKI)

[RPKI](https://rpki.readthedocs.io/en/latest/) is a method to help prevent BGP hijacking and Route Leaks. It uses cryptographic signatures to validate that an ASN is allowed to announce a particular Prefix. 

AS213151 has deployed RPKI Route Validation and Filtering. We reject RPKI Invalids on all BGP Sessions.

|RPKI State|Description|Policy|
|---|---|---|
|Valid|Correct IP/masklength from the correct origin AS according to the ROA.|Accept|
|Unknown|No ROA registered.|Accept|
|Invalid|Incorrect masklength and/or origin AS according to the registered ROA.|Reject|

AS213151 also maintains valid Route Origination Authorizations (ROA) for all originated prefixes. 

## Prefixes
AS213151 originates the following prefixes:
- [2a06:e881:7300::/40](https://apps.db.ripe.net/db-web-ui/query?searchtext=2a06:e881:7300::/40)
- [2001:678:1e8::/48](https://apps.db.ripe.net/db-web-ui/query?searchtext=2001:678:1e8::/48)
- [185.197.135.0/24](https://apps.db.ripe.net/db-web-ui/query?searchtext=185.197.135.0/24)

## Communities

|Description|Large Community|
|---|---|
|**Info: Origin Route**|
|Originated by AS213151|`213151:100:1`|
|**Info: Transit Route**|
|[Hurricane Electric](https://www.peeringdb.com/asn/6939)|`213151:200:6939`|
|[Meerfarbig](https://www.peeringdb.com/asn/34549)|`213151:200:34549`|
|[FreeTransit (Openfactory)](https://www.peeringdb.com/asn/41051)|`213151:200:41051`|
|[iFog](https://www.peeringdb.com/asn/34927)|`213151:200:34927`|
|**Info: IXP Route**|
|[DE-CIX Frankfurt](https://www.peeringdb.com/ix/31)|`213151:300:6695`|
|[KleyReX](https://www.peeringdb.com/ix/123)|`213151:300:31142`|
|[LocIX Frankfurt](https://www.peeringdb.com/ix/2084)|`213151:300:202409`|
|**Info: Peering Route**|
|[DFN](https://www.peeringdb.com/asn/680)|`213151:400:680`|
|[Apple](https://www.peeringdb.com/asn/714)|`213151:400:714`|
|[Hurricane Electric](https://www.peeringdb.com/asn/6939)|`213151:400:6939`|
|[GlobalConnect](https://www.peeringdb.com/asn/12552)|`213151:400:12552`|
|**Info: Customer Route**|
|[RIPE RIS](https://www.peeringdb.com/asn/12654)|`213151:500:12654`|

## SLA
No explicit SLA is guaranteed. This network operates on a best-effort basis.

## Want to peer?
Great! Send a mail to [peering@as213151.net](mailto:peering@as213151.net).
Include your ASN, your prefix limit count and your preferred peering location.


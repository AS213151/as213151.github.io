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
- [2a06:e881:7300::/40](https://stat.ripe.net/2a06:e881:7300::/40)
- [2001:678:1e8::/48](https://stat.ripe.net/2001:678:1e8::/48)
- [185.197.135.0/24](https://stat.ripe.net/185.197.135.0/24)

## Communities

|Description|Large Community|
|---|---|
|**Info: Origin Route**|
|Originated by AS213151|`213151:100:1`|
|**Info: Transit Route**|
|Meerfarbig|`213151:200:1`|
|Hurricane Electric|`213151:200:2`|
|FreeTransit (Openfactory)|`213151:200:3`|
|iFog|`213151:200:4`|
|**Info: IXP Route**|
|DE-CIX Frankfurt|`213151:300:1`|
|KleyReX|`213151:300:2`|
|LocIX Frankfurt|`213151:300:3`|
|**Info: Peering Route**|
|Hurricane Electric|`213151:400:1`|
|DFN|`213151:400:2`|
|Asympto|`213151:400:3`|
|**Info: Customer Route**|
|RIPE RIS|`213151:500:1`|
|Isolario Project|`213151:500:2`|

## SLA
No explicit SLA is guaranteed. This network operates on a best-effort basis.

## Want to peer?
Great! Send a mail to [peering@as213151.net](mailto:peering@as213151.net).
Include your ASN, your prefix limit count and your preferred peering location.


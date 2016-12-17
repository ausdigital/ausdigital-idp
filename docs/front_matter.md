# ADBC Identity Provider (IDP) Specification

-   Status: raw
-   Editor: Chris Gough
-   Contributors: Steve Capell

This document describes a federated model for providing identity
assurance for secure business messaging. The initial development is
focussed on supporting digital procure-to-pay protocols (in particular
the Australian e-Invoicng Framework), however the design is intended to
be more generic than that.

This specification is based on the widely used [OpenID
Connect](https://en.wikipedia.org/wiki/OpenID_Connect) standard (OIDC)
for authentication and authorisation. The specification uses the defined
extension mechanism in OIDC to provide a standardised set of scopes,
claims, and identity assurance levels.

These extensions:

 * Allow a person or online service to prove they have authorisation to update business metadata on behalf of a business. This authorisation is necessary to orchestrate the various distributed components that are involved in secure business messaging.
 * Simplify the adaption of existing identity schemes for secure business messageing procure-to-pay applications.
 * Leave jurisdictions free to regulate local business identity however they like.

This specification does not create or nominate any central authority,
other than to propose that identity providers implement this open
standard consistently. Instead, it is based on the idea of an *identity
market* that spans multiple jurisdictions, where participants and
individuals make their own decisions about trust.

This specification exists to support the Australian Digital Business
Council [e-Invoicing initiative](https://ausdigital.github.io), and is
under active development at
<https://github.com/ausdigital/identity-provider>.


## Licence

Copyright (c) 2016 the Editor and Contributors. All rights reserved.

This Specification is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License as published
by the Free Software Foundation; either version 3 of the License, or (at
your option) any later version.

This Specification is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
Public License for more details.

You should have received a copy of the GNU General Public License along
with this program; if not, see <http://www.gnu.org/licenses>.


## Change Process

This document is governed by the
[2/COSS](http://rfc.unprotocols.org/spec:2/COSS/) (COSS).

## Language

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT",
"SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this
document are to be interpreted as described in RFC 2119.

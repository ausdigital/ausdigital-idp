# Known Customers

The ADBC IDP Specification has a requirement to support fully automated
workflows. Some OIDC tokens provide persistent authorisation, but there
are some automated business to business processes where the End-User is
unlikely to be available to provide authorisation in realtime.

Our solution is what we call a "Known Customer" authentication. This
combines "on behalf of" relationship between businesses with contractual
proof of consent. The credential security of Known Customer
relationships is intriniscally weak, therefor needs to be supported by
strong perimeter security processes such as legal protection, audit,
monitoring, review and dispute resolution capabilities.

Known customer relationship is only allowed for LOA1 and LOA2 claims.

Support for Known Customers at LOA-1 or LOA-2 requires an aditional API
(not part of OIDC), to allow the trusted business to:

 * Assert that the business identity is a known customer request a JWT with a known customer's identity claim and "manage business metadata" authorisation scope.

TODO: cross reference API specifications

There must be a contractual relationship between the RP and the trusted
business, that ensures known customer assertions are auditable and
operated with appropirate security precautions.

An LOA-1 claim essentially relies on offline authorisation by the
business, through commercial/contractual arangements between End-User
businesses and the organisation that has a Known Customer relationship
with them.

An LOA-2 claim is like an LOA-1 claim, except the commercial/contractual
relationship between End User businesses and the organisation issueing
authorisations on their behalf is regulated by the KYC regulations in
the Jurisdiction of the Identity Scheme that the claim is made under.

The JWT is issued through the REST API, not using the OIDC protocol.
However, once issued it can be validated and renewed as though it were
issued through the OICD protocol (Authorisation Code Flow).

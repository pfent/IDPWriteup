# Intro
structure of this work

# Related work
## ACME smime extension:
https://tools.ietf.org/html/draft-ietf-acme-email-smime-02

letsencrypt FAQ explicitly does not issue such certificates and is not affiliated with that draft
https://letsencrypt.org/docs/faq/#does-let-s-encrypt-issue-certificates-for-anything-other-than-ssl-tls-for-websites

## Previous work instead of related work for securemail

# PKI -> Background

## PGP WoT
https://www.gnupg.org/gph/en/manual/x547.html
Several problems for organizations, difficulty to scale
key rotations made uneasy


# 3.4 certificates at TUM

small analysis with requirements
* centralized system to have consistent encryption standards
* integrated with TUM services / user management
* usable on *all* platforms, ideally browser-based

# 4 Design

## Flow diagram
To show the interaction of different stakeholders / components

## DFN *without* human RA:
DFN PKI CP : https://www.pki.dfn.de/fileadmin/PKI/DFN-PKI_CP.pdf
> 3.2.3 Authentification of a natural person

Needs to be checked in-person ("persönliche Identitätsprüfung"), but not necessarely for each new certificate, but needs to be documented.
Most organization's identity checks should already comply with those rules, e.g. at Matriculation / empolyment.

## "Einschränkungen" / Limitations
Nobody ever did such an "transfer" of authenticity with DFN certificates, yet.
Probably needs DFN regulatory rules.

# 5 Implementation

# Overview over components
            Gradle Build
 ________________/\________________
/                                  \
Frontend            --REST-- Backend
Built with node         CMS: certificate component & database persistency & models
Typescript              WEB: Authentication / user information with LDAP, certificate publishing with LDAP, 
Structured by pages          REST Interface within different "Controllers": Users, X509 CSR + finished certificates, separate OpenPGP

# 6 Discussion and Future Work
**NEW CHAPTER**

* wie das neue System den Status Quo verbessert

* copy / pasta future work

* was noch zu tun ist, bis das System vollends funktioniert. integration mit der wirklichen CA
(organisatorischer Schritt, damit diese Lösung DFN-compliantz ausgerollt werden dürfte)

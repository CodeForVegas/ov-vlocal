<!--
 Copyright (C) 2022 Innovate for Vegas Foundation
 
 This file is part of ov-vlocal.
 
 ov-vlocal is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.
 
 ov-vlocal is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with ov-vlocal.  If not, see <http://www.gnu.org/licenses/>.
-->

# vLocal Personal Profile Features

It is likely that an individual holder of at least one identity on the vLocal platform will want or need a public profile that is reachable via a url which they may share or otherwise reference, and which may be a part of a collection of identities (or credentials) held by the individual. That is, there may be more than one identity for one individual, related but mutually exclusive to maintain privacy per use of and reference to multiple identities, and the same will likely be true of credentials (see additional details below). A simplifying assumption for personal profiles, identities, and credentials, is to presume zero information sharing and that any given individual does not want profile information made public. On the other hand, it is likely that a given individual will want or need a public profile with some information made visible.

A privacy-aware identity profile will need a URL and a landing page of some sort, if showing only the minimal info (that an identity and/or some credential exist, visible in a web browser and via other means via APIs, etc). This personal profile spec is essentially a baseline, on which the entity profile spec can be built with differences.

## Highest Priority Considerations

We should assume that an individual has at least one identity and one credential, and that these are private and anonymous or pseudononymous. When generating a profile view or generally providing information about the identity,the association of the identity profile with an actual person should be, by default, undetermined. The privacy aware nature of the platform must always account for individual privacy settings and general privacy policies as they relate to the particular identity or identities and all credentials and personally identifying information (PII).

In general there must always be attention paid to the approach that zero data is shared and build up from there to the desired sharing preference and policy for a given scenario, so that we will avoid personal data leaks.

## Specification Details

The personal profile is a baseline bolus of information about a single human person, intended to provide authentication of the identity at that baseline without explicit association with a physical person. This is similar to the OpenPGP scheme of key generation and key trust, based on attestation but not requiring attestation, leaving a particular key pair (credential) verifiable, but not necessarily directly associate-able with a particular individual. While a government issued identification device could be associated with an identity, this is a feature to consider in some distant future. Initially, authentication of an individual person will be focused on the identity and the credential, not on the physical person.

There is no initial plan to offer integrated authorization services associated with identities and credentials. Management of individual authorization per identity or credential is left to an outside client once authentication is confirmed. This could be implemented at some later date, but would require substantially more architecture and security than we already need to manage.

### Public HTML

If a user chooses to make an identity visible and public, a structured HTML page will be available with machine-readable schema.org markup (in addition to OpenGraph meta tags and rel meta tags for simple identity such as with mastodon user verification). The public profile is essentially a normal online profile page, but for the additional structured information, and optional credential information, such as a PGP public key or a named VerusID or something similar. Specific options will appear in User Stories below.

There are at least four options for this public HTML page view:

1. A public identity with at least one public credential will appear together at a known URL, suitable for sharing or similar.
2. A public identity with zero public credentials will not show any credentials but will be shareable.
3. A private identity will appear at a valid URL with relevant identity validity information (at least HTTP response codes, eg 200 or 404)
4. A non-existent or invalid identity will appear at a previously-valid URL, or an invalid URL, and will return an appopriate HTTP response code (eg 404)

Note that private identities should not have any information associated with them that indicate a user name, location, or other PII.

### Hierarchy

In order to support privacy-aware identity, but at the same time supporting a public, visible identity scheme to enable public identity profiles and similar, a one-way identity hierarchy will be essential.

A private child identity of a public parent will be provably owned by the same person (as an alternate personal identity) without divulging the public information visible in the public identity profile.

## External Reference Materials

[Applied Cryptography Book](https://www.schneier.com/books/applied-cryptography/)

## User Stories

Individual stories may be converted into Issues, or consolidated or exploded as needed for development and implementation.

**Terms**:

- **Person**: a human with one or more identities.
- **Entity**: a non-human with one or more identities and one or more responsible Persons associated.
- **Consumer**: any service requesting identity and/or credential authentication and/or validation.
- **Provider**: the vLocal service(s) responding to Consumer requests and generally providing identity and credential responses

### Typical Uses

- **Card**: As a Person, I would like to make details about my identity visible to the general public.
  - **Conversation**: Similar to a personal profile page found on various social media platforms, but with structured identification and credential information (eg PGP Public Keys, etc) avalable in human- and machine-readable format.
  - **Confirmation**:
    - Person profile page displays current persona, identity, and credential details which have been made public according to Person preferences and platform policies.

---

- **Card**: As a Person, I would like to use my vLocal Personal Profile to verify my identity with a Mastodon account.
  - **Conversation**: Mastodon and other online services sometimes enable the use of a link tag with a rel attribute set to indicate that the document containing the link (or meta) tag and data can be used as a response to a service query. A Person should be able to add this rel (ie relationship) information to their profile and that information should be included in the HTML page structure where appropriate.
  - **Confirmation**:
    - Person profile page displays current Person details which have been made public, appropriate link and/or meta tags with identity information included.

---

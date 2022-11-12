<!--
 Copyright (C) 2022 Code for Vegas Foundation
 
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

# vLocal Public Keyserver Features

One of the older, yet still-used technologies available broadly for user data encryption and authentication is OpenPGP, which enables regular and high-value use of Public Key Infrastructure methodologies to encrypt and sign messages, which enables attestation trust assignments and checking, private messaging, message content validation without encryption, etc.

An OpenPGP Keyserver is an established technology and for first releases of the vLocal platform an OpenPGP Keyserver is a feature integration requirement

## Highest Priority Considerations

An OpenPGP Keyserver stores public key data only, with the user completely responsible for maintaining the security of their private key(s). The security of the key storage component of the keyserver is thus moot, as all data is public by design.

However, with the privacy-aware application focus of the vLocal platform in general, it is important to be clear about when an OpenPGP Public Key (which includes an email address) is associated in a visible or public way with a personal identity, which may or may not be public. Thus while the OpenPGP Public Key materials are public, they also include PII by design, and must not be directly linked or linkable to private personal identity materials where these private identity materials may be used for such applications as medical services data capture for data equity analysis, etc.

## Specification Details

The OpenPGP Keyserver specification and multiple implementations are available as open source projects, initial deployment of this component is an integration effort of the keyserver and the vLocal platform.

Note that the notion of keyserver peer sync/share of public key data is or was a part of the typical deployment, it is important to include support for peer key sync and share.

## External Reference Materials

[OpenPGP.org](https://www.openpgp.org/)

## User Stories

Individual stories may be converted into Issues, or consolidated or exploded as needed for development and implementation.

**Terms**:

- **Person**: a human with one or more identities.
- **Entity**: a non-human with one or more identities and one or more responsible Persons associated.
- **Consumer**: any service requesting identity and/or credential authentication and/or validation.
- **Provider**: the vLocal service(s) responding to Consumer requests and generally providing identity and credential responses

### Typical Uses

- **Card**: As a Person, I would like to publish my public PGP key for other Person, Entity, or general Consumer access to it
  - **Conversation**: Pervasive access to public keys for Persons removes one barrier to use of secure email and similar messaging and message content validation and sender verification.
  - **Confirmation**:
    - Person is able to upload public key and verify an associated email address via a URL or HOTP value or similar sent to the email address associated with the public key
  
---

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

# vLocal Services Summary

vLocal is a privacy aware identity platform conceived to enable a collection of services aimed at user authentication (eg for single-sign-on or SSO logins), identification (eg verification in blinded transactions), and such additional services as public key management and sharing, and secure credential storage and management. This is a blue-sky list but is achievable through integration of existing open source legacy and modern technology platforms and an integration and user experience effort into the future.

There are old and new ways of providing and managing digital online identity, for authentication, authorization, and data capture as examples. Because the vast majority of casual users of services that might require or benefit from a digital identity, are not well-versed in the old and new ways and how they function, part of the mission of the vLocal platform should be to make trusted and reliable use of digital identity trustworthy and transparent.

## Highest Priority Considerations

This consideration can not be highlighted and underscored enough:

User Privacy and Personal Identifying Information Security are paramount. There is no need to qualify this, it is the most important thing.

## Specification Details

TBD

## External Reference Materials

## User Stories

Individual stories may be converted into Issues, or consolidated or exploded as needed for development and implementation.

**Terms**:

- **Person**: a human with one or more identities.
- **Entity**: a non-human with one or more identities and one or more responsible Persons associated.
- **Consumer**: any service requesting identity and/or credential authentication and/or validation.
- **Provider**: the vLocal service(s) responding to Consumer requests and generally providing identity and credential responses

### Typical Uses

- **Card**: As a Person, I would like to identify myself to a third party Consumer requesting an identity with attestation, but without my name and home address visible to the third party.
  - **Conversation**: Use of a privacy-aware personal identity to respond to survey or other service identity requests can enable a Person to interact with services, and the Consumer service to interact with a Person without gaining unnecessary access to Personally Identifying Information which Person may not wish to share.
  - **Confirmation**:
    - Person can provide Identity and Credentials as needed by third party Consumer so that Consumer can trust the authenticity of identity and credential information without gaining access to additional PII.

---

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

# vLocal Credential Storage Features

As part of a drive to make security and privacy commonplace in our smart city, support for securely storing user credential information using established, tested, and highly-regarded open source tools and methods is a sensible feature to include in the vLocal platform. The initial component selection is the Bitwarden server and other tools, which are open source and self-hostable, and which include mobile and browser-integrated user-facing tools for credential management.

While Bitwarden is the first choice, it may not be the only choice, thus abstraction of any interfaces and design assumptions to enable other options is advisable.

## Highest Priority Considerations

This goes without saying, but the storage of a user *vault* which is a Bitwarden secure storage container for secret user data must be handled with absolute care and attention to security details. This applies to any other solution for user secret storage.

## Specification Details

The initial selection of the Bitwarden technology stack for a self-hosted and highly-regarded user secret storage feature makes specification more a matter of integration details than implementation.

A suitably-abstracted interface to the Bitwarden components to connect to and with the vLocal platform, should be flexible enough to allow alternate component selections if needed.

## External Reference Materials

[Bitwarden Open Source](https://bitwarden.com/open-source/)

## User Stories

Individual stories may be converted into Issues, or consolidated or exploded as needed for development and implementation.

**Terms**:

- **Person**: a human with one or more identities.
- **Entity**: a non-human with one or more identities and one or more responsible Persons associated.
- **Consumer**: any service requesting identity and/or credential authentication and/or validation.
- **Provider**: the vLocal service(s) responding to Consumer requests and generally providing identity and credential responses

### Typical Uses

- **Card**: As a Person with secrets to store in the cloud, I would like to be able to store my secrets securely using tried and trusted tools and methods.
  - **Conversation**: Companies such as Apple and Google are offering credential storage integrated with their mobile and desktop browsers, and more recently as part of system services in the operating systems of their respective mobile devices. Use of open source tools with tested and supported native mobile applications and user tools will empower each Person to control and keep their secret credentials and other information regardless of the vendor solutions they chose.
  - **Confirmation**:
    - Person is able to create a cloud storage vault and manage their secrets securely using readily available tools (eg Bitwarden)

---

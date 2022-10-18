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

# vLocal Overview

This Overview repository is a specification and documentation component of the vLocal Project. Please do not add code or other resources to this repository.

The goal of the vLocal Project is to provide a privacy-aware digital identity platform which may be used for a variety of applications in the virtual and real worlds by Locals.

The populace should be able to use various services and perhaps conduct various types of commerce and communications, using a virtual identity scheme that they can trust, and which is useful in a uniform way (thereby being more easily understood, and hopefully then, more trustworthy again). By developing and deploying a city-scale identity platform that is open for use for a variety of applications, but which may be inspected by its users, we endeavor to build a culture of secure trust and privacy control placed in the hands of the users of their identity and the services attached to it.

## Project Policies

Unless otherwise and specifically indicated with replacement files in this repository, this project will adhere to the default Code for Vegas Foundation policies for Code of Conduct and Contributing, found at

* [Code of Conduct - Code for Vegas Foundation](https://github.com/CodeForVegas/.github/blob/main/CODE_OF_CONDUCT.md)
* [Contributing to this Project - Code for Vegas Foundation](https://github.com/CodeForVegas/.github/blob/main/CONTRIBUTING.md)

## Services Summary

There are old and new ways of providing and managing digital online identity, for authentication, authorization, and data capture as examples. Because the vast majority of casual users of services that might require or benefit from a digital identity, are not well-versed in the old and new ways and how they function, part of the mission of the vLocal platform should be to make trusted and reliable use of digital identity trustworthy and transparent.

## Legacy Support

The internet is built on a variety of tried-and-true legacy practices and protocols. Few are perfect, but many are still in use so many years later. In order to provide a gentle introduction to securely-signed emails and encrypted messages, this platform should enable support for OpenPGP keys and key management, and possibly support for S/MIME and other secure email/data signing and encrypting platforms.

## Modern Methods

Use of blockchain or similar shared ledger schemes is a good fit for this platform. Integration with legacy schemes will be a small challenge but ultimately the ability to onboard users into a secure, privacy-aware digital identity platform that we may then use across multiple services (developed by Code for Vegas Foundation volunteers or others) for a variety of use cases.

## Services

### OpenPGP Keyserver

As a part of a gentle introduction, if that is even possible in this area, use of and support for PGP/GPG keys for message signing is a reasonable first step. On the client side, a signed email message is a normal email message with a signature attachment, the message can be read without any additional knowledge of email signatures. Building on that notion with a vLocal keyserver for key sharing, and some education about key management, will make use of the old ways, which are decades credible, without concern about headlines and rugpulls and whatnot.

### X.509 Certificate Server

This is by no means a near-term goal, but at some point integration with S/MIME certificate issuance and associated services, to enable secure messsaging across a variety of users and clients, would help to complete the picture of old ways integration. S/MIME if used, is typically found in corporate or government agencies, and is not so often used between indiduals. However, the ability to inform users about how S/MIME works, how the certificates work, and how they can verify messages received are examples we might include in an onboarding and general user education.

### Blockchain ID

TBD

## References

<https://www.openpgp.org/>

<https://en.wikipedia.org/wiki/S/MIME>

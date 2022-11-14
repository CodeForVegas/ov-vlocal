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

# vLocal Entity Profile Features

It is likely that a non-person (generically, an entity) holder of at least one identity on the vLocal platform will want or need a public profile that is reachable via a url which they may share or otherwise reference, with information content which a party responsible for that entity may control. We can assume that more often an entity will be some non-anonymous business, agency, or service. Aside from this difference in the non-human assumption, an entity and an individual human person are rather similar in feature and function.

Here we can describe the differences between the entity and personal profiles and, by extension, the differences between feature sets and expectations between an individual (human) account and an entity account.

## Highest Priority Considerations

We should assume that an entity has at least one personal (human) account holder as owner or responsible party. When generating a profile view or generally providing information about an entity,the association with one or more individuals and their personal accounts must be aware that, while an entity may be public, the individual(s) might not be. Thus the privacy aware nature of the platform must always account for individual privacy settings and general privacy policies as they relate to the particilar identity or identities related to a particular entity.

In general there must always be attention paid to the approach that zero data is shared and build up from there to the desired sharing preference and policy for a given scenario, so that we will avoid personal data leaks.

## Specification Details

The personal profile features generally align with the entity profile features, except where they do not. Since a non-person entity is presumed to be public or at least non-private, it is more likely that a standard business or government agency or similar information profile will be a minimal structure to return, with additional information depending on associated personal profiles, whether they are public, etc.

### Public HTML

A human-readable HTML webpage at a public URL very much like a personal profile, but with specific elements that we can cover here. It would be completely legitimate to make the entity and personal profile implementations one in the same with appropriate parameterization, so long as the zero-sharing initial conditions are always assumed. An HTML file with entity profile information will likely contain all of the relevant profile information, rather than enabling selection of data, but at the same time the generation of that page will be via use of a query interface to retrieve the profile data, thus we should always assume that the content of the HTML view is not quired to be everything.

An entity will most likely be a business, agency, service, or perhaps a job role that is public (for example, a member of a City Council is an individual role, held by an individual person for some period of time, and there are likely many similar examples we can examine as this spec is revised) and so it will encompass and display public details (business name or role title, etc) which could be generalized as schema.org annotated markup of names, titles, addresses, and so on (schema.org has a rich set of object types at present and is extensible).

There are several options for a public HTML profile view:

1. A public entity with one or more public responsible personal identities visible
2. A public entity with zero public responsible personal identities visible
3. A private entity with minimal information visible
4. A private entity with zero information visible
5. A non-existent, expired, or invalid entity (a valid or invalid URL which receives an appropriate HTTP response code, eg 404)

The key difference between an entity profile and a personal profile, then, is the attachment or association of zero or more personal identities of different persons with the given entity.

### Hierarchy

Any entity may have a parent entity and multiple child entities. In the example above, a City Council Member is a child of City Council. In other examples, a specific business location could be a child of a general business entity, eg a single Starbucks location as a child of the Starbucks entity.

This is an advanced feature but provides flexible compatibility with real-world relationships and open data structures, and will automatically enable specific personal identity associations at a granular level rather than globally attaching personal identities to entities. A responsible personal identity attached to any entity can be associated with child entities, or not, while personal identities are not associated with parent entities (they can be associated explicitly), which enables a reasonably robust service view of entity-person relationships for authorizing access to entity profile data (to create, edit, delete, etc).

Here again, the key difference between entity and personal profiles are the association of personal identities of zero or more different persons with an entity.

## External Reference Materials

[Schema.org](https://schema.org)

## User Stories

Individual stories may be converted into Issues, or consolidated or exploded as needed for development and implementation.

**Terms**:

- **Person**: a human with one or more identities.
- **Entity**: a non-human with one or more identities and one or more responsible Persons associated.
- **Consumer**: any service requesting identity and/or credential authentication and/or validation.
- **Provider**: the vLocal service(s) responding to Consumer requests and generally providing identity and credential responses

### Typical Uses

- **Card**: As an Entity, I would like to make details about my identity and responsible Persons visible to the general public.
  - **Conversation**: These are similar in concept to a Local page, or a Business Page, or Company Profile, found in most social media platforms or mapping tools or other directories, but are in the vLocal context integrated in to the underlying Person identity features.
  - **Confirmation**:
    - Entity profile page displays current Entity details which have been made public, including one or more responsible Person references for specific contact and profile management permissions.

---

- **Card**: As an Entity, I would like to use my vLocal Entity Profile to verify my Entity with a Mastodon account.
  - **Conversation**: Mastodon and other online services sometimes enable the use of a link tag with a rel attribute set to indicate that the document containing the link (or meta) tag and data can be used as a response to a service query. A responsible Person should be able to add this rel (ie relationship) information to their profile and that information should be included in the HTML page structure where appropriate.
  - **Confirmation**:
    - Entity profile page displays current Entity details which have been made public, including appropriate link and/or meta tags with identity information included.

---

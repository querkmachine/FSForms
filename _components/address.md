---
title: Address
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/address" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When collecting a user's physical address. 

## When to consider something else

Consider whether collecting the user's full address is necessary. For example, some payment services don't require a full billing address, asking only for the user's postcode. Information about the user's location can additionally by gained using geolocation and IP lookup, depending on the type of information and level of accuracy needed.

Some users will not be comfortable disclosing their address. Provide messaging on why you need it, and provide the facility for the user to remove this information if it's not needed on an ongoing basis. 

## Guidance

Asking for the address in a single text field is preferable, as it mirrors how the user will typically write an address and accounts for all possible permutations. Addresses can be infinitely complex and there is no "one size fits all" solution. For example, a parcel addressed to our office can be variably written as:

Felinesoft Ltd.<br>
4th Floor, North Block, The Quorum<br>
Bond Street South<br>
Bristol, County of Bristol<br>
BS1 3AE, United Kingdom

and:

Felinesoft<br>
The Quorum<br>
BS1 3AE

Each address contains a significant difference in the format of information, but both addresses are valid and both will result in the parcel arriving at the correct location. There are hundreds of permutations between these two that are also possible and also valid. 

### Validating input

Addresses should be validated as a whole. Do not try to validate specific elements of the address. 

Because of the wide variance in address formats between countries, all parts of the address should be optional. 

Try to avoid strictly validating the user's address. Although doing so can be useful for ensuring the user hasn't made a mistake, address databases rarely contain all possible addresses—for example, they often exclude new builds and converted flats that have a shared front entrance. The user should be able to bypass address validation if necessary.

### Multiple fields

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/address-alt" | relative_url }}" width="100%" height="300"></iframe>
</figure>

If it is necessary to collect the address as multiple fields, such as for integration with backwards third parties, try to reduce the inputs to the smallest number of fields possible. Remember that many fields (such as address line 2 and county) are usually wholly unnecessary when finding where a person lives.

The below shows an address field with all possible address fields and their intended usage according to the W3C spec. 

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/address-full" | relative_url }}" width="100%" height="300"></iframe>
</figure>

### Address lookup

Aim for address lookup to search the user's entire address, ideally doing so as they're typing. This allows the user to type any part of their address to search (convenient if they've recently moved house and haven't memorised the postcode), and allows them to stop typing as soon as their intended result is in the suggested options. 

Services such as Loquate and Google Maps provide services that allow searching by the entire address and not just the postcode.

Address lookups should populate an editable field so that, in the event that the user cannot find their address via lookup, they can still manually edit or add missing information. 

Address lookups generally only work for UK addresses. Avoid using them if you're trying to accommodate a large and varied user base. 

### Internationalisation

The standards and formats for addresses vary significantly between locales and even within individual countries. Creating a multi-input address form that complies with all standards is practically impossible, so using a single input is preferable when dealing with large audiences. 

#### Format

Some countries write addresses "backwards," that is, starting with the largest division and getting increasingly small. For example, Japanese addresses begin with the prefecture and work downwards. Japan is also a good example of the extremely different permutations an address may have. In written order they may be:

* Prefecture name (except for Tokyo, Kyoto and Osaka, which have special designations).
* Municipality.
* *Machi* and *chōme* (districts are often numbered, e.g. Asakusa 4) OR *ōaza* and/or *aza* and/or *koaza* (except Ryūgasaki, which doesn't use any area smaller than municipality).
* Town (for non-city areas) OR ward (if a city) OR special ward (for Tokyo).
* Block and building number (e.g. 5&zwj;番&zwj;10&zwj;号) OR block, building and apartment number (e.g. 5&zwj;番&zwj;10&zwj;-&zwj;301&zwj;号) OR land registry number (which may be written in several formats) OR a designator that land does not have a land registry number.

Everything from *chōme* downwards can be numbered. So it is also possible to write the above address as Asakusa 4-5-10-301.

#### Street address formats

Not all countries use UK-style street addresses. Japan, for example, does not name streets but names city blocks instead, so a person may live in "Hiroshima, Asakita 5&zwj;番&zwj;10&zwj;号" (building 10 of block 5, Asakita ward, in the city of Hiroshima). Mannheim in Germany uses a similar system, where a person may live at "C3 17" (block C3, building 17). Block based systems can cause issues, as the entrance to the address can be on any one of four different streets. 

There is also variance in how users write address formats. For example, some people prefer to list their flat number before their building number, whereas others prefer to put building number first. 

#### Postal codes

Some countries do not have any formal postal code system, such as Hong Kong and many African nations. 

Some countries have postcode-like systems that are not technically postal codes, such as Ireland and the Netherlands. 

Some countries and territories have a single postal code for the entire country, such as Anguilla, the Falkland Islands, and the Vatican.
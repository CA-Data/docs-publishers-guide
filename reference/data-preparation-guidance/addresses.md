# Addresses

## Why valid addresses matter

* Consistent formatting of valid addresses is important for accurately mapping and referencing geographic information
* A poorly formed address could end up mapping to the wrong geographic reference or not at all, reducing the usefulness of the data
* Poorly formed addresses can make cleanup of data labor intensive and result in reporting errors where geography (neighborhoods, census, etc.) is concerned
* Poorly formed addresses could also result in additional costs because of things like:
  * Undeliverable/returned mail
  * Failure to apply benefits to recipients appropriately based on geography
  * Poor routing of vehicles or people in the field

## Address formatting

* Addresses should be output with the level of detail relevant to the data
  * e.g. permits can be applied down to the sub-address level
* If providing addresses in a complete string, make sure the addresses are well formed and consistent for easy parsing, for example:
  * 741 Ellis Street, Unit 5, San Francisco, CA 94109
  * 901 Bayshore Boulevard, Unit 209, San Francisco, CA 94124
* When providing multiple addresses within a dataset, prepend your column names with the type of address
  * e.g. address vs. mailing\_address

## Address elements

Below are some common elements of an address (but not all)

* Not all addresses will have all elements
* Address granularity will be driven by the business need, so not all systems will collect every element
  * Note: systems can be designed to validate or lookup addresses on entry, minimizing error
* Make sure the individual elements of an address line up with the guidance below
* You can publish addresses as either single strings or break into separate fields

> **Note:** this guidance is provided to promote consistency across the bulk of shared tabular datasets and not as a comprehensive guide to address standards. For a comprehensive standard on addressing, see the [Federal Geographic Data Committee (FGDC) United States Thoroughfare, Landmark, and Postal Address Data Standard](https://www.fgdc.gov/standards/projects/address-data)

| Element                     | Data Type | Definition                                                                                                                                                                                                                                                                                                                                                                                      |
| --------------------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| From Address Number         | Numeric   | First part of a range: **1000**-1100 Main Street, San Francisco, CA 94102                                                                                                                                                                                                                                                                                                                       |
| To Address Number           | Numeric   | Second part of a range: 1000-**1500** Main Street, San Francisco, CA 94102                                                                                                                                                                                                                                                                                                                      |
| Address Number Prefix       | Numeric   | The portion of the Complete Address Number that precedes the Address Number itself: **B**315 Main Street, San Francisco, CA 94102                                                                                                                                                                                                                                                               |
| Address Number              | Numeric   | The numeric identifier for a land parcel, house, building, or other location along a thoroughfare or within a community: **315**A Main Street, San Francisco, CA 94102                                                                                                                                                                                                                          |
| Address Number Suffix       | Text      | The portion of the Complete Address Number that follows the Address Number itself: 315 **A** Main Street, San Francisco, CA 94102                                                                                                                                                                                                                                                               |
| Street Name Pre Modifier    | Text      | A word or phrase in a Complete Street Name that 1. Precedes and modifies the Street Name, but is separated from it by a Street Name Pre Type or a Street Name Pre Directional or both, or 2. Is placed outside the Street Name so that the Street Name can be used in creating a sorted (alphabetical or alphanumeric) list of street names.: 315A **Old** Main Street, San Francisco, CA 94102 |
| Street Name Predirectional  | Text      | A word preceding the street name that indicates the directional taken by the thoroughfare from an arbitrary starting point, or the sector where it is located: 315A **East** Main Street, San Francisco, CA 94102                                                                                                                                                                               |
| Street Name Pretype         | Text      | A word or phrase that precedes the Street Name and identifies a type of thoroughfare in a Complete Street Name: **US Route** 101, San Francisco, CA                                                                                                                                                                                                                                             |
| Street Name                 | Text      | The portion of the Complete Street Name that identifies the particular thoroughfare (as opposed to the Street Name Pre Modifier, Street Name Post Modifier, Street Name Pre Directional, Street Name Post Directional, Street Name Pre Type, Street Name Post Type, and Separator Element (if any) in the Complete Street Name.): 315A **Main** Street, San Francisco, CA 94102                 |
| Street Name Posttype        | Text      | A word or phrase that follows the Street Name and identifies a type of thoroughfare in a Complete Street Name: 315A Main **Street**, San Francisco, CA 94102                                                                                                                                                                                                                                    |
| Street Name Postdirectional | Text      | A word following the street name that indicates the directional taken by the thoroughfare from an arbitrary starting point, or the sector where it is located: 315A Main Street **East**, San Francisco, CA 94102                                                                                                                                                                               |
| Street Name Post Modifier   | Text      | A word or phrase in a Complete Street Name that follows and modifies the Street Name, but is separated from it by a Street Name Post Type or a Street Name Post Directional or both: 315A Main Street **Extended**, San Francisco, CA 94102                                                                                                                                                     |
| Occupancy Type              | Text      | The type of occupancy to which the associated Occupancy Identifier applies. (Building, Wing, Floor, Apartment, etc. are types to which the Identifier refers.): 315A Main Street, **Apt** 2, San Francisco, CA 94102                                                                                                                                                                            |
| Occupancy Identifier        | Text      | The letters, numbers, words, or combination thereof used to distinguish different subaddresses of the same type when several occur within the same feature: 315A Main Street, Apt **2**, San Francisco, CA 94102                                                                                                                                                                                |
| City                        | Text      | The city the address sits within: 315A Main Street, **San Francisco**, CA 94102                                                                                                                                                                                                                                                                                                                 |
| State Name                  | Text      | The names of the US states and state equivalents: the fifty US states, the District of Columbia, and all U.S. territories and outlying possessions. A state (or equivalent) is "a primary governmental division of the United States." The names may be spelled out in full or represented by their two-letter USPS or ANSI abbreviation: 315A Main Street, San Francisco, **CA** 94102         |
| ZIP code                    | Numeric   | A system of 5-digit codes that identifies the individual Post Office or metropolitan area delivery station associated with an address: 315A Main Street, San Francisco, CA **94102**                                                                                                                                                                                                            |
| ZIP+4                       | Numeric   | A 4-digit extension of the 5-digit Zip Code (preceded by a hyphen) that, in conjunction with the Zip Code, identifies a specific range of USPS delivery addresses: 315A Main Street, San Francisco, CA 94102-**1212**                                                                                                                                                                           |

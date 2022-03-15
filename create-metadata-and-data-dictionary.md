---
cover: >-
  https://images.unsplash.com/photo-1501594907352-04cda38ebc29?crop=entropy&cs=srgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHwxfHxjYWxpZm9ybmlhfGVufDB8fHx8MTY0MDAzMTE0NA&ixlib=rb-1.2.1&q=85
coverY: 0
---

# 📙 3. Create Metadata and Data Dictionary

Metadata is data about data. Metadata describes the dataset’s structure, data elements, its creation, access, format, and content. A data dictionary is a type of metadata that focuses on the data elements.

Metadata is necessary to improve the discoverability of data within the open data portal and on external search engines. The more relevant information the search engine has about your data resources, the easier it will be for users to find.

**Without good metadata, datasets are prone to getting lost.** Below we define minimum standards and best practices for:

1. [Creating good metadata](create-metadata-and-data-dictionary.md#create-your-metadata)
2. [Creating a good data dictionary](create-metadata-and-data-dictionary.md#create-your-data-dictionary)

{% hint style="success" %}
****:open\_file\_folder: **Resource reminder!**

Use the metadata template [started in Step 1](review-the-pre-publishing-checklist.md#start-documenting-your-data) to document according to this guide.&#x20;
{% endhint %}

## Create your metadata

### **Metadata checklist**

* [ ] Fill in the metadata fields relevant to your dataset - [see metadata field definition reference](reference-and-additional-documents/metadata-field-definitions.md)
* [ ] Make sure your dataset title is accessible and user friendly - [see best practices below](create-metadata-and-data-dictionary.md#best-practices-dataset-title-content)
* [ ] Ensure your dataset description is accessible and user friendly - [see best practices below](create-metadata-and-data-dictionary.md#best-practices-dataset-description-content)

{% hint style="info" %}
****:open\_file\_folder: **Additional** **Resources.** Refer to [Metadata Field Definitions ](reference-and-additional-documents/metadata-field-definitions.md)for definitions of and further guidance on metadata fields.&#x20;
{% endhint %}

{% hint style="success" %}
:mega: **Want to provide feedback on future metadata guidance?**

We want to develop additional human-centered practice guides. [Fill out the form to indicate interest](https://airtable.com/shrvIiRHxyAAEsq41).
{% endhint %}

### ****:page\_with\_curl: **Best practices: Dataset title content**

| **Do's**                                                  | **Dont's**                                                                                                                                                                                                                                                                                            |
| --------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| :white\_check\_mark: Keep titles concise and informative. | <p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Avoid using CA or California in the title if it does not meaningfully clarify the scope.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Avoid using jargon and spell out acronyms.</p> |

#### **Illustrative examples**

Click on the&#x20;

{% tabs %}
{% tab title="Example 1" %}
**Title:**&#x20;

<mark style="color:red;">SW\[1]</mark> - Toxicity in <mark style="color:red;">CA\[2]</mark>&#x20;



**Comments:**&#x20;

<mark style="color:red;"></mark>:x:<mark style="color:red;">\[1]:</mark> Uses an acronym in the title that is not clearly understood by the public.&#x20;

<mark style="color:red;"></mark>:x:<mark style="color:red;">\[2]:</mark> Uses CA in the title. This creates redundancy, as all datasets published on the CA Open Data Portal pertain to California.&#x20;
{% endtab %}

{% tab title="Example 2" %}
**Title:**&#x20;

Surface Water - Freshwater Harmful Algal Blooms from <mark style="color:red;">2016-2021\[1]</mark>



**Comments:**&#x20;

:white\_check\_mark:Overall, clear and concise title.&#x20;

<mark style="color:red;"></mark>:x:<mark style="color:red;">\[1]:</mark> Includes an unnecessary date range. This could lead to a need to update the title, and failing to update it could lead to potential misinformation about the content of the dataset.&#x20;
{% endtab %}
{% endtabs %}

### ****:page\_with\_curl: **Best practices: dataset description content**

| **Do's**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Dont's**                                            |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| <p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Create a summary paragraph that details the contents of your data table. The first few sentences are the most important.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Address the following points, if applicable:</p><ul><li>Data collection method and source (not the name of the database, but from what process, people, or organizations does the data come)</li><li><p>Purpose of dataset</p><ul><li>Include relevant ordinance references, particularly if the method or elements collected are defined in law</li></ul></li><li>Programs or policies this data supports</li></ul><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Include related legislation info if applicable.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Include relevant acronyms, but make sure to clearly define them at least once.</p> | :x: Avoid using acronyms in your first few sentences. |

****

**Illustrative examples**

{% tabs %}
{% tab title="Example 1" %}
**Description:**&#x20;

Freshwater **** harmful algal bloom <mark style="color:blue;">(HAB)\[1]</mark> data from the Freshwater Harmful Algal Bloom <mark style="color:blue;">(FHAB)\[1]</mark> Reports database. The <mark style="color:blue;">FHAB Reports database\[2]</mark> is the California State Water Resources Control Board's data system for data and <mark style="color:blue;">information voluntarily reported through the Freshwater Incident Form found on the CA HABs Portal\[3]</mark>. <mark style="color:blue;">Due to the voluntary basis of information\[4]</mark> and data included in the database, data and information may include: waterbody name and location, algal bloom location and observed characteristics, observed and/or analytical sampling results, advisory signs, waterbody and/or land management, general information and updates regarding bloom status.

&#x20;

**Comments:**&#x20;

****:x:Overall, this description does not include a defined purpose for the dataset.&#x20;

<mark style="color:green;"></mark>:white\_check\_mark:<mark style="color:blue;">\[1]:</mark> Includes relevant acronyms and properly defines them.&#x20;

<mark style="color:green;"></mark>:white\_check\_mark:<mark style="color:blue;">\[2]:</mark> Lists data source.&#x20;

<mark style="color:green;"></mark>:white\_check\_mark:<mark style="color:blue;">\[3]:</mark> Specifies data collection method.&#x20;

<mark style="color:green;"></mark>:white\_check\_mark:<mark style="color:blue;">\[4]:</mark> Specifies limitations of dataset.&#x20;
{% endtab %}

{% tab title="Example 2" %}
**Description:**&#x20;

Surface water toxicity data from the <mark style="color:blue;">California Environmental Data Exchange Network (CEDEN)\[1]\[2]</mark>. <mark style="color:blue;">CEDEN is the California State Water Board's data system for surface water quality in California\[3]</mark>, and seeks to include all available statewide data (such as that produced by research and volunteer organizations). <mark style="color:blue;">Data in CEDEN include field, sediment and water column data collected from freshwater, estuarine, and marine environments\[4]</mark>. Examples of data in CEDEN come from laboratory, physical and biological analyses and include data types associated with chemical, toxicological, field, bio-assessment, invertebrate, fish, and bacteriological assay assessments.&#x20;



<mark style="color:blue;">The data resource "Surface Water Toxicity" contains two provisionally assigned values ("DataQuality" and "DataQualityIndicator") to help users interpret the data quality metadata provided with the associated result\[5]</mark>.&#x20;



**Comments:**&#x20;

<mark style="color:blue;">****</mark>:white\_check\_mark:<mark style="color:blue;">\[1]:</mark> Includes relevant acronyms and properly defines them.

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[2]:</mark> Specifies data source.

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[3]:</mark> Lists the program this data supports.&#x20;

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[4]:</mark> Clearly lists the contents of the dataset.&#x20;

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[5]:</mark> Includes relevant guidance on how to best utilize the data resource.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Stuck on best practices, need advice?**

Send a message on the [CalData Communities Open Data Channel](https://teams.microsoft.com/l/channel/19%3a037b34f454d94a9fa7f6aa964c052af4%40thread.tacv2/Open%20Data?groupId=0f45987a-e632-4e93-be66-ebfd6079e926\&tenantId=68a88534-151d-4e79-8046-09be7890656c). If you need access, [sign up here](https://forms.office.com/Pages/ResponsePage.aspx?id=NIWoaB0VeU6ARgm-eJBlbP8EsQ790KZKrhPJ1tkPH1JURjFWN1paMUtURFU5TFZOSjdTNVFZMkxEQi4u).
{% endhint %}

## Create your data dictionary

A data dictionary is the information you provide that defines the fields in your data and how the data can be used.

### **Data dictionary checklist**

* [ ] For each field, document the field name, field label, data type, definition and valid values if applicable - [see detailed reference on these elements](reference-and-additional-documents/data-dictionary-what-to-include.md)
* [ ] Write field definitions in user friendly language - [see best practices below](create-metadata-and-data-dictionary.md#best-practices-field-definitions)

{% hint style="info" %}
****:open\_file\_folder: **Additional Resources.** Refer to [Data Dictionary: What to Include](reference-and-additional-documents/data-dictionary-what-to-include.md) for further guidance on what to include in the data dictionary.&#x20;
{% endhint %}

### :page\_with\_curl: **** Best practices: field definitions

| **Dos**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | **Donts**                                                                                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| <p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Be precise, unambiguous, and concise.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Include relevant acronyms, but make sure to clearly define them at least once.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> If the value is a date, document the time zone of the recording, e.g. PST (Pacific Daylight Time).</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> If the values are calculated, the source of raw data and calculation method should be included.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Include units of measurement if applicable.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Include any known limitations of the data collected, e.g. groundwater levels were not measured in the month of January.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> If the field is a category, include the list of allowable values, e.g. allowable or expected range.</p> | :x: Avoid writing these definitions from the perspective of an expert; write with the average public user in mind. |



#### Illustrative examples for field name, field label, and data type

| _**Field Name**_    | _**Field Label**_           | _**Data Type**_ |
| ------------------- | --------------------------- | --------------- |
| CalculatedValue     | Calculated Value            | float           |
| Dilution            | Dilution                    | float           |
| PSI                 | Pound-Force per Square Inch | float           |
| Latitude            | Latitude                    | float           |
| WaterBodyType       | Type of Waterbody           | text            |
| BloomLastVerifiedOn | Date Bloom Last Verified    | date            |

#### Illustrative examples for field definitions

{% tabs %}
{% tab title="Example 1" %}
**Field:** Visitor Population

**Description:**&#x20;

<mark style="color:blue;">The number of visitors at Sequoia National Park on a given week\[1]</mark>. <mark style="color:blue;">Since the park is closed on Sundays\[2]</mark>, this includes the number of visitors from the period of Monday through Saturday, PST, <mark style="color:blue;">as reported by the National Park Service\[3]</mark>. The park has a capacity of 10,000 individuals, so the <mark style="color:blue;">allowable range will not exceed 10,000 individuals\[4]</mark>.&#x20;



Comments:&#x20;

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[1]</mark>: Clear and concise description of the field.

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[2]</mark>: Lists limitations of dataset.&#x20;

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[3]</mark>: Specifies data source.

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[4]</mark>: Lists possible range of data.&#x20;
{% endtab %}

{% tab title="Example 2" %}
**Field:** Bus Route Code\
**Description:**&#x20;

The code for <mark style="color:red;">BBB\[1]</mark> routes throughout Los Angeles. <mark style="color:blue;">The possible BBB routes includes: 1, Main St & Santa Monica Blvd; 5, Olympic Blvd; 10, Downtown LA Freeway Express; 41, SMC - 17th St Station - Montana Ave; 43, San Vicente Blvd & 26th St\[2]</mark>.&#x20;



**Comments:**&#x20;

<mark style="color:red;"></mark>:x:<mark style="color:red;">\[1]</mark>: Uses an uncommon acronym without defining it. Alternatively, define the acronym as "Big Blue Bus (BBB)".&#x20;

<mark style="color:blue;"></mark>:white\_check\_mark:<mark style="color:blue;">\[2]</mark>: Lists allowable values. &#x20;
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Stuck on best practices, need advice?**

Send a message on the [CalData Communities Open Data Channel](https://teams.microsoft.com/l/channel/19%3a037b34f454d94a9fa7f6aa964c052af4%40thread.tacv2/Open%20Data?groupId=0f45987a-e632-4e93-be66-ebfd6079e926\&tenantId=68a88534-151d-4e79-8046-09be7890656c). If you need access, [sign up here](https://forms.office.com/Pages/ResponsePage.aspx?id=NIWoaB0VeU6ARgm-eJBlbP8EsQ790KZKrhPJ1tkPH1JURjFWN1paMUtURFU5TFZOSjdTNVFZMkxEQi4u).
{% endhint %}

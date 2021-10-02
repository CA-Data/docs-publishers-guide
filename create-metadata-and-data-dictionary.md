# 3. Create Metadata and Data Dictionary

Metadata is information about a dataset that makes the data easy to find or identify. Metadata describes the dataset’s structure, data elements, its creation, access, format, and content.

Metadata is necessary to improve the discoverability of data within the open data portal and on external search engines. The more relevant information the search engine has about your data resources, the easier it will be for it to point to your resource when users search. Metadata is what helps a user narrow down thousands of data resources to just a few that will likely provide the data they need to answer their question. 

**Without good metadata, datasets are prone to getting lost.** Below we define minimum standards and best practices for creating good metadata.

## Create your metadata

{% hint style="info" %}
\*\*\*\*📂 **Additional Resources:** [Download the metadata template](https://docs.google.com/spreadsheets/u/0/d/1CHJuE89yiNUHsxrjQxseMmxRWDAs11M4/edit) to fill in the required information. 
{% endhint %}

**General checklist:** 

1. [ ] Fill in the metadata fields relevant to your dataset - [see metadata field definition reference](reference-and-additional-documents/metadata-field-definitions.md)
2. [ ] Make sure your dataset title is accessible and descriptive  
3. [ ] Ensure your dataset description is user friendly

{% hint style="info" %}
\*\*\*\*📂 **Additional** **Resources:** Refer to [this list](reference-and-additional-documents/metadata-field-definitions.md) for definitions of and further guidance on metadata fields. 
{% endhint %}

### \*\*\*\*📃 **Best practices: Dataset title content**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Do&apos;s</b>
      </th>
      <th style="text-align:left"><b>Dont&apos;s</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#x2705; Keep titles concise and informative.</td>
      <td style="text-align:left">
        <p>&#x274C; Avoid using CA, California in the title if it does not meaningfully
          clarify the scope.</p>
        <p></p>
        <p>&#x274C; Avoid using jargon and spell out acronyms.</p>
      </td>
    </tr>
  </tbody>
</table>

#### **Illustrative example 1:** 

![](.gitbook/assets/screenshot-2021-09-24-at-7.32.38-pm.png)

**Illustrative example 2:**

![](.gitbook/assets/screenshot-2021-09-24-at-7.34.23-pm.png)

### 

### \*\*\*\*📃 **Best practices: Dataset description content**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Do&apos;s</b>
      </th>
      <th style="text-align:left"><b>Dont&apos;s</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>&#x2705; Create a summary paragraph that details the contents of your
          data table. The first few sentences are the most important.</p>
        <p></p>
        <p>&#x2705; Address the following points, if applicable:</p>
        <ul>
          <li>Data source</li>
          <li>Data collection method</li>
          <li>Purpose of dataset
            <ul>
              <li>Include relevant ordinance references, if applicable</li>
            </ul>
          </li>
          <li>Programs or policies this data supports</li>
        </ul>
        <p>&#x2705; Include related legislation info if applicable.</p>
        <p></p>
        <p>&#x2705; Include relevant acronyms, but make sure to clearly define them
          at least once.</p>
      </td>
      <td style="text-align:left">&#x274C; Avoid using acronyms in your first few sentences.</td>
    </tr>
  </tbody>
</table>

**Illustrative example 1:** 

![](.gitbook/assets/screenshot-2021-09-24-at-7.58.00-pm.png)

**Illustrative example 2:** 

![](.gitbook/assets/screenshot-2021-09-24-at-7.58.17-pm.png)

## Create your data dictionary

A data dictionary is the information you provide that tells a user exactly what is in your data resource and how it can be used. A data dictionary is what helps the user decide if your data resource will provide the data that is needed to answer their question, and also if it is in a form they can use.

**General checklist:** 

* [ ] For each field, document the name, title, data type, definition and valid values if applicable 
* [ ] Write field definitions in user friendly language

{% hint style="info" %}
\*\*\*\*📂 **Additional Resources:** Refer to [this list](reference-and-additional-documents/data-dictionary-what-to-include.md) for further guidance on what to include in the data dictionary. 
{% endhint %}

### 📃 ****Best practices: Field definitions

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Dos</b>
      </th>
      <th style="text-align:left"><b>Donts</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>&#x2705; Be precise, unambiguous, and concise.</p>
        <p></p>
        <p>&#x2705; Include relevant acronyms, but make sure to clearly define them
          at least once.</p>
        <p></p>
        <p>&#x2705; If the value is a date, document the time zone of the recording,
          e.g. PST (Pacific Daylight Time).</p>
        <p></p>
        <p>&#x2705; If the values are calculated, the source of raw data and calculation
          method should be included.</p>
        <p></p>
        <p>&#x2705; Include units of measurement if applicable.</p>
        <p></p>
        <p>&#x2705; Include any known limitations of the data collected, e.g. groundwater
          levels were not measured in the month of January.</p>
        <p></p>
        <p>&#x2705; If the field is a category, include the list of allowable values,
          e.g. allowable or expected range.</p>
      </td>
      <td style="text-align:left">&#x274C; Avoid writing these definitions from the perspective of an expert;
        write with the average public user in mind.</td>
    </tr>
  </tbody>
</table>



#### Illustrative examples for field name, field title and data type

| _**Field Name**_ | _**Field Title**_ | _**Data Type**_ |
| :--- | :--- | :--- |
| CalculatedValue | Calculation Value | float |
| Dilution | Dilution | float |
| PSI | Pound-Force per Square Inch | float |
| Latitude | Latitude | float |
| **WaterBodyType** | Type of Waterbody | text |
| BloomLastVerifiedOn | Bloom Last Verified on | date |

#### 

#### Illustrative examples for field definitions

![](.gitbook/assets/18.png)

![](.gitbook/assets/19.png)

{% hint style="info" %}
\*\*\*\*📂 **Additional Resources:** 

* [Metadata template](https://docs.google.com/spreadsheets/u/0/d/1CHJuE89yiNUHsxrjQxseMmxRWDAs11M4/edit)
{% endhint %}


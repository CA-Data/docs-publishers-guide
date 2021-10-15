# Simplify and Clean Data: Detailed Checklist

**Return to: **

{% content-ref url="../2.-prepare-data.md" %}
[2.-prepare-data.md](../2.-prepare-data.md)
{% endcontent-ref %}

## De-identify data if necessary

* [ ] Does the source data include personally identifiable information (PII) or personal health information (PHI)?
  * [ ] **Yes** - implement de-identification techniques per the guidance received during the [pre-publishing checklist](../review-the-pre-publishing-checklist.md)****
  * [ ] **No** - if your source data doesn’t have PII or PHI, you do not have to implement de-identification techniques
  * [ ] **Unsure** - consult your data coordinator and relevant privacy and legal contacts in your organization if you are unsure

## Determine data format and quality check the dataset

*   [ ] **Determine how to normalize and simplify the dataset beforehand.** Use the target data format you defined in [1. Pre-publishing checklist](../review-the-pre-publishing-checklist.md)

    * **Note:** If you’ve merged your data from multiple datasets in step [2. Consolidate and merge raw data](broken-reference), you’ve already had to normalize data to a single output format. You can take a little time here to assess if there are any further schema simplifications you can do.


* [ ] Check the usability, understandability, and quality of the dataset
  *   [ ] Ensure human readable data. Plain language should be used in naming datasets and the elements in them as far as possible.

      * [ ] Simplify any jargon or acronyms that are being used as header names in the dataset. If a field name cannot be simplified, ensure that all jargon is explained clearly in documentation, with appropriate references provided
      * [ ] If possible, provide a field that maps codes or acronyms within rows to a definition of those stored as an additional column
      * [ ] At minimum provide a list of definitions for codes and acronyms in your documentation


*   [ ] Identify fields where there are rows with no values

    * [ ] **Do the blank fields mean something other than missing or no value?** Consider mapping these on to a value (e.g. Not Applicable, -1, etc) or at least documenting that blank is intentional (e.g. no value selected in an optional field)
    * [ ] **Do the blank fields really indicate no value or are they missing for some other reason (data quality)?** Document any important factors about missing values to encourage appropriate use and interpretation of the data


* [ ] Identify fields where ranges are important (numeric scales, dates, etc.)
  *   [ ] **Are the values within allowable ranges?**

      * [ ] If not, let program staff know of any discrepancies and encourage upstream fixes to data sources
      * [ ] If these cannot be cleaned up, note the issues in the documentation to encourage proper use and interpretation of the data


* [ ] Identify fields that are categorical
  * [ ] **Are the categories in the same text cases (upper case, lower case, title case)?** If not, standardize categories to lower case (lower case is more legible to humans when reading)
  *   [ ] **Are the categories consistent?**

      * [ ] Note: you can check this by using GROUP BY or equivalent functions in your tool of choice and sorting alphabetically. This can capture things like mis-spellings or use of different names to mean the same thing
      * [ ] Let program staff know of any discrepancies and encourage upstream fixes to data sources
      * [ ] If you cannot clean up categories for some reason, note the issues in the documentation to encourage proper use and interpretation of the data


* [ ] Ensure your dataset is formatted properly for loading into data.ca.gov and for understandability using the formatting checklist below

## Check dataset for appropriate formatting for use on the open data portal

The final output of your dataset should be a delimited file like a CSV. We know that some datasets are prepared in Excel and have highlighted things to be aware of when formatting the dataset (particularly in the Not Allowed section). If you are working in other tools, some of these won’t be issues for you.

| **Mandatory**                                                                                                                                                                                                                                                                                      | **Not Allowed**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> The dataset has headers for each column (first row/column names) </p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Rows following the headers should be where the data values are</p> | <p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Merged cells</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Multiple tables in a single spreadsheet</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Notes/descriptions (add this information to your metadata)</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Non-data elements </p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Blank rows or columns within the data (an entire row of no values or entire column with no values)</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span> Aggregate (sum of values) rows </p> |

| **Formatting Best Practices**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Dates (i.e. years, or actual dates) should be stored as rows and not just as metadata</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Table should be tall and narrow vs short and wide, 30 columns max is suggested</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2705">✅</span> Identifiers and abbreviations should be changed to full names or values or a separate field should be provided with those definitions</p><p></p> |

## Saving your dataset for publishing on the open data portal

The dataset that you will upload must be in a delimited format with proper text encoding. The means of doing this will vary based on the tools you’re using. For those working in Excel to prepare data, [you can read how to export to a delimited file on Microsoft’s website](https://support.microsoft.com/en-us/office/save-a-workbook-to-text-format-txt-or-csv-3e9a9d6c-70da-4255-aa28-fcacf1f081e6).

* [ ] Ensure that the values are separated by any of the following five delimiters accepted on the California Open Data Portal:
  * Comma: , (most common in the US)
  * Semicolon: ;
  * Pipe: |
  * Plus: +
  * Tabs
* [ ] Ensure that your file is encoded in UTF-8, such that people who download your dataset can properly understand the characters when they download it.
  * Computers encode characters (i.e. “a”, “A”, “3”, “$”) in different formats. Any particular character can be encoded in many different ways, depending on which encoding is used to read or write them.
  * This is the standard encoding for most systems and if you are unsure about the encoding of your file, [email](mailto:opendata@state.ca.gov?subject=Help%20with%20encoding%20formats%20for%20open%20data\&body=I%20need%20help%20making%20sure%20I'm%20properly%20encoding%20my%20file%20in%20UTF-8.%20Note:%20Please%20provide%20additional%20information%20like%20the%20application%20you're%20using%20to%20prepare%20the%20data%20to%20assist%20the%20team%20in%20helping%20you.) [the California Department of Technology’s Open Data Team](mailto:opendata@state.ca.gov?subject=Help%20with%20encoding%20formats%20for%20open%20data\&body=I%20need%20help%20making%20sure%20I'm%20properly%20encoding%20my%20file%20in%20UTF-8.%20Note:%20Please%20provide%20additional%20information%20like%20the%20application%20you're%20using%20to%20prepare%20the%20data%20to%20assist%20the%20team%20in%20helping%20you.).

{% hint style="info" %}
****:file_folder: **Additional Resources: **

* [What is UTF-8?](https://www.twilio.com/docs/glossary/what-utf-8) from Twilio developer docs
* [Data.gov.sg Data Quality Guide for Tabular Data](https://github.com/datagovsg/data-quality) by Singapore’s open data program
{% endhint %}

****

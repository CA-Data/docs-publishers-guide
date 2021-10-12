# Consolidate and Merge Raw Data

Consolidating data refers to the gathering of existing datasets from multiple sources. It is important to ensure that each variable is processed and documented in the same way across these datasets. This makes it easier for users to understand the consolidated data and for the data producers to create a consistent dataset.

{% hint style="warning" %}
**Decision point: **

Do you have multiple sources (spreadsheets, database tables, etc.) that you need to consolidate into a single dataset? 

**If yes**, this section gives a generalizable checklist to consider when merging data. You may need to consult with other staff in your department on specific technical implementations of a repeatable process. 

**If no**, go ahead and skip to 3. Simplify and clean data. 
{% endhint %}

## Prepare for merging data

*   [ ] Identify how many rows you have across sources

    * **Note:** if you’re working in Excel, there are limits to how many rows you can have; make sure you don’t inadvertently drop records when merging sources (1,048,576 rows for modern versions of Excel, [read Microsoft documentation on Excel limitations](https://support.microsoft.com/en-us/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3))


*   [ ] Analyze the fields for each source and map on to your target data output

    * [ ] **Are there fields with different names that are actually the same thing?** Map those on to a common field name for your target output dataset
    * [ ] **Are there fields in some sources that aren’t in others?** Make note of those and include in the dataset documentation to clearly highlight data gaps


* [ ] Does the source data include personally identifiable information (PII) or personal health information (PHI)?
  * [ ] **Yes** - implement de-identification techniques per the guidance received during the [pre-publishing checklist](review-the-pre-publishing-checklist.md)****
  * [ ] **No** - if your source data doesn’t have PII or PHI, you do not have to implement de-identification techniques
  * [ ] **Unsure** - consult your data coordinator and relevant privacy and legal contacts in your organization if you are unsure

## Quality check merged data output

*   [ ] Merge data and check the resulting merge of datasets

    * [ ] **Note:** we are not prescriptive about how you merge data as that varies by tool. Please consult documentation or peers for specific technical questions for merging data. Regardless of approach, adopt one that is repeatable by you and others.



    * [ ] **Does the number of rows in your merged dataset match the number of rows across sources?** If not, check to see if anything was dropped as a result of your merge logic.



    *   [ ] Identify numeric** **fields** **that are meant to be calculated

        * [ ] **Do the sums of these fields in the merged dataset match the sum of values across the individual sources?** If not, check to see if anything was dropped as a result of your merge logic.


    *   [ ] Identify fields where there are rows with no values

        * [ ] **Are the fields blank in the source data as well? **If not, check to see if anything was dropped as a result of your merge logic.


    *   [ ] **Check demographic or population fields to make sure the dataset is inclusive of the full population represented across datasets. **For example, make sure all states/cities/counties or all race/ethnicity categories are included.

        * Note any missing sub-populations in your documentation if there is no way to address them. This is to encourage proper use and interpretation of the data.


    * [ ] Identify fields that are categorical
      *   [ ] **Are the categories consistent across sources? **

          * **Note:** you can check this by using GROUP BY or equivalent functions in your tool of choice and sorting alphabetically. This can capture things like mis-spellings or use of different names to mean the same thing
          * Let program staff know of any discrepancies and encourage upstream fixes to data sources
          * If you cannot clean up categories for some reason, note the issues in the documentation to encourage proper use and interpretation of the data

          ****
    * [ ] Follow the [checklist in step 3. Simplify and clean data](simplify-and-clean-data.md) to perform additional checks for the usability, understandability, and quality of the dataset



{% hint style="info" %}
**Additional Resources:** 

* [Guide to Bullet-proofing data](https://github.com/propublica/guides/blob/master/data-bulletproofing.md) by Jennifer LaFleur, ProPublica
* [Data Quality Testing: Ways to Test Data Validity and Accuracy](https://lakefs.io/data-quality-testing/) by Einat Orr, PhD., LakeFS
{% endhint %}

# Data Dictionary: What to Include

For each variable, a Data Dictionary lists:

* [ ] **Field Name.** The name of the field as it's written in the source data table. It’s okay for these to be shorter, and you often won’t have complete control over these. The field title is where you can write something more descriptive that will be a reference for users.
* [ ] **Field Title**. The common English title for the data contained in this column. Avoid using abbreviations here.
* [ ] **Data Type.** Can be one of the following
  * **Note:** these data types are the ones supported by data.ca.gov which is a CKAN portal. These are the ones you choose when initially uploading your dataset. Choosing the right format makes it easier for data users to use the dataset.
  * **text.** An arbitrary series of alphanumeric characters
  * **json**. Nested json data e.g. {"foo": 42, "bar": \[1, 2, 3\]}.
  * **date**. Date without time stored in an ISO8601:extended format e.g. 2015-05-25
  * **time**. Time without a date in 24 hour format e.g. 15:00:05
  * **timestamp**. Date and time stored in an ISO8601:extended format e.g. 2015-05-25T15:00:05
  * **int**. An integer number \(no decimals\)
    * Only use it if this field is meant to be used in a calculation. Otherwise use “text”.
  * **float**. A floating point number \(with decimals\)
    * Only use if this field is meant to be used in a calculation. Otherwise use “text”.
  * **bool**. A true/false \(boolean\) value; valid formats: true/false, 1/0, on/off
* [ ] **Field Definition.** Full description of what information is included for the field.
* [ ] **Valid Values.** \(if applicable\) Indicate what the expected set of valid values is for the field. This could be a list of controlled values, a range \(for numbers and dates\), or a minimum or maximum value \(for numbers and dates\).


# Column Headers and Order

## Column Headers

* Only use alphanumeric or these 3 special characters: period (.), dash (-), and underscore (\_)
  * Ampersand (&) should be replaced by “and” if needed
* Each header must be unique
  * e.g. can’t have two headers called "duration"
* Units of measure should be omitted
  * Units can and must be provided with the data dictionary
* Keep short (less than 30 characters)
  * A full description can and must be provided with the data dictionary

## Column Order <a href="#column-order" id="column-order"></a>

* _Unique identifiers_ should be in the left-most column if applicable
* _Date and time variables_ should be in the first column for time series data
* _Fixed or classified variables_ should be ordered with the highest-level variable on the left and most granular variable on the right, for example
* _Observed variables_ should always be on the rightmost columns, these are measured variables often numeric, the following are some example field names that could be observed variables:
  * Duration
  * Number of Units
  * Number of Stories
  * Year Built
  * People Served

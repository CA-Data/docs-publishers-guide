# Date and Time

* [Based on ISO8601](https://en.wikipedia.org/wiki/ISO\_8601), an international standard for representing date and time. We chose the "extended format" with the hyphens because it is more human readable.
  * Compare 2016-01-01 to 20160101
* All date and time variables must be local time (UTC -8hrs Pacific Standard Time UTC -7hrs Pacific Daylight Savings Time) unless specified.
  * Use the data dictionary to specify any important information about time encoding

## Date variables

| Interval    | Column name | Format      | Range of values      | Example    |
| ----------- | ----------- | ----------- | -------------------- | ---------- |
| Annual      | `year`      | YYYY        | YYYY: any valid year | 2022       |
| Monthly     | `month`     | YYYY-MM     | MM: 01 to 12         | 2022-01    |
| Daily       | `date`      | YYYY-MM-DD  | DD: 01 to 31         | 2022-01-01 |
| Weekly      | `week`      | YYYY-\[W]WW | \[W]WW: W01 to W52   | 2022-W01   |
| Quarterly   | `quarter`   | YYYY-\[Q]Q  | \[Q]Q: Q1 to Q4      | 2022-Q1    |
| Half-yearly | `half_year` | YYYY-\[H]H  | \[H]H: H1 or H2      | 2022-H1    |

**For fiscal periods, prefix "fiscal\_" to column name**

| Interval            | Column name        | Format     | Example |
| ------------------- | ------------------ | ---------- | ------- |
| Fiscal, annual      | `fiscal_year`      | YYYY       | 2015    |
| Fiscal, monthly     | `fiscal_month`     | YYYY-MM    | 2015-01 |
| Fiscal, quarterly   | `fiscal_quarter`   | YYYY-\[Q]Q | 2015-Q1 |
| Fiscal, half-yearly | `fiscal_half_year` | YYYY-\[H]H | 2015-H1 |

* Fiscal year start date must be indicated in the data dictionary
  * e.g. The fiscal year starts on July 1 and ends on June 30 for the State of California

## Date-time and time variables

* ISO 8601 uses 24 hour clock system in hh:mm:ss format sometimes referred to as military time (do not use AM or PM)
  * e.g. 13:00 is equivalent to 1:00 PM

| Type        | Column name | Format                      | Example             |
| ----------- | ----------- | --------------------------- | ------------------- |
| Date + time | `date_time` | YYYY-MM-DD\[T]hh:mm         | 2015-01-01T13:00    |
|             |             | _or_ YYYY-MM-DD\[T]hh:mm:ss | 2015-01-01T13:00:00 |
| Time only   | `time`      | hh:mm                       | 13:00               |
|             |             | _or_ hh:mm:ss               | 13:00:00            |

**Specify the timezone if it is not local time (UTC -8hrs Pacific Standard Time UTC -7hrs Pacific Daylight Savings Time):**

| Type        | Column name | Format                               | Example                      |
| ----------- | ----------- | ------------------------------------ | ---------------------------- |
| Date + time | `date_time` | YYYY-MM-DD\[T]hh:mm+hh:mm            | 2015-01-01T12:00+00:00       |
|             |             | _or_ YYYY-MM-DD\[T]hh:mm:ss+hh:mm:ss | 2015-01-01T12:00:00+00:00:00 |

## Date and time extracts

In certain cases you may want to provide a single variable representing the number or name of an individual date component, a day, a month, etc. There's no requirement to provide these, but follow this guidance:

| Extract          | Column name | Type    | Range of values                                                                                  |
| ---------------- | ----------- | ------- | ------------------------------------------------------------------------------------------------ |
| Year             | year\_num   | integer | any valid year                                                                                   |
| Month            | month\_num  | integer | 1 to 12                                                                                          |
| Month Name       | month\_name | string  | January, February, March, April, May, June, July, August, September, October, November, December |
| Week of Year     | woy\_num    | integer | 1 to 52                                                                                          |
| Day              | day\_num    | integer | 1 to 31 (varies by month)                                                                        |
| Day of Week      | dow\_num    | integer | 1 to 7                                                                                           |
| Day of Week Name | dow\_name   | string  | Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday                                   |
| Hour             | hour\_num   | integer | 1 to 24                                                                                          |
| Minute           | minute\_num | integer | 1 to 60                                                                                          |
| Second           | second\_num | integer | 1 to 60                                                                                          |

## Durations

Durations can be automatically calculated if you provide a separate start and end period in your dataset. If you also want to provide a duration, please:

* Provide the milliseconds between the start and end period (include the duration unit in the data dictionary)
  * Milliseconds can be rolled up to other time intervals
* Use duration in your column name but prepend with a useful descriptor, e.g:
  * flight\_duration
  * response\_duration
  * dwell\_time\_duration
  * travel\_duration
* Do not duplicate any of the duration column names per the [guidance on columns](column-headers-and-order.md)

{% hint style="info" %}
**Note:** ISO 8601 does have separate guidance on duration formatting, but we find this more cumbersome than just calculating milliseconds between a period for which there are many standard programming libraries.
{% endhint %}

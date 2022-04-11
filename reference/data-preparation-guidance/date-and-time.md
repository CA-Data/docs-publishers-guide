# Date and Time

* Based on ISO8601, an international standard for representing date and time. We chose the "extended format" with the hyphens because it is more human readable.
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

|   |   |   |   |
| - | - | - | - |
|   |   |   |   |
|   |   |   |   |
|   |   |   |   |

* Fiscal year start date must be indicated in the data dictionary
  * e.g. The fiscal year starts on July 1 and ends on June 30 for the State of California

## Date-time and time variables

* ISO 8601 uses 24 hour clock system in hh:mm:ss format (do not use AM or PM)
  * e.g. 13:00 is equivalent to 1:00 PM

|   |   |   |   |
| - | - | - | - |
|   |   |   |   |
|   |   |   |   |
|   |   |   |   |

**Specify the timezone if it is not local time (UTC -8hrs Pacific Standard Time UTC -7hrs Pacific Daylight Savings Time):**

|   |   |   |   |
| - | - | - | - |
|   |   |   |   |
|   |   |   |   |
|   |   |   |   |

## Date and time extracts

In certain cases you may want to provide a single variable representing the number or name of an individual date component, a day, a month, etc. There's no requirement to provide these, but follow this guidance:

|   |   |   |   |
| - | - | - | - |
|   |   |   |   |
|   |   |   |   |
|   |   |   |   |

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

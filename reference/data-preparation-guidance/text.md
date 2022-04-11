# Text

* UTF-8 encoding should be used
  * This ensures that special characters can be decoded by users
* No line breaks within cells
  * This can break parsing in software like Excel, introducing data integrity issues
  * There are many ways to remove and detect line breaks, but this can vary based on how you're extracting data

## Character case

Text should be presented in the easiest to interpret/read format where appropriate.

**Title case**

* Address String
* Categories when either the source system presents them this way or it is easy to interpret from the source consistently

**Upper case**

* Acronyms - e.g - PSA (Park Service Area)
* States - e.g. CA

**Lower case**

* Categories when the source system presents them in caps and there's no way to interpret them to title case
* [Research suggests lower case as opposed to uppercase is easier to read ](https://www.microsoft.com/typography/ctfonts/wordrecognition.aspx)for humans and just as useful to machines, note exceptions above

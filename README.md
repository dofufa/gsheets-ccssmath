# gsheets-ccssmath
Google Sheets custom functions for CCSS math items

# INSTALL
  + Open Google Sheets.
  + From the Extensions menu, select Apps Script.
  + Copy and paste `Code.gs` in releases into Apps Script.

# Function list

## `=CCSSMATHBYKEY(itemkey)`
Returns standards details using the required parameter `key`, a **valid CCSS Math key/code as defined by the [CCSS Math Standards][ccssm].**

> **NOTE:** Queries like `K . CC . A` are often padded by spaces because Google Sheets automatically converts values that look like URLs to hypertext. There is no option available to turn off the auto-hyperlink feature at this time.

  + Accepts text or array input.
  + EXAMPLE: `=CCSSMATHBYKEY("K . CC . A")`
  + EXAMPLE: `=CCSSMATHBYKEY("5.NF.A.1")`
  + EXAMPLE: `=CCSSMATHBYKEY(A1)`
  + EXAMPLE: `=CCSSMATHBYKEY(A1:A22)`  

## `=CCSSMATHBYID(itemid)`
Returns standards details using the required parameter `itemid`, a [valid CCSS Math Item ID][itemid].

+ Accepts text or array input.
  + EXAMPLE: `=CCSSMATHBYID(35)`
  + EXAMPLE: `=CCSSMATHBYID(42)`
  + EXAMPLE: `=CCSSMATHBYID(A1)`
  + EXAMPLE: `=CCSSMATHBYID(A1:A22)`  
  
## `=CCSSMATH(search_for, [ as_two_columns ])`
Returns standards keys and details for the required parameter `search_for`, if results found. Returns the results as two separate columns if the optional parameter `as_two_columns` is set to TRUE.

## Returning one column (1d array)
  + Accepts text input. Returns an array.
  + EXAMPLE: `=CCSSMATH("geometry")`
  + EXAMPLE: `=CCSSMATH(A1)`

 ## Returning two columns (2d array)
  + Accepts text input and a boolean. Returns an array.
  + EXAMPLE: `=CCSSMATH("function inverse", true)`
  + EXAMPLE: `=CCSSMATH(A1, true)`     

# Licenses
  + MIT



[ccssm]: http://www.corestandards.org/Math/
[itemid]: https://github.com/ccssapp/ccssmath-items/blob/main/ITEMID.md

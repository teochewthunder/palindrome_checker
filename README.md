# Palindrome Checker

## HTML
### `pnlString`
- Container for textbox `txtString`: calls `checkPalindrome()` on input.

### `pnlOptions`
- Container for checkbox `cbIgnoreCase`: used by user to determine if casing should be ignored; calls `checkPalindrome()` on click.

### `pnlOutput`
- Container for `pnlResult`: placeholder for sanitized input.
- Container for `pnlVerification`: placeholder for instructions or success/failure messages.

## Functions
`checkPalindrome()`:
- set temp variable.
- remove non-alphanumeric characters.
- check if `cbIgnoreCase` is checked. If so, convert temp variable to lowercase.
- set Result's HTML content to temp variable. (call to `setResult()`)
- if temp variable has less than 1 character, set message. (call to `setVerification()`)
- otherwise, check if is palindrome. (call to `isPalindrome()`)
  - if `true`, set message. (call to `setVerification()`)
  - if `false`, set message. (call to `setVerification()`)
- if temp variable has 0 characters, set message. (call to `setVerification()`)
 

`isPalindrome(str)`:
- set temp variable of `str` converted to array, reversed, then joined.
- compare if temp variable is same as `str`.

`setResult(str)`:
- set `pnlResult` HTML content to `str`.

`setVerification(str, colorCode)`:
- `colorCode` default value "default"
- set `pnlVerification` HTML content to `str`.
- set `pnlVerification` color to value determined by `colorCode`.

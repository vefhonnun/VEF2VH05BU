# Telephone Input Regex

**HTML5 `input` with `type="tel"`** uses the `pattern` attribute to apply **regular expressions (regex)** for validating telephone number formats.

- The `pattern` attribute accepts a **JavaScript regular expression** that the input value must match.
- Example for a US-style 10-digit number (e.g., `123-456-7890`):
  ```html
  <input type="tel" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" required>
  ```
- To allow optional dashes, use `?` to make the hyphen optional:
  ```html
  <input type="tel" pattern="[0-9]{3}-?[0-9]{3}-?[0-9]{4}" required>
  ```
- For international numbers (e.g., `+1-123-456-7890`), include `+` and allow 9–12 digits:
  ```html
  <input type="tel" pattern="^\+?[0-9]{9,12}$" required>
  ```
- Use the `title` attribute to provide a user-friendly error message:
  ```html
  <input type="tel" pattern="[0-9]{3}-?[0-9]{3}-?[0-9]{4}" title="Enter a valid 10-digit phone number" required>
  ```

> **Note**: `type="tel"` does not validate format by default—**regex in `pattern` is required**. Client-side validation can be bypassed; always validate on the server.
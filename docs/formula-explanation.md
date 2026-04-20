# Formula Explanation

## Observed Workbook Logic

The workbook generates Office 365-ready account data from structured user input.

### Main Functional Behavior
- First name and last name are entered in the input sheet
- A domain is selected from a controlled list
- The result sheet generates:
  - a normalized username
  - a formatted export string
  - CSV-ready output for provisioning

---

## Username Generation Logic

The username creation flow can be summarized as follows:

1. Read **first name**
2. Read **last name**
3. Convert text to lowercase
4. Replace German umlauts:
   - `ä` → `ae`
   - `ö` → `oe`
   - `ü` → `ue`
5. Combine values into:
   - `firstname.lastname@domain`

### Example

Input:
- First name: `Jörg`
- Last name: `Müller`
- Domain: `example.org`

Output:
- `joerg.mueller@example.org`

---

## Why This Matters

This logic helps to:

- standardize account naming
- reduce repetitive manual formatting
- lower the risk of inconsistent user creation
- support structured bulk provisioning workflows

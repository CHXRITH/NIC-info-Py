# NIC Number Parser 🇱🇰

Welcome to the NIC Number Parser! This Python script helps you extract valuable information from Sri Lankan National Identity Card (NIC) numbers, including gender and birth date.


## Features

- **Input Validation:** Ensures the NIC number is of the correct length and format.
- **Gender Detection:** Identifies the gender associated with the NIC number.
- **Birth Date Calculation:** Determines the birth month and day based on the NIC number.

## How to Use

1. Run the script.
2. Enter a valid NIC number when prompted.
3. Get instant details about the gender and birth date associated with the NIC number.

## Example

```python
# Example usage:
nic_number = input("Enter NIC number: ")
error, gender, bday = parse_nic(nic_number)

if error:
    print("Error:", error)
else:
    print("Gender:", gender)
    print("Birth Date:", bday)
```
<br>

> 👾 HAPPY CODING !!

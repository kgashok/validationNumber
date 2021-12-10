### Valid Account Number
  
Use Modulo Formula Method (Mod 10) for validating Account numbers
 
It has the following steps: 
 
**Step 1**: Double the value of alternate digits of the Account number beginning with the second digit from the right (the rightmost digit is the check digit.)
 
**Step 2**: Add the individual digits comprising the products obtained in Step 1 to each of the unaffected digits in the original number.
 
**Step 3**: The total obtained in Step 2 must be a number
ending in zero (30, 40, 50, etc.) for the account number 
to be validated. The Total mod 10 must be 0.

Write a function `validate` which will accept a number as argument and return 
  
    VALID         # if valid account number   
    INVALID 3     # if invalid, and correct check digit 

## Example 
 
For example, to validate the  account number `79927398713`:

Step 1:	Account number      7 	`9	9	2	7	3	9	8	7	1	3`	  
Step 2: Double every other	7 `18	9	4	7	6	9	16	7	2	3`
  
7 +(1+8) + 9 + (4) + 7 + (6) + 9 +(1+6) + 7 + (2) + 3 
 
Step 3: Sum = 70 : Account number is valid because the 
`70 % 10` yields no remainder. 

## Example 2

For the account number, `513467882134`, 

- The digits to be doubled and then summed are: 
    `[5, 3, 6, 8, 2, 3]`

- The digits that are to summed: 
    `[1, 4, 7, 8, 1]`

- The original check_digit is `4` 

The total comes to `48` without the check_digit. To make it a valid account number, the `correct` check_digit is 2 (`50 - 48 = 2`). 

Therefore, return `"INVALID 2"`


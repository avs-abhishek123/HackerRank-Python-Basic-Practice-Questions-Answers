# Write a function
_We add a Leap Day on February 29, almost every four years. The leap day is an extra, or intercalary day and we add it to the shortest month of the year, February. In the Gregorian calendar three criteria must be taken into account to identify leap years:_ <br />

- The year can be evenly divided by 4, is a leap year, unless: <br />
  - The year can be evenly divided by 100, it is NOT a leap year, unless:
  - The year is also evenly divisible by 400. Then it is a leap year.<br />
<br />
This means that in the Gregorian calendar, the years 2000 and 2400 are leap years, while 1800, 1900,
2100, 2200, 2300 and 2500 are NOT leap years. <br />
<br />
* Task <br />
<br />
You are given the year, and you have to write a function to check if the year is leap or not.
Note that you have to complete the function and remaining code is given as template.

## Input Format<br />
Read y, the year that needs to be checked.<br />
### Constraints: <br /> 
1900<=y<=10000<br />
## Output Format<br />
Output is taken care of by the template. Your function must return a boolean value (True/False)<br />
### Sample Input 0<br />
1990<br />
### Sample Output 0<br />
False<br />
### Explanation 0<br />
1990 is not a multiple of 4 hence it's not a leap year.<br />
<br />

# ANSWER: <br />
<br />
def is_leap(year):<br />
    leap = False
    
    # Write your logic here
    if year%4==0 :
        if year%100==0:
            leap = False
        elif year%400==0:
            leap = True

    return leap

year = int(input()) <br />
print(is_leap(year))

# Collections.namedtuple()

_Basically, namedtuples are easy to create, lightweight object types.They turn tuples into convenient containers for simple tasks.With namedtuples, you don’t have to use integer indices for accessing members of a tuple._ <br />

Example<br />
> from collections import namedtuple<br />
> Point = namedtuple('Point','x,y')<br />
> pt1 = Point(1,2)<br />
> pt2 = Point(3,4)<br />
> dot_product = ( pt1.x * pt2.x ) +( pt1.y * pt2.y )<br />
> print dot_product<br />
<br />
11<br />
<br />

> from collections import namedtuple <br />
> Car = namedtuple('Car','Price Mileage Colour Class')<br />
> xyz = Car(Price = 100000, Mileage = 30, Colour = 'Cyan', Class = 'Y') <br />
> print xyz <br />
> Car(Price=100000, Mileage=30, Colour='Cyan', Class='Y') <br />
> print xyz.Class <br />

<br />
Y<br />
<br />

## Task<br />

<br />
Dr. John Wesley has a spreadsheet containing a list of student's , , and .<br />
Your task is to help Dr. Wesley calculate the average marks of the students.<br />
<br />

## Input Format<br />
The first line contains an integer , the total number of students.<br />
The second line contains the names of the columns in any order.<br />
The next lines contains the , , and , under their respective column names.<br />
## Output Format<br />
Output is taken care of by the template. Your function must return a boolean value (True/False)<br />
### Sample Input 0<br />
5<br />
ID MARKS NAME CLASS<br />
1 97 Raymond 7<br />
2 50 Steven 4<br />
3 91 Adrian 9<br />
4 72 Stewart 5<br />
5 80 Peter 6<br />
<br />
5<br />
MARKS CLASS NAME ID
92 2 Calum 1<br />
82 5 Scott 2<br />
94 2 Jason 3<br />
55 8 Glenn 4<br />
82 2 Fergus 5<br />
### Sample Output 0<br />
78.00<br />
81.00<br />
### Explanation 0<br />
Average =<br />
Can you solve this challenge in 4 lines of code or less ?<br />
NOTE: There is no penalty for solutions that are correct but have more than 4 lines.<br />
<br />
### Constraints<br />
### Output Format<br />
<br />
Print the average marks of the list corrected to 2 decimal places.<br />
collections.namedtuple()<br />
<br />
Code 01<br />
Code 02<br />
### Note: <br /

1. Columns can be in any order. IDs, marks, class and name can be written in any order in the spreadsheet.<br />
2. Column names are ID , MARKS , CLASS and NAME . (The spelling and case type of these names won't change.)<br />

<br />

# ANSWER: <br />
<br />
from collections import namedtuple <br />

(n, categories) = (int(input()), input().split())

Grade = namedtuple('Grade', categories)

marks = [int(Grade._make(input().split()).MARKS) for _ in range(n)]

print((sum(marks) / len(marks)))

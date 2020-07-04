


# Print Function
_Read an integer. Without using any string methods, try to print the following:Note that " " represents the values in between._ <br />

## Input Format<br />
The first line contains an integer .
<br />
### Constraints: <br /> 
1900<=y<=10000<br />
## Output Format<br />
Output the answer as explained in the task.
<br />
### Sample Input 0<br />
3<br />
### Sample Output 0<br />
123<br />


# ANSWER: <br />
<br />
   
   if __name__ == '__main__': <br />
    <br />n = int(input()) <br />
    <br />print(*range(1, n+1), sep='')<br />

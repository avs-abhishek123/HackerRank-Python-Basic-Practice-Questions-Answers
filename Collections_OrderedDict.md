# Collections.OrderedDict()
An OrderedDict is a dictionary that remembers the order of the keys that were inserted first. If a new entry<br />
overwrites an existing entry, the original insertion position is left unchanged.<br />
Example<br />
>>> from collections import OrderedDict<br />
>>> ordinary_dictionary = {}<br />
>>> ordinary_dictionary['a'] = 1<br />
>>> ordinary_dictionary['b'] = 2<br />
>>> ordinary_dictionary['c'] = 3<br />
>>> ordinary_dictionary['d'] = 4<br />
>>> ordinary_dictionary['e'] = 5<br />
<br />
>>> print ordinary_dictionary<br />
{'a': 1, 'c': 3, 'b': 2, 'e': 5, 'd': 4}<br />

<br />
>>> ordered_dictionary = OrderedDict()<br />
>>> ordered_dictionary['a'] = 1<br />
>>> ordered_dictionary['b'] = 2<br />
>>> ordered_dictionary['c'] = 3<br />
>>> ordered_dictionary['d'] = 4<br />
>>> ordered_dictionary['e'] = 5<br />

print ordered_dictionary<br />
OrderedDict([('a', 1), ('b', 2), ('c', 3), ('d', 4), ('e', 5)])<br />
## Task<br />
You are the manager of a supermarket.<br />
You have a list of items together with their prices that consumers bought on a particular day.<br />
Your task is to print each item_name and net_price in order of its first occurrence.<br />
Input Format<br />
The first line contains the number of items, .<br />
The next lines contains the item's name and price, separated by a space.<br />
Constraints<br />
Output Format<br />
Print the item_name and net_price in order of its first occurrence.<br />
Sample Input<br />
9<br />
BANANA FRIES 12<br />
POTATO CHIPS 30<br />
collections.OrderedDict<br /><br />
Code<br />
item_name = Name of the item.<br />
net_price = Quantity of the item sold multiplied by the price of each item.<br />
APPLE JUICE 10<br />
CANDY 5<br />
APPLE JUICE 10<br />
CANDY 5<br />
CANDY 5<br />
CANDY 5<br />
POTATO CHIPS 30<br />
Sample Output<br />
BANANA FRIES 12<br />
POTATO CHIPS 60<br />
APPLE JUICE 20<br />
CANDY 20<br />
Explanation<br />
BANANA FRIES: Quantity bought: , Price:<br />
Net Price :<br />
POTATO CHIPS: Quantity bought: , Price:<br />
Net Price :<br />
APPLE JUICE: Quantity bought: , Price:<br />
Net Price :<br />
CANDY: Quantity bought: , Price:<br />
Net Price :<br />

<br />
<br />

#ANSWERS
<br />
from collections import OrderedDict<br />

d = OrderedDict()<br />

for _ in range(int(input())):<br />

    item, space, quantity = input().rpartition(' ')<br />

    d[item] = d.get(item, 0) + int(quantity)<br />

for item, quantity in d.items():
    print(item, quantity)<br />

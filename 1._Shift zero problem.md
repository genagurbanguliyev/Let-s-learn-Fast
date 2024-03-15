> [! information] function that takes list of integers and it takes each ZERO from that list, and it shift it to the end of the list. So every nonezero integer keeps that the same order, but all zeros get moved to the end of the list

##### lest's a pretty simple idea:
basically iterate through each element of the list, if that element is a zero to remove from the list and append zero to the end of the list:

```python
def func(arr):
	for i in arr:
		if i == 0:
			arr.remove(i)
			arr.append(0)
	return arr

#if we test it:
my_array = [1,2,0,3,0,4,5]
func(my_array)

# result -> [1,2,3,4,5,0,0]
```

it work as we need.
But, if we increase my_array's size, this algorithm takes many time:

# 1
```python
def func(arr):
	for i in arr: # O(n)
		if i == 0:
			arr.remove(i) # O(n)
			arr.append(0)
	return arr

# calculate time:
import random
import time
n = 200000
my_array = [random.randint(0,9) for _ in range(n)]
start = time.time()
result = func(my_array)
stop = time.time()

# it prints how many time it takes (in seconds)
print(stop-start)
```

Total time Complexity: O(n^2)
when we see zero and remove it python has to shift every item that comes after it to fill its place...
that's why removing items from the list gives us the worst case time complexity: O(n)
```
arr.remove(i):
[1,2,0,3,0,4,5]
[1,2,  3,0,4,5]
[1,2,3,  0,4,5]
[1,2,3,0,  4,5]
[1,2,3,0,4,  5]
[1,2,3,0,4,5]

arr.append(0):
[1,2,3,0,4,5,0]
```

***
#### Let's see different approach
```
#create new_list and zero_count
new_list = []
zero_count = 0

my_array = [1,2,0,3,0,4,5]
iterate my_array and each element equals nonezore append it new_list,
and if element is zero zero_count+=1
result:
new_list = [1,2,3,0,4,5]
zero_count = 2

[1,2,3,0,4,5] + 2*[0]
```

# 2
```python
def func(arr):
	new_list = []
	zero_count = 0
	for i in arr: # O(n)
		if i != 0:
			new_list.append(i) # O(1)
		else:
			zero_count+=1
	new_list.extend(zero_count*[0])
	return new_list

# calculate time:
import random
import time
n = 200000
my_array = [random.randint(0,9) for _ in range(n)]
start = time.time()
result = func(my_array)
stop = time.time()

# it prints how many time it takes (in seconds)
print(stop-start)
```

> [!tip] ! Compare two Time complexities 1 and 2
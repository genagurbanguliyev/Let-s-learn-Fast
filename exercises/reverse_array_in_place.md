```python
def reverse(arr)
	# start and end index
	start_index = 0
	end_index = len(arr) - 1
	
	while start_index < end_index:
		# swapping the items
		arr[start_index], arr[end_index] = arr[end_index], arr[start_index]
		start_index += 1
		end_index -= 1

if __name__ == "__main__":
	arr = [2,7,4,10,6]
	reverse(arr)
	print(arr)

```
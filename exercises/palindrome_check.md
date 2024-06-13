```python
def reverse(data):  
    data = list(data)
    start_index = 0  
    end_index = len(data) - 1  
    while start_index < end_index:  
        data[start_index], data[end_index] = data[end_index], data[start_index]
        start_index += 1  
        end_index -= 1  
    return ''.join(data)  
  
def is_palindrome(my_string):  
    if my_string == reverse(my_string):  
        return True  
    return False


if __name__ == '__main__':  
    print(is_palindrome("ala"))
```
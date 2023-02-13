### Palindrome in Python

The `is_palindrome` function checks if a given string is a palindrome or not. A palindrome is a string that reads the same forwards and backwards.


## Get the code.

1. Get the code:

```
git clone https://github.com/wandersonsc/isPalindrome
```

2. Run it! Assuming you have Python setup.

```python
    def is_palindrome(string):
        if not string or len(string) == 1:
            return True

        if string[0] == string[-1]:
            return is_palindrome(string[1:-1])
        return False
```

## How it works

The function uses recursion to shrink the problem space until it's reduced to a base case.

##There are two base cases:

1. If the length of the input string is 0 or 1, it returns True.
2. If the first and last characters of the input string are different, it returns False.


The code `if input[0] == input[-1]:` checks if the first character of the input string is the same as the last character. If they are the same, it's possible that the whole string is a palindrome.

The line `return is_palindrome(input[1:-1])` then calls the `is_palindrome` function again, but with a modified input string. The `[1:-1]` part of the code slices the input string to exclude the first and last characters, effectively shrinking the problem space.

The function will continue to call itself with smaller and smaller input strings until either the length of the string is 0 or 1 (base case 1), or until the first and last characters of the string are different (base case 2).

If the modified string is a palindrome, the function will eventually return `True`. If the string is not a palindrome, the function will eventually return `False`.

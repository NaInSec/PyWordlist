## Wordlist Generator With Python.


```python
import random
import string

def generate_random_char(length, char_set):
    return ''.join(random.choice(char_set) for _ in range(length))

output_file = input("Input Name Output File : ")

wordlist_length = 8
char_set = string.ascii_letters + string.digits + '@$#%&!?{}'

with open(output_file, 'w') as file:
    for _ in range(500):
        password = generate_random_char(wordlist_length, char_set)
        file.write(password + '\n')

print("Wordlist", output_file, "Success...")
```







```







# &#35; string to hex


```python
$ cat str2hex.py
import sys


#strings="/bin/sh"

if len(sys.argv) != 2:
    print("Usage : " + sys.argv[0] + " string" )
    sys.exit(-1)

strings = sys.argv[1]

print(strings)
for string in strings:
    print("\\x"+hex(ord(string))[2:], end='')

print()

print("0x",end='')
for string in strings:
    print(hex(ord(string))[2:], end='')

print()

```


```bash
$ python3 str2hex.py
Usage : a.py string

$ python3 str2hex.py /bin/sh
/bin/sh
\x2f\x62\x69\x6e\x2f\x73\x68
0x2f62696e2f7368

```

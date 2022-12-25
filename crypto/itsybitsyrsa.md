
## description

<p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209480410-c2316a90-68da-40e5-ad3a-75214895a08a.png">
</p>

#### You can download files for this challenges [here](https://github.com/vtran0314/niteCTF2022-Write-Up/tree/main/crypto)

In this challenge there are 3 given files: c_value, n_value and e_value.
The value of n_value is very big which lag out my VM machine couple times and the other two file are pretty small.

Up on analyzing and researching the files I noticed that the given n value is it greater than the value of m^e. Therefore, we can take a cube root of c and get the original message.


###Below is the code I used to solve this challenge

```
#!/usr/bin/python3

from decimal import *

with open('n_val', 'rb') as fn:
  n = fn.read()
  n = n.decode('utf-8')
  #print()

with open('c_cipher', 'rb') as fc:
  c = fc.read()
  c = c.decode('utf-8')
  #print(c_value)
  
e = 19


# https://docs.python.org/3/library/decimal.html
c = Decimal(c)
e = Decimal(e)

getcontext().prec = 500 # Set a big enough precision
root = pow(c, 1/e) # Calculate c^(1/e) = m^(e * 1/e) = m
print(root)

# Decode with no padding
m = hex(int(root))[2:-1] # Number to hex
m = ''.join(chr(int(m[i:i+2], 16)) for i in range(0, len(m), 2)) # Hex to Ascii
print(m)

```


```
┌──(kali㉿kali)-[~/Desktop/niteCTF/Crypto/itsybitsyrsa]
└─$ chmod +x solve1.py 
                                                           
┌──(kali㉿kali)-[~/Desktop/niteCTF/Crypto/itsybitsyrsa]
└─$ ./solve1.py 
32729160497211424999476882957330932909571487711098215779149999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999
nitectf{rsa_can_be_very_adaptable
```

#### Flag: nitectf{rsa_can_be_very_adaptable}

#### Resource I used to solve this challenge: [Attack RSA with very big module n and very small e](https://user-images.githubusercontent.com/106710730/209481119-7f584fc6-bbc7-443f-b735-48c5bb207a23.png)


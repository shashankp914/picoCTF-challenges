In this challenge,

First step is to download the **value** file from the description.

after that you'll encounter:

Decrypt my super sick RSA:

c: 62324783949134119159408816513334912534343517300880137691662780895409992760262021

n: 1280678415822214057864524798453297819181910621573945477544758171055968245116423923

e: 65537 

### It is an asymmetric cryptography encryption and we have to decode this. [READ MORE](https://en.wikipedia.org/wiki/RSA_(cryptosystem))

so for the first step we have to find p and q as the algo suggest and to divide n into p and q. we will use [factordb](http://factordb.com/) website:
then we'll get 
p:  1899107986527483535344517113948531328331

q: 674357869540600933870145899564746495319033

Lets do a python program to get this e decrypt this encryption:

follow the command to open editor in terminal:
```bash
vim mindpq.py
```

```bash
c = 62324783949134119159408816513334912534343517300880137691662780895409992760262021
n = 1280678415822214057864524798453297819181910621573945477544758171055968245116423923
e = 65537 
p = 1899107986527483535344517113948531328331
q = 674357869540600933870145899564746495319033

#totient is t

t = (p-1)*(q-1)

#d is private key 

d= pow(e,-1,t)

p= pow(c,d,n)

#converting hexcode to ascii string character

print(bytearray.fromhex(hex(p)[2:]).decode('ascii'))
```
You'll get the flag of this Challenge,

***Flag for this challenge:***  picoCTF{sma11_N_n0_g0od_05012767}

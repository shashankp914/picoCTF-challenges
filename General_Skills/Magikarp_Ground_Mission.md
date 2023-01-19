In this challenge, 

First, you have to start the instance given in hint!

after that, it will give a ssh port to connect, copy the server and connect by following command:

```bash
ssh ctf-player@venus.picoctf.net -p 56889
```
after connecting to the server, see the file given in the directory by following command:
```bash
ls
```
the flag is divided into 3 parts in 3 files, so the main task is to search for the files by given instruction files.

```bash
cat 1of3.flag.txt
```
you'll get first part of the flag!

then,
```bash
cat instructions-to-2of3.txt
```
now, it asked to go to the / directory so, copy the following command:
```bash
cd /
```

after that, you'll encounter 2nd part of the flag, for opening that, copy the following command:

```bash
cat 2of3.flag.txt
```

now, for last part of the flag, it asked to go to the home directory i.e. ~
so, copy the following command:

```bash
cd ~
```
after reaching home directory, follow the command for the 3rd part of the flag:
```bash
cat 3of3.flag.txt
```

You'll get the flag of this Challenge,

***Flag for this challenge:***  picoCTF{xxsh_0ut_0f_\/\/4t3r_5190b070}
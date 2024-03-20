# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/20f24a6a-8844-4709-a928-2b71b45f7b50)



cat < file2
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/d341302a-3310-4f18-90ec-eff690ae49ba)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/42d97403-8cc7-4b45-85cd-28731eb3f4b8)
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/c37aaac1-7bef-4513-b489-ea7cb4bdc9ea)

 
diff file1 file2
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/ab94eda2-c225-4fb1-ba55-2f058bcf3b76)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/12e66eb3-94a6-4951-97f7-37b4abfe966d)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/d89ad1e5-0286-4408-b0d5-36b82e8ae5f4)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/bf29cd0f-1c17-444f-8fe6-aea21e4dc567)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/f668e1ba-4232-4e77-b24f-109a845bce37)



grep hello newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/91813c5a-5c5e-48f1-b531-1219b472c820)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/959f4714-131b-47c2-b2f5-19913cc39548)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/e31b5105-7e6a-4da0-ba3f-019af8471df2)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/7007995d-4718-442e-b74c-21582d27c86e)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/8f6a8a8d-fd7e-4e9d-9b89-7e2849b90b45)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/8f74008e-5c1d-45b9-a58d-0ce78544129d)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/351f8626-e602-45ad-add8-091f68a855bd)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/d0e38208-33df-44d8-bee3-dc02a865db0d)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/c82dcfd1-dfe1-434c-aab6-f5d54af55e47)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/1b462c6d-a9df-456c-a912-27fe40149a25)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/0b48847f-6d82-441b-a616-d42e093bf848)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/ae86cc83-eb08-4c0c-912a-b7e46b176981)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/04e79f99-fb00-42d1-a294-644d50d8f19e)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/ae793648-5ba0-4172-99d6-c41d6b6a5b57)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/d4ac7aeb-7a69-464f-84ff-6277902fdabc)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/2b653063-beb0-41e8-b005-66682c83ff6f)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/4db0977a-c89e-446b-8bb8-1666d5b50e86)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/cebeaca7-ddf3-4f12-baf5-55a9920197c1)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/9fd86775-0a92-4809-8494-53d9f9b25309)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/9d02b2ec-df6a-457a-a1b4-b0bf8164a13c)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/2f6c90ec-f440-4f82-b5e8-ba4821e0c11d)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/fe70e6dd-b4f4-4b23-a2ed-cff1bfd19f83)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/d613186d-8f55-4bd6-91a9-359bf8e545b6)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/10bb4685-7aa5-4c09-8ec5-96530856f852)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/66f64840-978d-4170-9fd4-bab578bf9503)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/58350cb1-790b-44b3-b054-bc89dea5d55a)



seq 10 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/8dcd8d29-9515-4d54-b9fe-bb34e652b8d2)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/36b60de1-fb4a-453b-8006-37844d7aa36b)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/44b522d4-b9ba-4f73-a705-3e836389d3d2)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/72505b7c-f4ab-4806-8de4-4bd5b88486e2)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/9085b96c-3816-4ef5-9f23-cb62fc1480eb)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/5454d83f-d48d-4451-a095-ce5db06d90ce)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/0ffe94d6-0ffd-4fae-a3ff-6dfa401fe15b)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/c850970b-7c37-43b7-8ed9-179dcc5b2133)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/9923d2c7-57c9-49ee-8b85-e44f45f94b01)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/13e6698c-957e-4ae9-92b8-da5bf4da42ad)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/a5623fb7-20e3-4474-a785-eb2f0551034d)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/da8b7cd9-3488-463b-93e3-743fee0ebed7)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/460a1f3e-1bee-4040-af59-250962b2ad9d)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/fc021a3b-ce08-49a2-af2c-e8eb909f3b97)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/44efefd1-3b16-4825-8374-1fe9d3f78f62)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/05250e1f-3a43-4620-b821-2bd381495ee2)

gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/a72d61a8-20db-41ef-a2ce-52810c8144e3)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/e16e7002-28c1-46c7-9b2c-2928c4d07f05)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/d197d98f-482d-42dd-8e73-b6d190f7bc28)

 
ls file1
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/660466d3-22a1-44e9-8f13-986b17955a9f)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/158fef75-2ba6-413a-8994-170fc0ff0057)

abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/9a1910c0-d408-4656-9d95-9f56648547a0)


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/f224a10e-9484-4ccf-ad73-d5ee609f38dc)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/88302a3c-1544-4cc4-a68e-65c11e6a26d7)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/7afd2e68-ea4a-4ca6-bb08-88b5d6b1c16e)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/227cb896-8101-4a54-8362-44f142eebbff)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/efa73eb1-d25a-4338-9200-06a955fb86d9)


# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/1a0c896a-bec7-478a-ae0f-0a75bff1a026)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/634c4440-f671-4f5b-9f9a-36b81722465c)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/f9b6fdf8-1b52-4453-8574-8d0c379c7df5)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/75f26b12-5b64-44ab-9a64-883baffbdba5)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/9e439feb-08ab-4846-8e69-e23c3a850b67)

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/0131f3bd-f62d-4cff-a98b-621d001729c5)

 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/39ea25ed-1984-4508-b74b-97c143cf787b)

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/e75368ea-7329-4ce6-8be9-2bf8967dabdb)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/ef01d83a-4af8-4a12-840f-2be3b7426a3e)

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/cee4b411-74c0-4803-a329-b29ece3019db)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/a64e062a-d1bc-46e2-9922-e7017f80d9ab)


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/39b86708-8481-467e-9594-405599c59eed)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/6682c754-af9b-4f99-b307-f7b3b2519644)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/0b89576b-85c8-4172-b978-66d8b3c04e06)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/4f1077d4-693a-451c-8bd4-e8f1ffbe0dde)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/51aa68fd-cfd5-40a7-acb1-780148e44ed9)

cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 

 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/017a8dd6-cfdb-4634-97c0-3bad29f51a90)



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/66ed3d00-3035-470a-bf27-b17119df4f81)

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/99912dad-f5dc-4d33-9781-cfcdd0f95fd8)

 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/dd847c56-00c9-4ff8-9874-a9415fe37c76)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/17b3598c-307b-47d8-baf3-5ac0c267bc63)

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/875c284b-5bef-4c46-9a31-100881921325)

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![image](https://github.com/Suriya-MD/OS-Linux-commands-Shell-script/assets/147120571/a615b07c-298a-4873-986c-e22356edc482)


# RESULT:
The Commands are executed successfully.

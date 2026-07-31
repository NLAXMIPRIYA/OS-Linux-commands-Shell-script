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

<img width="476" height="343" alt="image" src="https://github.com/user-attachments/assets/0bbe8299-4587-44bf-99b7-da1154a2df5c" />


cat < file2
## OUTPUT

<img width="476" height="343" alt="image" src="https://github.com/user-attachments/assets/ad23b915-663e-4489-aa8e-9928564d3a7a" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="473" height="64" alt="image" src="https://github.com/user-attachments/assets/6934588f-0e2d-4221-b63c-0758d1b52b61" />

 
comm file1 file2
 ## OUTPUT
<img width="476" height="178" alt="image" src="https://github.com/user-attachments/assets/2bc622e8-3899-4e74-9411-638fd4eebe4e" />

 
diff file1 file2
## OUTPUT
<img width="469" height="158" alt="image" src="https://github.com/user-attachments/assets/c1800f18-8f90-4088-8745-a2cf759cc218" />


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

<img width="468" height="80" alt="image" src="https://github.com/user-attachments/assets/a9426c8b-4bff-46a2-bf8c-e68addc00f16" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="476" height="84" alt="image" src="https://github.com/user-attachments/assets/ca5b5eb8-fbbd-4f50-816a-d2f829d2f90b" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="466" height="92" alt="image" src="https://github.com/user-attachments/assets/4e9963cb-89d3-41fa-9f90-dd73c1636679" />


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

<img width="452" height="104" alt="image" src="https://github.com/user-attachments/assets/19b188a5-9095-48c0-a47b-535e1515d6a4" />


grep hello newfile 
## OUTPUT

<img width="476" height="67" alt="image" src="https://github.com/user-attachments/assets/ebb66708-66a5-4d22-873c-99c9e6fed4ec" />



grep -v hello newfile 
## OUTPUT
<img width="460" height="58" alt="image" src="https://github.com/user-attachments/assets/7107b652-c795-4858-b314-fd2dc9ef182e" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="461" height="74" alt="image" src="https://github.com/user-attachments/assets/075469ef-9f0b-4ad2-a095-a7344558effb" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="457" height="63" alt="image" src="https://github.com/user-attachments/assets/66fb2f3d-a6f7-43be-92aa-0341d954223d" />




grep -R ubuntu /etc
## OUTPUT

<img width="467" height="355" alt="image" src="https://github.com/user-attachments/assets/aabdbf5c-5873-45d9-afd5-235a9be21c8e" />



grep -w -n world newfile   
## OUTPUT
<img width="455" height="85" alt="image" src="https://github.com/user-attachments/assets/3cf9ced3-23ee-4f73-b4fa-77c2fd3f02d5" />


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

<img width="463" height="69" alt="image" src="https://github.com/user-attachments/assets/e9867f90-ce0f-4cf3-b528-3249d02a6a08" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="455" height="69" alt="image" src="https://github.com/user-attachments/assets/e2516982-ae21-4f68-bdb9-1f51932c9124" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="466" height="78" alt="image" src="https://github.com/user-attachments/assets/ebceebd1-c6e0-4753-aca1-024c9e752909" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="461" height="37" alt="image" src="https://github.com/user-attachments/assets/cb46a5b0-9db5-44ad-a8e3-ac784fe02aea" />



egrep '(world$)' newfile 
## OUTPUT

<img width="458" height="70" alt="image" src="https://github.com/user-attachments/assets/92f2505a-ab49-4e91-a120-aa038ca4f48b" />


egrep '(World$)' newfile 
## OUTPUT
<img width="449" height="47" alt="image" src="https://github.com/user-attachments/assets/e243c7d3-116b-4566-abef-92e1cdab9b47" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="461" height="79" alt="image" src="https://github.com/user-attachments/assets/25194732-c83d-4b8f-a7da-2d20561f9036" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="448" height="58" alt="image" src="https://github.com/user-attachments/assets/d54f55bf-e01d-4b8b-9ea8-d1776b431d6d" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="455" height="70" alt="image" src="https://github.com/user-attachments/assets/b046b70c-697b-4650-ad6b-fa4fd32ebd6e" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="450" height="53" alt="image" src="https://github.com/user-attachments/assets/50ac0d9c-cd9f-43ac-9dbf-805455bc950b" />


egrep l{2} newfile
## OUTPUT

<img width="457" height="55" alt="image" src="https://github.com/user-attachments/assets/acd003b5-2bd2-408f-94b3-5caf7ce03013" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="460" height="74" alt="image" src="https://github.com/user-attachments/assets/0fc014c5-71af-41dc-b5b2-20d06b78306a" />


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

<img width="460" height="71" alt="image" src="https://github.com/user-attachments/assets/a96400ff-6371-4b62-8a2e-8a3486152a6c" />


sed -n -e '$p' file23
## OUTPUT

<img width="445" height="65" alt="image" src="https://github.com/user-attachments/assets/4af7f850-5ef9-4d28-803c-097fa6947f44" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="477" height="153" alt="image" src="https://github.com/user-attachments/assets/77afb626-9e59-4205-b634-9de8988125fc" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="398" height="147" alt="image" src="https://github.com/user-attachments/assets/b2e0f46e-5410-4569-8a06-e3c7218b8d3d" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="475" height="152" alt="image" src="https://github.com/user-attachments/assets/b84ad976-b46c-41e2-9524-3d40d8808add" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="457" height="112" alt="image" src="https://github.com/user-attachments/assets/f59d5944-26bd-4484-9f8d-bd3afd0d60ff" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="341" height="104" alt="image" src="https://github.com/user-attachments/assets/d08893a5-d1f7-4522-bdf5-30936a70822b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="454" height="79" alt="image" src="https://github.com/user-attachments/assets/d21b7747-b035-4382-b1d9-49c420c8b36b" />



seq 10 
## OUTPUT

<img width="466" height="146" alt="image" src="https://github.com/user-attachments/assets/3bc58dca-6d9f-416c-8a7c-9fdf8ead7693" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="463" height="85" alt="image" src="https://github.com/user-attachments/assets/d11a7723-4ebe-4d75-83b4-fef71ebe55c3" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="475" height="83" alt="image" src="https://github.com/user-attachments/assets/51c6cc66-2a42-4039-b4db-ad5bae8f9715" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="452" height="101" alt="image" src="https://github.com/user-attachments/assets/8f05cf37-fe81-442d-8714-ae567b0103a2" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="455" height="88" alt="image" src="https://github.com/user-attachments/assets/ce5aa2d7-a7a2-476c-aecb-b68c6e6bfd16" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="451" height="92" alt="image" src="https://github.com/user-attachments/assets/e29f5fdd-e9ac-4cbf-8749-cd1843834a72" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="470" height="89" alt="image" src="https://github.com/user-attachments/assets/ad40dfa3-3e98-4582-8dba-5d4a69743822" />



sed -n '2,4{s/$/*/;p}' file23

<img width="458" height="94" alt="image" src="https://github.com/user-attachments/assets/baf0ceda-715c-4ce1-9946-37691e544ed4" />


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
<img width="467" height="113" alt="image" src="https://github.com/user-attachments/assets/e5be1f66-1e77-43fd-a054-a4a1841eacab" />


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
<img width="457" height="110" alt="image" src="https://github.com/user-attachments/assets/a1d808dd-079d-4679-8705-e2e2c4577509" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="443" height="161" alt="image" src="https://github.com/user-attachments/assets/14e1f435-681c-4c20-b567-8a4a276b5767" />

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
<img width="470" height="116" alt="image" src="https://github.com/user-attachments/assets/c432c43d-c335-497e-9466-53fecf39007b" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="455" height="104" alt="image" src="https://github.com/user-attachments/assets/3ca66e20-35ca-41a2-aa4f-4d99ad847270" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="478" height="152" alt="image" src="https://github.com/user-attachments/assets/cfb641e6-6ecb-4ecc-9eaf-bb090684d321" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="465" height="150" alt="image" src="https://github.com/user-attachments/assets/9c70df7b-d0d1-46ba-9f22-117f16706caa" />


tar -xvf backup.tar
## OUTPUT
<img width="469" height="154" alt="image" src="https://github.com/user-attachments/assets/d49c6606-727d-448d-a70f-80f337f4e88d" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="449" height="59" alt="image" src="https://github.com/user-attachments/assets/210f3797-758c-490d-bf46-c893e6a6775d" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="461" height="103" alt="image" src="https://github.com/user-attachments/assets/51d82df6-50e7-49c6-ac89-8c5bb467b564" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="466" height="69" alt="image" src="https://github.com/user-attachments/assets/22d69269-5c91-4899-91dc-995a1a37014b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="461" height="94" alt="image" src="https://github.com/user-attachments/assets/167e4290-ad30-4a32-86f9-f60a043a0880" />


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

<img width="436" height="214" alt="image" src="https://github.com/user-attachments/assets/c14959b0-5d84-42eb-b083-282b5169bc14" />

 
ls file1
## OUTPUT
<img width="470" height="72" alt="image" src="https://github.com/user-attachments/assets/57aeca00-e5db-46fd-9b43-dbfde3deaf96" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
<img width="478" height="113" alt="image" src="https://github.com/user-attachments/assets/f814c2cb-e1d8-45bd-9cb4-b8bf01b2b6bd" />

 
echo $?
## OUTPUT 
 
abcd
<img width="475" height="43" alt="image" src="https://github.com/user-attachments/assets/36d35f1f-a84a-4144-a143-d1fe56044d8b" />

 
echo $?
 ## OUTPUT
<img width="403" height="72" alt="image" src="https://github.com/user-attachments/assets/450da70a-ccfa-4f1b-9cdf-85f804b6cbf5" />


 
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
##OUTPUT

<img width="463" height="174" alt="image" src="https://github.com/user-attachments/assets/59df7a95-923b-4f47-a814-b29568f8fed2" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="446" height="274" alt="image" src="https://github.com/user-attachments/assets/79358ac8-67bd-4d01-8c9c-9dce62d6efcf" />


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
<img width="448" height="106" alt="image" src="https://github.com/user-attachments/assets/22715e4e-a649-49f0-8df0-580340aadc50" />

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
##OUTPUT

<img width="476" height="283" alt="image" src="https://github.com/user-attachments/assets/5f5192ae-5dea-4048-ab4f-2f3b70c1f33e" />


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
##OUTPUT
<img width="462" height="157" alt="image" src="https://github.com/user-attachments/assets/72a5e2d4-a341-40d4-8800-59aa19f132a1" />

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
<img width="452" height="126" alt="image" src="https://github.com/user-attachments/assets/eefc0df8-d5ed-43b6-b8c0-d489e6f20e4e" />

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
 
 <img width="467" height="249" alt="image" src="https://github.com/user-attachments/assets/5f6ec460-5fbc-49dc-8aeb-11864ac33382" />

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

 <img width="458" height="266" alt="image" src="https://github.com/user-attachments/assets/abe3ddcf-3ec6-422d-9eab-85ee011ae5e5" />

 
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
<img width="456" height="238" alt="image" src="https://github.com/user-attachments/assets/26f6c738-c082-467e-973f-d1ad8f33881c" />

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
 <img width="469" height="200" alt="image" src="https://github.com/user-attachments/assets/7d102002-e295-4862-9b5f-adc7b6024f2b" />

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
<img width="457" height="230" alt="image" src="https://github.com/user-attachments/assets/f25234cc-2563-4dbb-b866-965426e64a0d" />

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
<img width="470" height="218" alt="image" src="https://github.com/user-attachments/assets/cf7ae4ea-d106-40d3-8b14-0cd1dffb94b6" />


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

<img width="175" height="128" alt="image" src="https://github.com/user-attachments/assets/59f6fb21-69ca-43a8-81b5-baea98c217db" />


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

<img width="316" height="155" alt="image" src="https://github.com/user-attachments/assets/c1555d64-b800-4ff9-ac41-e89f08586197" />


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
<img width="290" height="166" alt="image" src="https://github.com/user-attachments/assets/0424a843-2b4d-4279-b7d5-f0a5c03ed60e" />

 
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

<img width="308" height="140" alt="image" src="https://github.com/user-attachments/assets/52f85284-dc13-40d6-bf72-ca6215915786" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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
## OUTPUT
 <img width="308" height="97" alt="image" src="https://github.com/user-attachments/assets/e2d3305d-6be3-4ded-972c-c6fa953f2a79" />

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
## OUTPUT
<img width="310" height="107" alt="image" src="https://github.com/user-attachments/assets/3a34cec3-b2d9-46a9-a8f0-2094aa96a107" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Uploading image.png…]()


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

## OUTPUT
$ ./argshift.sh 1 2 3
 
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


# RESULT:
The Commands are executed successfully.

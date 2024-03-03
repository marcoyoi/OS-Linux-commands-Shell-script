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
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/fbe0bc98-6da8-4e23-866f-8d5c5f44b8e5)



cat < file2
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/8279c19c-a21b-404c-b0c3-0e7567363944)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/3071a2f9-ae05-413d-bd36-1fe91ac3f3ca)

comm file1 file2
 ## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/a7942b0c-79a0-49b9-be76-d992c05d8269)

 
diff file1 file2
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/2a8cee62-bada-42d3-88ba-f0dd00a76823)


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
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/2431ad55-f118-4c69-8b6f-a2fbf1f3d752)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/3ba6a32b-bd56-4464-9a63-23f2358924ef)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/ce334c4c-b249-447e-8e46-f588e71e9b3e)


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
 ![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/5e656d53-72fe-474c-861b-012c233d536d)




grep hello newfile 
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/15fc26b0-90b1-4a27-89c3-3b2a530b9d2b)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/e086fad4-f839-4ddb-ac2d-d1da48a0e840)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/d6f00ee0-149b-4f3a-b724-0e2bdbde947c)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/9610bf74-0423-461f-ada3-c530eaf61091)




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/ae68ef07-333d-457c-bbbf-f20599ae965b)


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
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/695515f2-c4b0-4162-812e-3d0340766883)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/28827ea3-f1f1-48ff-b655-4562def24e9c)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/6ecfce4e-8c4a-432b-91cc-aa15de74eab8)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/0cad1aff-9aba-4e6b-b24f-8a615d487914)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/4f280a81-6ba4-4286-96fb-1ead60d7c039)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/b703763c-5cce-4ea2-b61e-9229ec3c65e7)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![304756993-8407e750-360d-4618-bcf1-a15397ac5679](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/e7a1913c-d85a-47f0-9553-4a3f050d09c3)



egrep '[1-9]' newfile 
## OUTPUT
![304756993-8407e750-360d-4618-bcf1-a15397ac5679](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/aca8c451-1f6e-41de-a553-5a92fb9f9204)



egrep 'Linux.*world' newfile 
## OUTPUT
![305806311-11d2f11a-d9dd-4031-ae76-4a1e5d45cbab](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/113d0fee-04d5-40ad-a609-93d81dde00de)


egrep 'Linux.*World' newfile 
## OUTPUT
![305806567-aea04219-9477-4c77-8869-7e5a236b52cd](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/5833194e-a0bc-4e53-a33b-3ff9a94dca1a)


egrep l{2} newfile
## OUTPUT

![305806939-57a931c1-b4a9-474b-85f6-673a6677fa74](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/48bf60d7-46ad-4f14-9272-c15430adff7b)


egrep 's{1,2}' newfile
## OUTPUT 
![305807162-0b0e3818-ad4a-4457-8d48-bb0b9781d525](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/8c100544-66a9-487d-a0e6-5bef6f48f4d3)


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
![305807842-15f71b7d-9de1-486b-95f9-d0a47edd4cb2](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/ec0bcfdc-8437-45ba-b72a-e9f7436079b6)


sed -n -e '3p' file23
## OUTPUT
![305808121-935e41ac-cef7-4004-86bd-8468ce609fd9](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/f6dcdd26-1058-4677-84aa-df932d8c4a13)



sed -n -e '$p' file23
## OUTPUT
![305808421-fde3c44c-c67b-4577-add4-04f19672d4c7](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/00514ad6-a5de-4c13-8607-ab15558a6432)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![305808879-515073f9-5a64-4e95-b71e-d79c8587acf6](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/b20c15a0-e230-497d-a0c8-aa105cd34c1a)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![305809256-438d0526-e72c-48a8-b2c2-02c72d41d513](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/96019097-f7bd-4625-acbb-eb33134133db)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![305809737-6aa011d2-186a-414f-b514-00debb8a44e1](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/c0fe0276-13a1-4ad7-9288-9697b8b26924)



sed -n -e '1,5p' file23
## OUTPUT
![305809737-6aa011d2-186a-414f-b514-00debb8a44e1](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/ebe97395-e1cf-45a9-b7ec-83c1a20c28c7)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![305810312-b7e023e8-c5e4-4af6-bbcd-6438f58cad6b](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/fcdaf555-b847-4da1-b720-6e1629b3bca1)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![305810312-b7e023e8-c5e4-4af6-bbcd-6438f58cad6b](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/5a9a74ab-5270-435e-b4f8-7490ab970dcd)



seq 10 
## OUTPUT
![305810629-1430b248-5100-409c-b0f7-a6ad12c5f959](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/81ca8356-ed64-46c5-870a-f40a48faa8dc)



seq 10 | sed -n '4,6p'
## OUTPUT
![305810904-1f5d6e2f-1a7b-4eea-8552-acff8c81523b](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/053a9147-6aab-425b-9e32-cd9f38ba3994)



seq 10 | sed -n '2,~4p'
## OUTPUT
![305811484-eb525a7e-43b5-4916-af88-3bc8c6b4cdca](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/d1cb1712-b654-4649-b0d7-9f9a09ac7e35)



seq 3 | sed '2a hello'
## OUTPUT
![305811718-84f84424-6a15-4d3b-a285-941d3fe16861](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/0944c95c-3af8-431f-943b-fdecf92a546a)



seq 2 | sed '2i hello'
## OUTPUT
![305812046-7bea0f04-279e-4903-a337-d4902ebd4032](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/8050f6b4-519d-4d1c-a5c8-cc846dcb578c)


seq 10 | sed '2,9c hello'
## OUTPUT
![305812297-eafaeb58-e136-4d78-8e1f-bd4de3e2ff9d](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/cc05daa4-6b46-4007-ac1b-5fe60ad93550)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![305812800-12731e6d-a860-400f-a9bb-2f5065523170](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/9da71deb-2602-4466-9ab2-a74604ade15f)



sed -n '2,4{s/$/*/;p}' file23



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
![305813529-e5d6736e-cf4e-41a3-b67d-1782fb4559b3](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/9dcd02e6-c1bc-4477-88f5-447b0b74bc8b)


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
![305814410-c09905f2-fb18-476a-96fc-e262f634d64e](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/d4dc3d4a-8a66-47e4-8bd4-dac17a844178)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![305816229-5f25712f-0ef9-4879-9d54-e78ff0d86f5e](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/e1ddf951-6edd-4a92-9c94-85a7c2161de8)

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
![306538777-aef9e430-000a-4eca-a90b-5c110a4f8b44](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/3141d3d6-4c32-4fd7-958a-4a1eeef4f473)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![306538908-c3162aaa-49f9-4871-975f-c899bad6ddad](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/42013c1f-7c15-48d8-b811-35a6cdfd4b53)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![306539900-259a58b1-5889-4760-8ec0-f67ea57c7483](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/81c2a979-8ae8-478a-a609-0fb196adf13f)


tar -xvf backup.tar
## OUTPUT
![306540140-27f00a78-61df-4953-b159-2234ef1e8472](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/6cc3ed69-0e28-407b-9e37-3c24f7807626)

gzip backup.tar

ls .gz
## OUTPUT
 
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


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
 ![306552604-0873e9e1-fc55-454b-9b95-af81ffff5b78](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/b1f018ae-78f0-4214-b83e-6e51d8089d73)


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![306541738-5afd01d6-bc49-420d-9376-f1d88e9b0178](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/b88a70e3-86d7-4432-9f81-53e661375a7b)

abcd
 
echo $?
 ## OUTPUT
![306542087-e7518e15-b5da-412c-a1ed-a9f6bc85220d](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/9784998f-827d-445d-a1b3-e73823a28193)


 
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
![306557718-2266709f-d5df-4e6e-8825-f7a4e29cf7d0](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/6caa5124-beb7-49d2-81de-b4b3032934e6)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![306566416-0f088335-0b68-436e-b56e-a413b3316a37](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/528b3a80-a3ef-4a18-89a9-ca9bf807f0d9)


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
![307673145-3194dc09-c476-4167-a39e-779103ef8029](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/434dfefb-4912-4cb9-a52c-878fc88430df)

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
![307673777-cfa8b86b-0e65-478d-aeaa-5a507d5bedc9](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/1dc07a2e-bdc2-463a-a027-3bef37fa75ce)



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
![306545355-49a3408b-2e23-4f73-9cf2-407575a726c6](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/2dd0643b-0a15-43bc-9a01-a6425c7e4b15)

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![307674113-fe1af2ba-772b-44ba-938f-01691ae96134](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/d67460cc-9343-4f73-8262-6cb9224295dc)

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
![307674426-969d3670-be61-4d5b-81d2-d53103223e8d](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/a998b22e-cf27-499b-aae7-b74814b365de)

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
![307674756-4f69c2a2-0a5d-47db-af34-ce60e46db3b5](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/22caa0d2-a17e-4bfa-8058-3ff59ee2f43d)


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
![307675139-3ba0b9af-a6b9-433f-8acf-dd42ecf4932d](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/ba822c9e-a4cf-44c2-b71d-dbbc05912aa9)

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
 ![307675139-3ba0b9af-a6b9-433f-8acf-dd42ecf4932d](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/83efe235-68fc-49f6-b86b-8d2109789b03)
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
 ![307675139-3ba0b9af-a6b9-433f-8acf-dd42ecf4932d](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/83efe235-68fc-49f6-b86b-8d2109789b03)

 
 
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
 ![307676514-f7fe8180-dde0-4567-b576-c29d30b63b55](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/5c28cecf-b2fc-4482-b722-25f60a00c6fd)

 
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
 ![307676785-169b4ed1-16f1-4f17-b7cc-e3cd3d5ab22a](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/48cb47b5-a095-430e-bac8-7ebbc69039d6)

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
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
![307677131-885626ba-ec97-4b35-8972-68e3f4d814ab](https://github.com/marcoyoi/OS-Linux-commands-Shell-script/assets/128804366/dc2d7467-b775-43e9-a3dd-30f03f3c58f3)

$ chmod 755 forin1.sh

## OUTPUT
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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

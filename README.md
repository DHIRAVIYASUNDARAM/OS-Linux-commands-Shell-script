# Name: DHIRAVIYA S
# Register No:212223040041
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

cat < file2
## OUTPUT
![Screenshot 2024-08-26 135138](https://github.com/user-attachments/assets/f864ce07-f0e2-4808-822d-b177d8b043cc)


# Comparing Files
cmp file1 file2

comm file1 file2
 ## OUTPUT
![Screenshot 2024-08-26 135204](https://github.com/user-attachments/assets/ea4d1ab8-3377-469a-90b8-2582a28c27cd)

 
diff file1 file2
## OUTPUT
![Screenshot 2024-08-26 135218](https://github.com/user-attachments/assets/3b5621d2-8481-43c5-9750-0dfacba548bb)


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
![Screenshot 2024-08-26 135602](https://github.com/user-attachments/assets/fb4127ae-bcb1-4f8e-8cfa-f27d56bc71e0)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2024-08-26 135608](https://github.com/user-attachments/assets/c1c0bed8-fe05-4a60-b3f0-6fe7b3afd405)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2024-08-26 135618](https://github.com/user-attachments/assets/f2fc7262-b3d9-4ab6-8ead-234e3d77e7cd)


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
![Screenshot 2024-08-26 135803](https://github.com/user-attachments/assets/d76f2993-bf55-4619-ba31-6414f0810b89)



grep hello newfile 
## OUTPUT
![Screenshot 2024-08-26 135809](https://github.com/user-attachments/assets/040df74f-558d-42bc-b646-93740eea151d)




grep -v hello newfile 
## OUTPUT
![Screenshot 2024-08-26 173855](https://github.com/user-attachments/assets/85cf2cb5-c285-4f68-a537-21a60b1e591b)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2024-08-26 135826](https://github.com/user-attachments/assets/0e775134-33f8-48fe-803c-dbdc22e53877)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2024-08-26 135835](https://github.com/user-attachments/assets/b45807fc-5515-45c2-87e6-3114c90f9b32)




grep -R ubuntu /etc

grep -w -n world newfile   
## OUTPUT
![Screenshot 2024-08-26 140017](https://github.com/user-attachments/assets/9b427e33-3209-4689-9a25-fabf8a78c322)


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
![Screenshot 2024-08-26 140112](https://github.com/user-attachments/assets/f8107750-7053-436c-b0c5-80ba30138f6b)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2024-08-26 140122](https://github.com/user-attachments/assets/32b55fee-0744-4f12-9e2b-0ae62bb01683)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2024-08-26 140128](https://github.com/user-attachments/assets/e1df181a-9afd-46d4-af8d-2a4876a74231)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2024-08-26 140139](https://github.com/user-attachments/assets/3869773b-114f-4f20-a3d7-635286614616)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2024-08-26 140145](https://github.com/user-attachments/assets/e96d9a70-1ae0-4889-8da9-7227779c1fd4)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2024-08-26 140156](https://github.com/user-attachments/assets/98881563-4501-4bcf-bca3-f4ee59086b05)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2024-08-26 174022](https://github.com/user-attachments/assets/4f9a5b54-0321-4fd7-bdf2-1c9b9da4ca37)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2024-08-26 140225](https://github.com/user-attachments/assets/ad0c5a24-1000-405e-808d-f8f8acf09e03)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2024-08-26 140237](https://github.com/user-attachments/assets/2de9dcda-a96d-42cd-bdb8-db28f0145296)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2024-08-26 140245](https://github.com/user-attachments/assets/c8cbc2d5-a639-43a3-9417-5256dc6a295d)


egrep l{2} newfile
## OUTPUT
![Screenshot 2024-08-26 174132](https://github.com/user-attachments/assets/57598cd9-b500-41fb-acb6-78200c9783d5)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2024-08-26 174143](https://github.com/user-attachments/assets/eb4d1556-5b98-4bbe-85c2-209ea644d616)


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
![Screenshot 2024-08-26 160522](https://github.com/user-attachments/assets/2f3304e9-0bfc-4b64-b340-b46555f64dd9)



sed -n -e '$p' file23
## OUTPUT
![Screenshot 2024-08-26 160530](https://github.com/user-attachments/assets/46cae32d-9445-4b4e-869e-32c76d14ad33)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-08-26 160542](https://github.com/user-attachments/assets/b0c99219-5a7c-43b1-86aa-04a4f52f8ed4)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2024-08-26 160549](https://github.com/user-attachments/assets/ec4a262a-79f0-4bc9-99b9-86086244d9c2)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2024-08-26 160606](https://github.com/user-attachments/assets/a35f2332-240e-44e2-9dc6-33964628d012)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot 2024-08-26 160613](https://github.com/user-attachments/assets/228b5bca-22a7-4747-a179-25d387201902)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2024-08-26 160622](https://github.com/user-attachments/assets/786952a1-75e3-4215-9b9c-c9ad04838b85)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2024-08-26 160630](https://github.com/user-attachments/assets/0f400ac1-2426-4426-b431-acaf5b23734d)



seq 10 
## OUTPUT
![Screenshot 2024-08-26 160637](https://github.com/user-attachments/assets/46f3f83c-edc5-44a0-b86e-a8b490ef70be)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2024-08-26 160642](https://github.com/user-attachments/assets/327ce4ff-6976-4036-b4e1-e5c378090dec)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2024-08-26 160655](https://github.com/user-attachments/assets/5dd205b7-e61a-47e3-b0f8-5d98e3029ac5)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2024-08-26 160700](https://github.com/user-attachments/assets/e0fb7b20-60fb-4c48-8326-5b3f9b98852e)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2024-08-26 160708](https://github.com/user-attachments/assets/44d40e5b-f158-4a1e-b7fc-9a0a165d153a)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2024-08-26 160716](https://github.com/user-attachments/assets/87205a14-42ea-4d99-b420-b112993ef481)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot 2024-08-26 160729](https://github.com/user-attachments/assets/f13fe69f-ff8c-41c3-8459-7a44fa69973c)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot 2024-08-26 160751](https://github.com/user-attachments/assets/fca3fabe-160d-4f48-a261-6528613e113e)



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
![Screenshot 2024-08-26 161732](https://github.com/user-attachments/assets/c81f5ba9-3e3c-48b5-b7d9-8312f346608b)


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
![Screenshot 2024-08-26 161807](https://github.com/user-attachments/assets/4398bd51-2b26-4d43-ac72-9322eab1f486)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2024-08-26 161814](https://github.com/user-attachments/assets/e989764b-db90-412f-8917-907dc8bfdbdd)


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
![Screenshot 2024-08-26 161825](https://github.com/user-attachments/assets/d5415f9b-7968-4d31-8f28-879eab502ce0)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot 2024-08-26 161831](https://github.com/user-attachments/assets/0276db20-34ab-468c-bac2-79a7354b7de5)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2024-08-26 161951](https://github.com/user-attachments/assets/88d18a4d-e0fa-48d8-8dfe-378fa5381a77)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2024-08-26 162533](https://github.com/user-attachments/assets/9f59d0f1-1dcb-4cf0-81fd-ee7430dc6803)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2024-08-26 162016](https://github.com/user-attachments/assets/2d176ada-bfe1-4a9c-812f-a98e52ad5070)



gzip backup.tar

gunzip backup.tar.gz
## OUTPUT
![Screenshot 2024-08-26 164129](https://github.com/user-attachments/assets/e2d00965-7012-49d2-ab0a-f81480df3568)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh

./my-script.sh
## OUTPUT
 ![Screenshot 2024-08-26 165407](https://github.com/user-attachments/assets/f4d1b5fe-2c2c-48e2-b407-4f0ec4dfa6be)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2024-08-26 165602](https://github.com/user-attachments/assets/ecd49b65-eb13-43b7-8559-1c961377cc57)


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
![Screenshot 2024-08-26 165917](https://github.com/user-attachments/assets/ad12eb83-dffa-40db-ba0a-86015487a9d3)

 
ls file1
## OUTPUT
![Screenshot 2024-08-26 170053](https://github.com/user-attachments/assets/2a58c8d5-859d-49d7-8ffb-12692e77ef4c)


echo $?
## OUTPUT
![Screenshot 2024-08-26 164528](https://github.com/user-attachments/assets/01042460-9206-4d1f-bf6e-399258bd704b)


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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2024-08-26 170224](https://github.com/user-attachments/assets/ba1c937d-ce20-4788-96bd-214dc61c16d2)


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
![Screenshot 2024-08-26 170249](https://github.com/user-attachments/assets/7a8b3756-9878-400c-bc9f-46cd3ec5fdb5)

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
![Screenshot 2024-08-26 170339](https://github.com/user-attachments/assets/685e6136-5436-480b-b921-9c6f2170133d)



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
![Screenshot 2024-08-26 170408](https://github.com/user-attachments/assets/332af5c6-1f6f-461f-9701-34dc26ca7a4d)


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
![Screenshot 2024-08-26 170427](https://github.com/user-attachments/assets/bb2bb39c-ce98-46ee-839d-faf20af52564)


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
![Screenshot 2024-08-26 170440](https://github.com/user-attachments/assets/44fe25e3-b595-4185-9275-50dc8e909984)

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
## OUTPUT
 ![Screenshot 2024-08-26 170453](https://github.com/user-attachments/assets/1d33bd11-7f19-4d40-81fe-b641873e6cc4)

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
## OUTPUT
![Screenshot 2024-08-26 170528](https://github.com/user-attachments/assets/a20ba2be-4dd3-4507-8e73-1d7894076283)

 
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
$ ./untiltest.sh
## OUTPUT
![Screenshot 2024-08-26 170548](https://github.com/user-attachments/assets/77ee6284-10a4-423f-b8e9-0bc3f344af6b)

 
 
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
$ ./forin1.sh
## OUTPUT
![Screenshot 2024-08-26 170610](https://github.com/user-attachments/assets/098cae74-7956-4b0f-8b8b-081ae7e0ebac)

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ``` 
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
## OUTPUT

 ![Screenshot 2024-08-26 170630](https://github.com/user-attachments/assets/bb42aef7-1a59-47bf-b60d-3a707b8fcbbf)

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
## OUTPUT
![Screenshot 2024-08-26 170646](https://github.com/user-attachments/assets/b0b4f208-0fb7-4cde-bbe9-f940e8eaa2e5)


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
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```

## OUTPUT
![Screenshot 2024-08-26 171740](https://github.com/user-attachments/assets/e22eabab-94b5-47cb-86d0-e8887ec00a04)


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
![Screenshot 2024-08-26 171850](https://github.com/user-attachments/assets/c9f26f2d-0c64-4099-93df-907a613d8a92)

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
![Screenshot 2024-08-26 171903](https://github.com/user-attachments/assets/020fdc89-b84e-4548-910a-f113eec8fcdf)

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
![Screenshot 2024-08-26 171925](https://github.com/user-attachments/assets/e5ffdcba-6349-43d4-8423-df4ca8ab3982)

 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
![Screenshot 2024-08-26 171948](https://github.com/user-attachments/assets/0c030265-7e5a-44f4-82da-438235fd3ac6)
 
 
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
![Screenshot 2024-08-26 172015](https://github.com/user-attachments/assets/ca843eba-6b90-41f1-b9c8-f98df1189e73)


 
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
 $./funcex.sh 
 ## OUTPUT
![Screenshot 2024-08-26 172951](https://github.com/user-attachments/assets/338963c7-2f22-40cd-8c09-34e9475d99bc)

 
 $./funcex.sh 1 2
 ## OUTPUT
![Screenshot 2024-08-26 172958](https://github.com/user-attachments/assets/335a5e12-8b42-45a6-b6d1-7974430f600b)

 
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
![Screenshot 2024-08-26 173024](https://github.com/user-attachments/assets/9ee4052d-96fa-46f0-bfcc-6f94742d5e77)

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

$ ./argshift1.sh 1 2 3
 
## OUTPUT
![Screenshot 2024-08-26 175636](https://github.com/user-attachments/assets/34b9a0fe-51f5-4159-80d8-77b5a55e2c51)
 
 
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
 ![Screenshot 2024-08-26 173619](https://github.com/user-attachments/assets/539a0f73-502f-4b31-846a-af9ecce2d02a)

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
![Screenshot 2024-08-26 173639](https://github.com/user-attachments/assets/0c7687ff-f3cd-4779-a2f9-96417eba3df5)


# RESULT:
The Commands are executed successfully.

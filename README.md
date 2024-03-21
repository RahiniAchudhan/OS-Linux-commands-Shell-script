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
```cat < file1```
## OUTPUT
![Screenshot (189)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/6ca5edc1-fa91-44f0-9c92-37e53399c2c2)

```cat < file2```
## OUTPUT
![Screenshot (190)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/85c731a5-b1c4-437f-8f05-c473035443f2)

# Comparing Files
```cmp file1 file2```
## OUTPUT
![Screenshot (191)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/dcf534a6-99dd-4bc2-b601-667cca5e0aee)
 
```comm file1 file2```
 ## OUTPUT
![Screenshot (192)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/c5a9921e-c213-4eb8-958d-453e2a6e45c4)

```diff file1 file2```
## OUTPUT
![Screenshot (193)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/2da51cd3-e660-4c8e-85b5-3891033ef313)
\ No newline at end of file
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


```cut -c1-3 file11```
## OUTPUT
![Screenshot (194)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/f1de8441-328a-4602-92c7-0febd670dae8)

```cut -d "|" -f 1 file22```
## OUTPUT
![Screenshot (195)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/e7e04cd9-55c8-440e-9cc5-5e15b4e621b9)

```cut -d "|" -f 2 file22```
## OUTPUT
![Screenshot (196)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/e12042b0-0271-4823-af8a-7493884cfaee)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
```grep Hello newfile ```
## OUTPUT
![Screenshot (198)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/a95bd96d-bbb9-4eaf-938d-3c183696ca09)

```grep hello newfile ```
## OUTPUT
![Screenshot (199)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/8806a80f-3320-4a7d-9fe0-c445885f5d74)

```grep -v hello newfile ```
## OUTPUT
![Screenshot (200)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/c1c75f7e-2b07-451b-bedf-a667e4389f88)

```cat newfile | grep -i "hello"```
## OUTPUT
![Screenshot (201)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/4ba4f3de-87eb-4dab-9671-fc004ee51ad7)

```cat newfile | grep -i -c "hello"```
## OUTPUT
![Screenshot (202)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/622ce37b-b9ff-4b43-80b2-8c3c5a87407e)

```grep -R ubuntu /etc```
## OUTPUT
![Screenshot (203)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/29a97096-3d25-44e8-9ee1-89196450c032)

```grep -w -n world newfile```
## OUTPUT
![Screenshot (204)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/3ef941b8-b408-467a-8421-386c707ffa92)

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

Hello world hello world

```egrep -w '(H|h)ello' newfile ```
## OUTPUT
![Screenshot (205)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/2e9a9361-c012-4199-9c85-a70d9ae068d7)

```egrep -w '(H|h)ell[a-z]' newfile ```
## OUTPUT
![Screenshot (206)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/c0332a26-1ce8-4a8b-8840-52b4ba626381)

```egrep '(^hello)' newfile ```
## OUTPUT
![Screenshot (207)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/79db0678-2f7c-41fd-99ad-db7bdcff88cd)

```egrep '(world$)' newfile ```
## OUTPUT
![Screenshot (208)](https://github.com/RahiniAchudhan/OS-Linux-commands-Shell-script/assets/145742838/66600ccb-c3e4-45a8-9686-025499a22710)

```egrep '(World$)' newfile ```
## OUTPUT

Lunix is best in the World
```egrep '((W|w)orld$)' newfile``` 
## OUTPUT

Hello world

hello world

Lunix is best in the World


```egrep '[1-9]' newfile``` 
## OUTPUT

Lunix is world number 1


```egrep 'Linux.*world' newfile ```
## OUTPUT

Lunix is world number 1

```egrep 'Linux.*World' newfile ```
## OUTPUT

Lunix is best in the World

```egrep l{2} newfile```
## OUTPUT

Hello world

hello world


```egrep 's{1,2}' newfile```
## OUTPUT 

Lunix is world number 1

Unix ix predecessor

Lunix is best in the World

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


```sed -n -e '3p' file23```
## OUTPUT

1002 | tom |  5000 | Admin

```sed -n -e '$p' file23```
## OUTPUT

1001 | Ram | 10000 | HR


```sed  -e 's/Ram/Sita/' file23```
## OUTPUT

1001 | Sita | 10000 | HR

1001 | Sita | 10000 | HR

1002 | tom |  5000 | Admin

1003 | joe |  7000 | Developer

1005 | Sam |  5000 | HR

1004 | Sit |  7000 | Dev

1003 | Joe |  7000 | Developer

1001 | Sita | 10000 | HR




```sed  -e '2s/Ram/Sita/' file23```
## OUTPUT

1001 | Ram | 10000 | HR

1001 | Sita | 10000 | HR

1002 | tom |  5000 | Admin

1003 | joe |  7000 | Developer

1005 | Sam |  5000 | HR

1004 | Sit |  7000 | Dev

1003 | Joe |  7000 | Developer

1001 | Ram | 10000 | HR



```sed  '/tom/s/5000/6000/' file23```
## OUTPUT

1001 | Ram | 10000 | HR

1001 | Ram | 10000 | HR

1002 | tom |  5000 | Admin

1003 | joe |  7000 | Developer

1005 | Sam |  5000 | HR

1004 | Sit |  7000 | Dev

1003 | Joe |  7000 | Developer

1001 | Ram | 10000 | HR

```sed -n -e '1,5p' file23```
## OUTPUT


1001 | Ram | 10000 | HR

1001 | Ram | 10000 | HR

1002 | tom |  5000 | Admin

1003 | joe |  7000 | Developer

1005 | Sam |  5000 | HR


```sed -n -e '2,/Joe/p' file23```
## OUTPUT


1001 | Ram | 10000 | HR

1002 | tom | 5000 | Admin

1003 | Joe | 7000 | Developer

```sed -n -e '/tom/,/Joe/p' file23```
## OUTPUT

1002 | tom | 5000 | Admin

1003 | Joe | 7000 | Developer

```seq 10 ```
## OUTPUT

1 2 3 4 5 6 7 8 9 10


```seq 10 | sed -n '4,6p'```
## OUTPUT

4 5 6

```seq 10 | sed -n '2,~4p'```
## OUTPUT


2 3 4
```seq 3 | sed '2a hello'``
## OUTPUT

1 2 hello 3

```seq 2 | sed '2i hello'```
## OUTPUT

1 hello 2

```seq 10 | sed '2,9c hello'```
## OUTPUT

1 hello 10

```sed -n '2,4{s/^/$/;p}' file23``
## OUTPUT

$1001 | Ram | 10000 | HR

$1002 | tom | 5000 | Admin

$1003 | Joe | 7000 | Develop

```sed -n '2,4{s/$/*/;p}' file23```
1001 | Ram | 10000 | HR*

1002 | tom | 5000 | Admin*

1003 | Joe | 7000 | Developer*

# Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
```sort file21```

##OUTPUT

1001 | Ram | 10000 | HR

1002 | tom | 5000 | Admin

1003 | Joe | 7000 | Developer

1004 | Sit | 7000 | Dev

1005 | Sam | 5000 | HR

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

1001 | Ram | 10000 | HR 
1002 | tom | 5000 | Admin 
1003 | Joe | 7000 | Developer 
1005 | Sam | 5000 | HR 
1004 | Sit | 7000 | Dev

# Using tr command

```cat file23 | tr [:lower:] [:upper:]```
 ## OUTPUT
1001 | RAM | 10000 | HR
1001 | RAM | 10000 | HR 
1002 | TOM | 5000 | ADMIN 
1003 | JOE | 7000 | DEVELOPER 
1005 | SAM | 5000 | HR 
1004 | SIT | 7000 | DEV 
1003 | JOE | 7000 | DEVELOPER 
1001 | RAM | 10000 | HR


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
```cat urllist.txt | tr -d ' '```

 ## OUTPUT

www.yahoo.com 
www.google.com 
www.mrcet....com
 
```cat urllist.txt | tr -d ' ' | tr -s '.'```
## OUTPUT

www.yahoo.com 

www.google.com 

www.mrcet.com

#Backup commands

tar -cvf backup.tar *
## OUTPUT

tar: can't open 'bench.py': I/O error file21 file22 file23 tar: can't open 'hello.c': I/O error tar: can't open 'hello.js': I/O error newfile tar: can't open 'readme.txt': I/O error urllist.txt tar: error exit delayed from previous errors

```
mkdir backupdir
 
mv backup.tar backupdir

tar -tvf backup.tar
```
## OUTPUT
tar -xvf backup.tar

```tar -xvf backup.tar```
## OUTPUT

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
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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

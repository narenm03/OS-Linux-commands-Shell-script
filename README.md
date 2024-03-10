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
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d

cat < file2
## OUTPUT
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/219c84e6-dfa1-4731-94b6-f7c515a7a818)
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/47bee42d-2ce6-4070-a1ec-09446275c7de)

diff file1 file2
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/b4eefb2d-faf4-41a6-83cc-a7198e20246c)

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

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/43dce95b-432d-4a74-914d-ab12c1fa25fb)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/9e730d1e-f3d6-4b84-95b2-e5a0e767cc66)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/180c44e5-127c-4fa0-a658-a8a341145623)

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
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/1f731852-9a3c-48e7-b927-6d18fb617dc7)

grep hello newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/ac2d1277-85b8-4087-98f2-54c420a274ae)

grep -v hello newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/a6c4e2af-f796-47fb-8e9f-a654a0dca8d4)

cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/c226609d-ee9d-419a-be26-8eac062723e5)

cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/9e545756-4825-4bb3-a469-135c1bd625fe)

grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/d32ae7d5-398c-4b09-935c-7b906b1ae767)

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
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/1be4f29a-e72b-43a3-b5be-9d5105a7380d)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/88bf9486-3ded-4b07-8757-492b79dbfafb)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/4fe51f98-a29a-44b6-970d-2be4c7aa835f)

egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/303d470a-a395-4a64-bb38-2ae89f3e650a)

egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/e468d242-6a94-428b-8e07-9deb2c48b562)

egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/ca597094-acc1-4477-b0bc-852f6da7166b)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/7fc4cb5a-c98a-4abb-8adc-6375851631e0)

egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/d8ac34e4-828a-40fb-b53a-e4adf3d930af)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/1cc76366-b98b-4cbe-b692-c8010501ec0f)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/f781303c-6d13-40a6-bb9a-2a6e14c69a68)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/1277707d-b315-4e03-abcf-a88e6d48bb24)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/40ac8f96-903f-4c90-8044-a12e26aae0a2)


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
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/90d0d35a-83fb-400e-82bd-9340df721b89)

sed -n -e '$p' file23
## OUTPUT

sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/3766286a-ab3d-4967-aeff-2c770ebee982)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/4bed05e2-23f1-4376-b7c1-113bf3529664)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/774077c1-cfe2-4f74-93f8-d003b6a9f47e)

sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/87a2da81-1716-41d8-9f07-917a38a6674e)

sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/41b1fa1a-b3ee-43aa-93ed-612ee4bf949a)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/1b89ec7e-b239-4b24-9f9b-720f56a2a1d7)

seq 10 
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/1233f6c5-d211-404a-8e67-546863ed473d)

seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/66878a39-eb23-4a13-aaa3-6ccf6c2deb75)

seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/5a1808d9-9538-47ae-b060-4d94bba5b882)

seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/55deb2b9-4887-4bb5-86ac-0a9c73054bd3)

seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/c460881f-fd65-4a10-b0d2-89deedc6ef7c)

seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/c12b4421-46cd-41d8-95ee-edd53b11ab33)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/0d51cfca-a96d-4d3c-bdf2-35480c01275b)

sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/f4d129cb-f8e5-4de0-a23c-055763385805)

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
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/1b708d3b-3462-445a-9167-def23c89debd)

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
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/b57492a0-5542-423a-809f-d4df0f7250e0)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/2c14be45-1924-4b17-80f3-f68f2914043c)

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
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/683c6015-2585-41e5-92bb-ab3c37482cc3)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/cbbb3a93-541f-4c8c-bffc-69f74783d45d)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/narenm03/OS-Linux-commands-Shell-script/assets/152469427/111facf1-c81b-4fa4-a58a-76539531f740)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
tar -xvf backup.tar
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
##OUTPUT



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

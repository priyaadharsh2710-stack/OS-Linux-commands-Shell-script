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
 <img width="424" height="161" alt="image" src="https://github.com/user-attachments/assets/2df2a5f2-1693-4271-b8b6-58a3ec34fd8d" />



cat < file2
## OUTPUT
<img width="469" height="176" alt="image" src="https://github.com/user-attachments/assets/9fc0c7de-3009-4465-960c-1d2fb56c4c08" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="315" height="62" alt="image" src="https://github.com/user-attachments/assets/b45a117f-ac20-4d74-957d-a70f53ba542a" />

comm file1 file2
 ## OUTPUT
 <img width="470" height="218" alt="image" src="https://github.com/user-attachments/assets/a817d19e-b078-413c-b7f8-e0c62c636614" />

 
diff file1 file2
## OUTPUT
 <img width="460" height="280" alt="image" src="https://github.com/user-attachments/assets/5ed0e127-f060-46c9-b0b3-cb6aefd18228" />


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
<img width="471" height="108" alt="image" src="https://github.com/user-attachments/assets/a6f69113-4c66-4f88-b52b-b0c40e0431f0" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="320" height="105" alt="image" src="https://github.com/user-attachments/assets/bc3c1fbd-d7c8-4421-9728-b0aebc255ba8" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="317" height="97" alt="image" src="https://github.com/user-attachments/assets/0eea3db6-c1ef-43c8-b327-e064400566a2" />


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

 <img width="287" height="61" alt="image" src="https://github.com/user-attachments/assets/75986686-659c-4b76-ae28-77c01b97493b" />


grep hello newfile 
## OUTPUT
<img width="332" height="81" alt="image" src="https://github.com/user-attachments/assets/193b4f80-aeab-44d9-b918-aedd7a8c78df" />




grep -v hello newfile 
## OUTPUT
<img width="345" height="81" alt="image" src="https://github.com/user-attachments/assets/20a780de-d16d-4d67-8001-5bedc85ceb27" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="312" height="85" alt="image" src="https://github.com/user-attachments/assets/388c5d83-4528-4a29-bfe9-eb137c981773" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="452" height="520" alt="image" src="https://github.com/user-attachments/assets/818dd51f-9c9c-46ca-9bf5-c7f0857833f2" />



grep -R ubuntu /etc
## OUTPUT
<img width="352" height="101" alt="image" src="https://github.com/user-attachments/assets/44e83070-17bb-4c59-9220-c13cf1e77433" />



grep -w -n world newfile   
## OUTPUT


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
<img width="310" height="82" alt="image" src="https://github.com/user-attachments/assets/2f311bda-9e36-4076-a2e2-56243e51aca6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="386" height="100" alt="image" src="https://github.com/user-attachments/assets/5881e4ef-4258-432a-a9e1-bb6b8b212693" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="325" height="65" alt="image" src="https://github.com/user-attachments/assets/074e6002-6b1d-49ae-a56e-3dcb4dd13c1f" />



egrep '(^hello)' newfile 
## OUTPUT

 <img width="353" height="97" alt="image" src="https://github.com/user-attachments/assets/747a8809-193e-4eab-97a3-6d3f219ef1a1" />


egrep '(world$)' newfile 
## OUTPUT

<img width="301" height="65" alt="image" src="https://github.com/user-attachments/assets/d61f64c3-ccce-4d05-b511-8cb41bbad979" />


egrep '(World$)' newfile 
## OUTPUT

<img width="422" height="117" alt="image" src="https://github.com/user-attachments/assets/42e6b33b-a153-43a9-8ef4-09c744c1b7eb" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="355" height="60" alt="image" src="https://github.com/user-attachments/assets/710b37f0-162b-4840-b8d0-04af1251a206" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="345" height="62" alt="image" src="https://github.com/user-attachments/assets/ac7970f3-9dad-44cf-be8d-1ea0b7f6802a" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="372" height="65" alt="image" src="https://github.com/user-attachments/assets/de878881-fa45-43dc-aa6b-ab6cb99a4f78" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="372" height="82" alt="image" src="https://github.com/user-attachments/assets/8c5341bc-8e64-49cc-8aff-d1bfca136338" />

egrep l{2} newfile
## OUTPUT

<img width="431" height="103" alt="image" src="https://github.com/user-attachments/assets/9477d351-9a02-484c-b365-8cbf8b86f3b2" />


egrep 's{1,2}' newfile
## OUTPUT 


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

<img width="413" height="61" alt="image" src="https://github.com/user-attachments/assets/1a7cc186-9c32-4c95-a482-2751fb10f782" />


sed -n -e '$p' file23
## OUTPUT
<img width="366" height="61" alt="image" src="https://github.com/user-attachments/assets/13733fd3-2590-4fbd-bcc0-525bbada8c25" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="350" height="202" alt="image" src="https://github.com/user-attachments/assets/fbd42250-03ed-4ba5-8cba-6d4a69c0138f" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="397" height="197" alt="image" src="https://github.com/user-attachments/assets/5e6112bc-5c94-4a0c-a4de-7ef78b6e857b" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="388" height="201" alt="image" src="https://github.com/user-attachments/assets/a4158395-628a-4fa0-8380-94d226a1c9bd" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="352" height="162" alt="image" src="https://github.com/user-attachments/assets/3c9e3a1d-8c98-4760-af35-15895ca89bd3" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="403" height="102" alt="image" src="https://github.com/user-attachments/assets/2b70514b-0098-4fc0-88b1-27d2c539dc6a" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="350" height="78" alt="image" src="https://github.com/user-attachments/assets/14345e5d-3986-4935-995d-9153e78b3c0b" />


seq 10 
## OUTPUT
<img width="317" height="241" alt="image" src="https://github.com/user-attachments/assets/5fe6bab3-ff4d-4add-8913-1fff716d38e7" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="335" height="98" alt="image" src="https://github.com/user-attachments/assets/5845c331-fb18-418a-b012-c988d208f823" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="315" height="101" alt="image" src="https://github.com/user-attachments/assets/7fb846c7-6e45-40fd-9016-bcd57bafb59a" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="363" height="120" alt="image" src="https://github.com/user-attachments/assets/e03326e1-735d-4916-9e5b-794ba39b26d5" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="317" height="105" alt="image" src="https://github.com/user-attachments/assets/10303921-6279-45e0-acee-821ddbf2434c" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="317" height="101" alt="image" src="https://github.com/user-attachments/assets/6de511ee-f32b-4f85-a74c-cfc6aadec1a3" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="367" height="100" alt="image" src="https://github.com/user-attachments/assets/a7e4ea52-2858-4b1c-ba5e-2dbba829c085" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="363" height="103" alt="image" src="https://github.com/user-attachments/assets/e25bcb26-febb-4090-a009-2ca00e9a4be0" />

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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
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

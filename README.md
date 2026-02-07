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
<img width="341" height="102" alt="image" src="https://github.com/user-attachments/assets/5b52858f-207a-449e-88be-eaaf132ee95b" />



cat < file2
## OUTPUT
<img width="328" height="162" alt="image" src="https://github.com/user-attachments/assets/a1160cc6-d890-4d35-9416-ec32dd6adcff" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/a9a1e0bd-12e7-4178-bc48-3270daec9997" />

 
comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="image" src="https://github.com/user-attachments/assets/0ce02bd7-694f-48c9-9376-7d32ae8abbb9" />

 
diff file1 file2
## OUTPUT
<img width="428" height="305" alt="image" src="https://github.com/user-attachments/assets/b3a75a85-da7f-4ed7-bd2b-9acedf74cd89" />


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
<img width="383" height="84" alt="image" src="https://github.com/user-attachments/assets/3db85cf0-b3ff-4098-8f58-68b2c97b4d73" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="433" height="109" alt="image" src="https://github.com/user-attachments/assets/ad0fcd31-afb6-47d8-8dd4-2b80a2715105" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="110" alt="image" src="https://github.com/user-attachments/assets/5b1afbc0-d961-40f8-a53e-30f45e88ba1c" />


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
<img width="409" height="56" alt="image" src="https://github.com/user-attachments/assets/dd345d85-fca3-4ace-b39e-37c9f6e6b081" />



grep hello newfile 
## OUTPUT
<img width="400" height="58" alt="image" src="https://github.com/user-attachments/assets/99d71c26-502b-48c5-83d6-d873ab8d676b" />




grep -v hello newfile 
## OUTPUT
<img width="430" height="59" alt="image" src="https://github.com/user-attachments/assets/b8420a88-9c1f-40ff-845c-5b20eae265f4" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="546" height="81" alt="image" src="https://github.com/user-attachments/assets/35144211-f0bb-4024-be1c-4d7725112c41" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="578" height="52" alt="image" src="https://github.com/user-attachments/assets/d3b3b5d5-b788-469e-ad35-dc39a2f08e44" />




grep -R ubuntu /etc
## OUTPUT
<img width="609" height="218" alt="image" src="https://github.com/user-attachments/assets/461e5e3e-045d-4f1e-9b1b-3087473b92aa" />



grep -w -n world newfile   
## OUTPUT

<img width="474" height="80" alt="image" src="https://github.com/user-attachments/assets/d081f480-05d7-4ca0-b2c2-22f9232cd549" />

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
<img width="563" height="78" alt="image" src="https://github.com/user-attachments/assets/88d6ce81-4aec-4ec5-9bf8-cb3b14a1b3b5" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/ac3f77a3-205c-48c4-ab58-abb6d881af98" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/8979bd0b-10dd-4586-9899-3b15c7eddec4" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="489" height="58" alt="image" src="https://github.com/user-attachments/assets/7a5d0954-c680-42ea-9289-a62ff875aad9" />



egrep '(world$)' newfile 
## OUTPUT
<img width="495" height="54" alt="image" src="https://github.com/user-attachments/assets/397a450d-6027-43f8-8e31-66735e9d5103" />



egrep '(World$)' newfile 
## OUTPUT
<img width="485" height="49" alt="image" src="https://github.com/user-attachments/assets/2c8df0b5-5d3b-40e9-bc35-395f89aa9933" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="559" height="76" alt="image" src="https://github.com/user-attachments/assets/92cccd0c-43a3-4950-9dec-0430ff3886c6" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="475" height="62" alt="image" src="https://github.com/user-attachments/assets/8090d1ba-8dc7-48a2-b44b-c9ed09477c7c" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="547" height="55" alt="image" src="https://github.com/user-attachments/assets/e55fa551-3cd6-48f3-8887-b49a8aa9a7a3" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="540" height="57" alt="image" src="https://github.com/user-attachments/assets/521c1586-ef0c-4207-bfbd-aed10e1c0294" />


egrep l{2} newfile
## OUTPUT
<img width="549" height="76" alt="image" src="https://github.com/user-attachments/assets/a5e47313-8e94-4382-bfa5-ebc00a676c8c" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="116" alt="image" src="https://github.com/user-attachments/assets/d85bc9eb-6e70-4717-b3ab-5f0fc6b9d179" />


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
<img width="446" height="52" alt="image" src="https://github.com/user-attachments/assets/f5100a42-8f1d-40e4-8556-aee9eeabd63f" />



sed -n -e '$p' file23
## OUTPUT
<img width="463" height="58" alt="image" src="https://github.com/user-attachments/assets/aa852c1f-2000-455a-aab9-7a1e88e4f9d6" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="520" height="243" alt="image" src="https://github.com/user-attachments/assets/e8fbdebd-207c-4969-8275-c9a5a9f4e817" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="521" height="237" alt="image" src="https://github.com/user-attachments/assets/de2aac46-f320-4866-8a06-44a657a479ae" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="555" height="245" alt="image" src="https://github.com/user-attachments/assets/766a29f5-5ea1-4f2c-9375-061002014fa5" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="481" height="169" alt="image" src="https://github.com/user-attachments/assets/53295913-7801-4913-86b2-60c347101b0e" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="520" height="108" alt="image" src="https://github.com/user-attachments/assets/3879888c-ef0e-48ac-928d-dc3665e93aaf" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/6082bc35-2566-4d2d-91a7-b4c14d1dcac3" />



seq 10 
## OUTPUT

<img width="470" height="241" alt="image" src="https://github.com/user-attachments/assets/7dcc2d24-0771-4884-9f5e-31ef344d9b80" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/6fa69641-7ce8-4adf-96bc-d56078831feb" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/32e93296-70a2-44ae-aba1-7b18c6a99ca1" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="476" height="116" alt="image" src="https://github.com/user-attachments/assets/ca819df8-4772-48c0-9a64-0953e6fe7c9c" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/ddafc1ad-48db-450b-b4f6-425fb93b4376" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/9a5b747c-ee28-4a18-a7a0-d5ec8af966c5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="542" height="102" alt="image" src="https://github.com/user-attachments/assets/08804d07-924c-4b3b-9625-2fe25771cf43" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="565" height="112" alt="image" src="https://github.com/user-attachments/assets/94d1985d-c124-454f-a6b4-1c208aaf9248" />


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

<img width="343" height="156" alt="image" src="https://github.com/user-attachments/assets/d1c6a3cb-1acf-40e7-b154-56b9fc8b2bb4" />


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

<img width="363" height="160" alt="image" src="https://github.com/user-attachments/assets/8bfe5082-fbd3-4899-a9e3-afff37cd1e46" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT

<img width="652" height="243" alt="image" src="https://github.com/user-attachments/assets/3ebf1c6a-e041-451d-896d-062786c61b47" />

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

![Image1](https://github.com/user-attachments/assets/0154c46c-d7cb-4bd9-a947-b7b514245de1)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image 2](https://github.com/user-attachments/assets/edd50040-4f2f-44c4-9051-b54f9782b2e4)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image 3](https://github.com/user-attachments/assets/a205f4ca-4428-4b21-96e8-9fa52c74bfe1)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![image 3](https://github.com/user-attachments/assets/a205f4ca-4428-4b21-96e8-9fa52c74bfe1)


tar -xvf backup.tar
## OUTPUT

![image 4](https://github.com/user-attachments/assets/9117deaf-e64c-4ffd-8778-96cd437b228d)

gzip backup.tar

ls .gz
## OUTPUT

![image 8](https://github.com/user-attachments/assets/9f2693fc-3408-4de0-8456-fa0bbfde0f16)
 
gunzip backup.tar.gz
## OUTPUT

![image 7](https://github.com/user-attachments/assets/b6216f29-f59a-4043-bfc4-ed61091789ed)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image 6](https://github.com/user-attachments/assets/6f455798-de9b-4413-a3ff-ee45db1316cc)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/8f062ba5-bd8f-4218-b794-179d4a19ab04" />


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
<img width="430" height="331" alt="image" src="https://github.com/user-attachments/assets/b36e6eb3-3d88-4e9c-a682-991fcbd80f4c" />

 
ls file1
##OUTPUT
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/c06aee84-a165-4eea-bc4c-a728fa76b5f3" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/1f0244f7-2a5d-41b9-8a46-6f75741ce9b5" />
 

echo $?
## OUTPUT 

<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/c71f8516-4895-481e-8727-b7faec2d47d8" />
 
abcd
 
echo $?
 ## OUTPUT

<img width="469" height="221" alt="image" src="https://github.com/user-attachments/assets/2f676427-536b-4922-bea9-82b3f48ec48b" />

 
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

<img width="476" height="243" alt="image" src="https://github.com/user-attachments/assets/0c1c3575-f77a-47c1-a7f1-7ed1371bf77d" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="725" height="222" alt="image" src="https://github.com/user-attachments/assets/3bff51df-2b03-42d4-b024-39a9d24967f3" />


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

<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/b34eced0-ba5a-4a45-bdc5-c29d6ecbb2fc" />

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


<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/8fbdc6b8-0beb-47c9-820f-e8614bef708e" />



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

<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/5e91c160-cec2-453b-a3c1-5a76df12cdf4" />

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

<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/25fcf6e3-632e-40c9-9aa3-3f30798f1b19" />

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

<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/22bac222-ed45-4f5f-ab2b-959f9f7f6de3" />


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

<img width="541" height="248" alt="image" src="https://github.com/user-attachments/assets/909ea603-6bfa-47f7-b0f4-bac024b7363e" />

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
<img width="504" height="160" alt="image" src="https://github.com/user-attachments/assets/2f025cd8-2e8a-44a3-9afd-c2944c41b23d" />

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
<img width="446" height="201" alt="image" src="https://github.com/user-attachments/assets/17d2dab3-1f52-4ec2-8e2c-8ecfa7a2f3d4" />


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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/cb854902-9814-4294-b622-f0e4d13de187" />

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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/dd1b6697-ec63-4ecd-8cc5-f4e5e7cb81d9" />

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
<img width="412" height="201" alt="image" src="https://github.com/user-attachments/assets/a6fd6363-d7c4-49db-b80f-bab7f307ed16" />

 
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

![image 9](https://github.com/user-attachments/assets/6eac4ac0-78fd-4917-ac91-9e5f6177651c)


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
<img width="756" height="275" alt="image" src="https://github.com/user-attachments/assets/4c4614e2-8aeb-4e05-b7ac-1309827c4647" />
 
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
<img width="481" height="144" alt="image" src="https://github.com/user-attachments/assets/f3cf3687-350b-45bf-8868-57e060bf9188" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="774" height="137" alt="image" src="https://github.com/user-attachments/assets/52edc223-ac96-4f80-8338-662d89d3f60e" />



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
 
 <img width="755" height="44" alt="image" src="https://github.com/user-attachments/assets/1def3f35-346d-4436-bfd4-39bda2d7f3de" />

 
./funcex.sh 1 2

<img width="762" height="38" alt="image" src="https://github.com/user-attachments/assets/b5c63f26-7ca4-4011-9925-8362d47253b8" />

 
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
<img width="758" height="63" alt="image" src="https://github.com/user-attachments/assets/55224fbb-8f5f-4580-9326-7bf62889542e" />

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
<img width="762" height="87" alt="image" src="https://github.com/user-attachments/assets/777470e3-5298-4b45-96fb-8ca42fe97253" />

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
<img width="765" height="327" alt="image" src="https://github.com/user-attachments/assets/cae85762-59a1-4647-898c-33472e3b69ff" />
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
<img width="783" height="218" alt="image" src="https://github.com/user-attachments/assets/e79f133f-1dc7-4436-b5ae-23c5aab77ccc" />
 
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
<img width="772" height="70" alt="image" src="https://github.com/user-attachments/assets/84a912a6-e8d7-41b1-8741-a8d5cb89b06a" />


# RESULT:
The Commands are executed successfully.

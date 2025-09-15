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

<img width="572" height="99" alt="Screenshot from 2025-09-13 19-12-17" src="https://github.com/user-attachments/assets/414aa9bb-de82-45f4-9ee7-9cc78a751f1a" />


cat < file2
## OUTPUT
<img width="475" height="109" alt="Screenshot from 2025-09-13 19-14-39" src="https://github.com/user-attachments/assets/97d701f2-38b1-41ad-9db0-aa1f2a87949c" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="500" height="49" alt="Screenshot from 2025-09-13 19-15-42" src="https://github.com/user-attachments/assets/01916510-f96c-4e56-8d32-94a15657cb77" />

comm file1 file2
 ## OUTPUT

 <img width="493" height="156" alt="Screenshot from 2025-09-13 19-16-53" src="https://github.com/user-attachments/assets/55b7ec2c-73cb-4716-89a5-18b537b5bf67" />

diff file1 file2
## OUTPUT

<img width="616" height="194" alt="Screenshot from 2025-09-13 19-17-35" src="https://github.com/user-attachments/assets/1c5443df-dd62-41e6-9438-5d12fed7b0fc" />

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

<img width="526" height="65" alt="Screenshot from 2025-09-13 19-22-25" src="https://github.com/user-attachments/assets/8a9f7151-7f98-4dfa-a0fc-66ac20083c93" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="510" height="67" alt="Screenshot from 2025-09-13 19-23-50" src="https://github.com/user-attachments/assets/649bb704-57ea-48ba-947d-18350c4bda3d" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="515" height="50" alt="Screenshot from 2025-09-13 19-24-15" src="https://github.com/user-attachments/assets/6a08db87-9dd2-4bd5-930d-52692d084d5c" />


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

<img width="533" height="50" alt="Screenshot from 2025-09-13 19-25-07" src="https://github.com/user-attachments/assets/31c6c7f9-3b80-4d9d-a55b-0b3fcfc67b36" />


grep hello newfile 
## OUTPUT


<img width="601" height="50" alt="Screenshot from 2025-09-13 19-26-15" src="https://github.com/user-attachments/assets/ceca6181-5338-4b8c-8f54-4d78ce3b0c66" />


grep -v hello newfile 
## OUTPUT

<img width="623" height="50" alt="Screenshot from 2025-09-13 19-27-39" src="https://github.com/user-attachments/assets/8e899fcc-8468-4b4d-8faa-26d0b4d761f0" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="847" height="375" alt="Screenshot from 2025-09-13 19-29-37" src="https://github.com/user-attachments/assets/dd399fef-e94a-4b40-a814-1b14fc81bc46" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="583" height="64" alt="Screenshot from 2025-09-13 19-30-15" src="https://github.com/user-attachments/assets/20f512cb-fd8c-45d0-96e1-e954fbb296d9" />


grep -R ubuntu /etc
## OUTPUT

<img width="631" height="87" alt="Screenshot from 2025-09-13 19-34-09" src="https://github.com/user-attachments/assets/d3882f8d-61f3-47a6-b375-572407e80710" />


grep -w -n world newfile   
## OUTPUT
<img width="642" height="87" alt="Screenshot from 2025-09-13 19-35-22" src="https://github.com/user-attachments/assets/d86f53d3-e8e0-44af-a5ff-f544fed70783" />


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

<img width="577" height="50" alt="Screenshot from 2025-09-13 19-36-18" src="https://github.com/user-attachments/assets/7dbac8ce-069d-46fb-a02e-63b0fbd2530b" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="577" height="50" alt="Screenshot from 2025-09-13 19-37-04" src="https://github.com/user-attachments/assets/33b9acc7-5a29-4ade-8b13-d0d9b27a18c0" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="619" height="65" alt="Screenshot from 2025-09-13 19-38-12" src="https://github.com/user-attachments/assets/979ad6ce-eb61-4c2a-a530-c58c5808f7d5" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="619" height="47" alt="Screenshot from 2025-09-13 19-38-46" src="https://github.com/user-attachments/assets/bfbc0651-5ee6-41e8-b8d6-e34a6cd3eb96" />


egrep '(world$)' newfile 
## OUTPUT

<img width="619" height="47" alt="Screenshot from 2025-09-13 19-39-35" src="https://github.com/user-attachments/assets/58b8faeb-c4d9-47d1-a84c-3b7a42ad6cf0" />


egrep '(World$)' newfile 
## OUTPUT

<img width="619" height="47" alt="Screenshot from 2025-09-13 19-44-23" src="https://github.com/user-attachments/assets/d932a49c-058c-407e-84cc-ced59ffc5bd9" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="626" height="62" alt="Screenshot from 2025-09-13 19-45-16" src="https://github.com/user-attachments/assets/ab2b577c-8515-464a-be16-55d51d05d794" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="622" height="79" alt="Screenshot from 2025-09-13 19-46-03" src="https://github.com/user-attachments/assets/3a5e79a8-b834-46f2-b4ec-a31b0d110ed4" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="622" height="45" alt="Screenshot from 2025-09-13 19-49-33" src="https://github.com/user-attachments/assets/2c90826d-8390-4c93-b64c-ece83559e063" />

egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT

<img width="622" height="45" alt="Screenshot from 2025-09-13 19-50-10" src="https://github.com/user-attachments/assets/18057a7e-2deb-4063-8ffc-cd5abf4d62ae" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="623" height="154" alt="Screenshot from 2025-09-13 19-51-09" src="https://github.com/user-attachments/assets/9bd6c3bb-5497-4d5c-b900-d82e05cdfdc2" />

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

<img width="623" height="154" alt="Screenshot from 2025-09-13 19-51-55" src="https://github.com/user-attachments/assets/ed227d72-b017-4fd7-8e4d-53b3c467bbac" />


sed -n -e '$p' file23
## OUTPUT

<img width="623" height="154" alt="Screenshot from 2025-09-13 19-52-36" src="https://github.com/user-attachments/assets/e1ce3696-8912-4129-bfee-1fb6957e00cf" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="614" height="119" alt="Screenshot from 2025-09-13 19-53-15" src="https://github.com/user-attachments/assets/e396ced4-7c0d-41a8-ab8b-415170781c15" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="616" height="84" alt="Screenshot from 2025-09-13 19-54-12" src="https://github.com/user-attachments/assets/b6aa9418-0a3e-4948-a520-ce33e888caff" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="639" height="66" alt="Screenshot from 2025-09-13 19-55-03" src="https://github.com/user-attachments/assets/1e71cf97-05b5-494f-8521-745dce9d36df" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="590" height="209" alt="Screenshot from 2025-09-13 19-55-26" src="https://github.com/user-attachments/assets/75d732e1-764f-4c80-9604-09a4cde16b4a" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="564" height="83" alt="Screenshot from 2025-09-13 19-56-08" src="https://github.com/user-attachments/assets/94ccca24-f1ab-4330-9b14-7faf166fad61" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="564" height="83" alt="Screenshot from 2025-09-13 19-58-03" src="https://github.com/user-attachments/assets/3565e695-b31a-4986-84dd-98b10be69585" />


seq 10 
## OUTPUT

<img width="576" height="101" alt="Screenshot from 2025-09-13 19-58-33" src="https://github.com/user-attachments/assets/91064c47-ec65-4dc6-b710-8b3e38a42f2f" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="576" height="83" alt="Screenshot from 2025-09-13 19-59-15" src="https://github.com/user-attachments/assets/6c2c1e46-703a-4113-b892-f16c92f4ffc8" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="576" height="83" alt="Screenshot from 2025-09-13 19-59-57" src="https://github.com/user-attachments/assets/2a9d35dd-ad0a-4c90-822c-644abdedfbf5" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="576" height="83" alt="Screenshot from 2025-09-13 20-00-47" src="https://github.com/user-attachments/assets/49496ca8-bae7-4611-86b7-aaa40fc45cd6" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="576" height="83" alt="Screenshot from 2025-09-13 20-01-37" src="https://github.com/user-attachments/assets/2d7268c4-d686-4edd-9ed3-ec0affe752fc" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="583" height="119" alt="Screenshot from 2025-09-13 20-05-23" src="https://github.com/user-attachments/assets/59d2e4ae-56d9-4259-ac1b-58f0c0e1230d" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="678" height="150" alt="Screenshot from 2025-09-13 20-09-20" src="https://github.com/user-attachments/assets/92d57728-5d89-4fd2-88f8-4a33213799f5" />


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
<img width="615" height="80" alt="Screenshot from 2025-09-13 20-12-47" src="https://github.com/user-attachments/assets/f5ac58b1-54ed-4afc-ba27-bc804743e759" />


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
<img width="692" height="80" alt="Screenshot from 2025-09-13 20-13-50" src="https://github.com/user-attachments/assets/fcc19e58-8b03-4d73-88e9-8f0cbc900b5e" />

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

<img width="666" height="367" alt="Screenshot from 2025-09-13 20-16-08" src="https://github.com/user-attachments/assets/017581ec-2f59-4121-b105-2a5995230473" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="666" height="367" alt="Screenshot from 2025-09-14 21-20-44" src="https://github.com/user-attachments/assets/37d69223-7f07-492e-ab7e-832af474abd9" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="666" height="367" alt="Screenshot from 2025-09-14 21-21-47" src="https://github.com/user-attachments/assets/196c0440-6539-4735-ba06-4e32c5ac028d" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="590" height="65" alt="Screenshot from 2025-09-14 21-24-24" src="https://github.com/user-attachments/assets/54cf184c-b68f-43c7-8a9e-650ba1660e6a" />


tar -xvf backup.tar
## OUTPUT
<img width="1631" height="136" alt="Screenshot from 2025-09-14 21-25-51" src="https://github.com/user-attachments/assets/fb799104-0e69-4424-9d32-1a9477867c11" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 <img width="729" height="80" alt="Screenshot from 2025-09-14 22-42-47" src="https://github.com/user-attachments/assets/0fe4784e-3d0f-4995-9250-2b98c3a78356" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="616" height="218" alt="Screenshot from 2025-09-14 22-44-55" src="https://github.com/user-attachments/assets/b5c28239-76cd-4fbf-b6d3-6c1dfdd8268e" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="611" height="563" alt="Screenshot from 2025-09-14 22-53-54" src="https://github.com/user-attachments/assets/dfba6bd7-d4e8-41aa-a5af-db5e8a29d29d" />

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
<img width="445" height="54" alt="Screenshot from 2025-09-14 22-59-04" src="https://github.com/user-attachments/assets/9d1c5653-2e7f-447a-8e1e-68e586a57dee" />

echo $?
## OUTPUT 

<img width="436" height="50" alt="Screenshot from 2025-09-14 22-59-40" src="https://github.com/user-attachments/assets/c4a66e70-2e3d-4d76-8472-e1bc562ada1d" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="411" height="151" alt="Screenshot from 2025-09-14 23-00-08" src="https://github.com/user-attachments/assets/e68bd2ff-b658-4e3d-9cfc-241a4e49f41e" />

abcd
 
echo $?
 ## OUTPUT

<img width="517" height="184" alt="Screenshot from 2025-09-14 23-03-51" src="https://github.com/user-attachments/assets/ea598188-127b-4534-9801-179d9b696c43" />

 
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



<img width="590" height="61" alt="Screenshot from 2025-09-14 23-04-42" src="https://github.com/user-attachments/assets/5104010a-6a9c-43ec-9c9e-5eb45422be0e" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="561" height="189" alt="Screenshot from 2025-09-14 23-09-17" src="https://github.com/user-attachments/assets/793b4e07-02c9-4d34-aa69-37ebdd1e528a" />

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



<img width="619" height="402" alt="Screenshot from 2025-09-14 23-16-24" src="https://github.com/user-attachments/assets/b4a6744b-88c2-4e1f-97e1-2993f2534a11" />


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

<img width="619" height="402" alt="Screenshot from 2025-09-14 23-25-15" src="https://github.com/user-attachments/assets/c4213f9a-8c68-4417-b9d8-7738f9c56e2b" />


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

<img width="627" height="241" alt="Screenshot from 2025-09-14 23-29-57" src="https://github.com/user-attachments/assets/f08a1af9-25c6-43a6-9564-f8f73af386c7" />



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

<img width="645" height="299" alt="Screenshot from 2025-09-14 23-36-55" src="https://github.com/user-attachments/assets/5ac8d998-5858-48e3-8f47-44613cfb8950" />



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


<img width="665" height="420" alt="Screenshot from 2025-09-14 23-42-46" src="https://github.com/user-attachments/assets/f731bec0-5879-4d68-83e2-827a36832913" />



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


<img width="665" height="420" alt="Screenshot from 2025-09-14 23-46-14" src="https://github.com/user-attachments/assets/2152a7a0-cf93-4a9b-b742-6e73aa2c14c0" />




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
 <img width="665" height="420" alt="Screenshot from 2025-09-14 23-46-14" src="https://github.com/user-attachments/assets/528d144a-e2fe-400a-a552-27f1c3b1f388" />

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
 <img width="655" height="331" alt="Screenshot from 2025-09-14 23-49-13" src="https://github.com/user-attachments/assets/03f57956-aee8-4089-a6ad-4e170df82f8e" />

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
 <img width="645" height="276" alt="Screenshot from 2025-09-14 23-53-01" src="https://github.com/user-attachments/assets/b588d8ba-68f7-4777-a4c4-e824709e0c3a" />

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
 <img width="644" height="369" alt="Screenshot from 2025-09-14 23-56-19" src="https://github.com/user-attachments/assets/0c47e6e7-4765-45be-ab23-d63cd8941553" />

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

<img width="642" height="512" alt="Screenshot from 2025-09-15 00-20-19" src="https://github.com/user-attachments/assets/318a13ad-38aa-4034-90ef-d6e615547bfc" />

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
<img width="642" height="512" alt="Screenshot from 2025-09-15 00-20-19" src="https://github.com/user-attachments/assets/60a4a147-8a57-4a8c-83d9-9c0142abb4bf" />


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

<img width="634" height="301" alt="Screenshot from 2025-09-15 00-23-39" src="https://github.com/user-attachments/assets/6215deb0-91d1-4d06-b201-044a4b1ef759" />

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

<img width="634" height="301" alt="Screenshot from 2025-09-15 00-27-17" src="https://github.com/user-attachments/assets/804f676f-3e92-4fbe-8493-093753c82425" />


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


 
<img width="632" height="257" alt="Screenshot from 2025-09-15 00-27-35" src="https://github.com/user-attachments/assets/d94c061a-ee1e-47a0-aa04-6c3591cb067f" />

 
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

<img width="640" height="489" alt="Screenshot from 2025-09-15 00-31-01" src="https://github.com/user-attachments/assets/1a440b93-17dc-40a0-887f-a03b3d0597c9" />


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

<img width="630" height="381" alt="Screenshot from 2025-09-15 00-34-24" src="https://github.com/user-attachments/assets/0cada64e-6317-49b7-bf25-097614fcb8e7" />

 
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
<img width="623" height="212" alt="Screenshot from 2025-09-15 00-37-24" src="https://github.com/user-attachments/assets/13e8a959-74dc-4193-b95f-84fa526b0848" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="604" height="198" alt="Screenshot from 2025-09-15 00-37-41" src="https://github.com/user-attachments/assets/29fd9b1b-7f66-4964-a0a9-757c696f9293" />


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


<img width="594" height="327" alt="Screenshot from 2025-09-15 00-42-07" src="https://github.com/user-attachments/assets/b4da144d-a515-4872-be89-db8d22731909" />

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

<img width="577" height="62" alt="Screenshot from 2025-09-15 00-42-40" src="https://github.com/user-attachments/assets/14b1c7ad-ad2c-461c-aedb-3b6ff9c0de4b" />


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

<img width="620" height="257" alt="Screenshot from 2025-09-15 00-46-23" src="https://github.com/user-attachments/assets/0a6e0de8-654c-4620-9e64-ef2463ee3f83" />

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

<img width="656" height="513" alt="Screenshot from 2025-09-15 00-49-19" src="https://github.com/user-attachments/assets/e3bccd6a-79e9-405b-b7b0-a766c9bc8949" />

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

<img width="624" height="329" alt="Screenshot from 2025-09-15 00-55-15" src="https://github.com/user-attachments/assets/bbbfbe02-0f7e-4398-9045-2967983cc1ff" />

 
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

<img width="624" height="329" alt="Screenshot from 2025-09-15 01-03-52" src="https://github.com/user-attachments/assets/806f8570-9e89-411f-a624-a5743fc7e2dd" />

# RESULT:
The Commands are executed successfully.

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
<img width="691" height="115" alt="image" src="https://github.com/user-attachments/assets/26862dfe-59a0-4889-8319-c334035c08c3" />
cat < file2
## OUTPUT
<img width="692" height="162" alt="image" src="https://github.com/user-attachments/assets/f7337cb5-ca7c-44ca-847d-292698f487f8" />
# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="541" height="47" alt="image" src="https://github.com/user-attachments/assets/daacc6fe-3cc5-4810-b1cd-d261af69eeea" />

comm file1 file2
## OUTPUT
<img width="570" height="207" alt="image" src="https://github.com/user-attachments/assets/844d33f4-1a2a-4a0c-81c9-efaa7261edc9" />

 
diff file1 file2
## OUTPUT
<img width="552" height="257" alt="image" src="https://github.com/user-attachments/assets/1ab25edc-8206-4456-8664-bc2bd3970a05" />


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
<img width="547" height="71" alt="image" src="https://github.com/user-attachments/assets/e6dd4523-42a7-4c0a-9e69-f8ec5b662c5c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="622" height="87" alt="image" src="https://github.com/user-attachments/assets/20cb21dd-f5b8-4693-8bad-3ec77bb63739" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="711" height="85" alt="image" src="https://github.com/user-attachments/assets/653a111d-8819-4d55-ad0f-5df8feba7777" />


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
<img width="662" height="41" alt="image" src="https://github.com/user-attachments/assets/c033cdb9-e9b8-4850-982a-b34e773b8a9d" />



grep hello newfile 
## OUTPUT

<img width="667" height="37" alt="image" src="https://github.com/user-attachments/assets/c4e858c2-d261-436d-8f9a-aeec9b916e90" />



grep -v hello newfile 
## OUTPUT

<img width="700" height="45" alt="image" src="https://github.com/user-attachments/assets/c619afd3-2254-4f64-b818-dae540a05471" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="808" height="67" alt="image" src="https://github.com/user-attachments/assets/26efc89d-9abb-4405-9a0a-b60f00e06f29" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="842" height="45" alt="image" src="https://github.com/user-attachments/assets/701cb1cf-ce8b-401e-b4ab-0ca330dcb99d" />




grep -R ubuntu /etc
## OUTPUT



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
<img width="808" height="65" alt="image" src="https://github.com/user-attachments/assets/d3070e23-6f30-452c-b226-681d45fed0f6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="776" height="65" alt="image" src="https://github.com/user-attachments/assets/6ffd97e6-5dc0-4c64-a79b-319f55ba1f4e" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="828" height="65" alt="image" src="https://github.com/user-attachments/assets/135c0cdd-9e8c-41a2-82eb-f1e23deb0fd6" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="733" height="42" alt="image" src="https://github.com/user-attachments/assets/7e8b5b65-3285-4642-8ce3-1263e52fa040" />


egrep '(world$)' newfile 
## OUTPUT

<img width="745" height="67" alt="image" src="https://github.com/user-attachments/assets/853d4fce-b05f-42da-a9fe-3aa4850ee2ae" />


egrep '(World$)' newfile 
## OUTPUT
<img width="732" height="42" alt="image" src="https://github.com/user-attachments/assets/b320cb9b-a108-4d71-a8f5-9056ab467c25" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="782" height="66" alt="image" src="https://github.com/user-attachments/assets/68cad66c-a8c8-4176-b660-30d33eed56a2" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="701" height="43" alt="image" src="https://github.com/user-attachments/assets/f7a866b8-8c0c-44b0-8f35-6aefc68f347c" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="777" height="42" alt="image" src="https://github.com/user-attachments/assets/69e873d8-e9a3-4d60-b83b-145b9cfed3df" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="785" height="45" alt="image" src="https://github.com/user-attachments/assets/ab4f22eb-b5f2-4c2c-903a-a22c6a138cba" />


egrep l{2} newfile
## OUTPUT
<img width="661" height="65" alt="image" src="https://github.com/user-attachments/assets/0f1eda6c-5083-4a57-972f-0970937192fa" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="711" height="87" alt="image" src="https://github.com/user-attachments/assets/4e2437b7-490c-4fe9-a1aa-cdd6f80426ad" />


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
<img width="700" height="47" alt="image" src="https://github.com/user-attachments/assets/924b6118-a0fc-40c3-bc71-60369b73150b" />



sed -n -e '$p' file23
## OUTPUT

<img width="697" height="50" alt="image" src="https://github.com/user-attachments/assets/3cd03458-0bbc-4935-92e1-19160615ae79" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="780" height="205" alt="image" src="https://github.com/user-attachments/assets/7ef66a32-da4e-45f7-9ef5-0ede968f024d" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="780" height="212" alt="image" src="https://github.com/user-attachments/assets/d6dd1669-c6f6-4e90-ac91-f793eaa9033a" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="806" height="207" alt="image" src="https://github.com/user-attachments/assets/04f97e83-fec9-4acc-b07a-a8d4ab969f11" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="717" height="137" alt="image" src="https://github.com/user-attachments/assets/c36eb84a-276a-482c-aee3-dd4979ddc934" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="770" height="90" alt="image" src="https://github.com/user-attachments/assets/3e33513d-9fc0-42d4-a1ea-3b45617bd6e6" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="817" height="67" alt="image" src="https://github.com/user-attachments/assets/47213c6c-1330-4477-a9c5-66efd46acf2b" />



seq 10 
## OUTPUT

<img width="521" height="260" alt="image" src="https://github.com/user-attachments/assets/f36ba71f-98ee-460c-9ee2-8e46cda6a948" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="706" height="90" alt="image" src="https://github.com/user-attachments/assets/09ab3642-a8d2-4670-9a69-08755f81c794" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="728" height="93" alt="image" src="https://github.com/user-attachments/assets/9925fc94-5deb-4cbf-95ef-707e07867d25" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="703" height="116" alt="image" src="https://github.com/user-attachments/assets/bf7e45a4-d057-4e0e-ae2b-f8836d4edfaa" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="707" height="90" alt="image" src="https://github.com/user-attachments/assets/408599cb-a51a-4c2c-9b08-ed6a25d488e5" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="742" height="93" alt="image" src="https://github.com/user-attachments/assets/30db2968-8295-4f56-bdfd-4fd358e1c049" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="795" height="95" alt="image" src="https://github.com/user-attachments/assets/403021e9-a0ae-4f34-a759-532df0fe677c" />



sed -n '2,4{s/$/*/;p}' file23
<img width="793" height="86" alt="image" src="https://github.com/user-attachments/assets/3453e741-4eb4-40e9-bd9e-518bfdef32fd" />


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
<img width="575" height="137" alt="image" src="https://github.com/user-attachments/assets/55c45b2e-1cab-4a2e-bfd4-a8a52344978a" />


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
<img width="585" height="137" alt="image" src="https://github.com/user-attachments/assets/320144d0-22b0-4619-ac24-d196c42a0deb" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="872" height="207" alt="image" src="https://github.com/user-attachments/assets/df0c51ad-8fb5-4f0a-bef1-b7eee9b9758e" />

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
<img width="768" height="91" alt="image" src="https://github.com/user-attachments/assets/ded148ab-bacd-49d2-aaaa-35a29fb5bf6f" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="916" height="87" alt="image" src="https://github.com/user-attachments/assets/75a64ed4-40de-4796-87be-a00d465ec823" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="708" height="205" alt="image" src="https://github.com/user-attachments/assets/08206e00-745f-46c7-a597-1bcd53afb4f3" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="810" height="212" alt="image" src="https://github.com/user-attachments/assets/1c33658a-c00d-43f6-9392-5209c0675d3c" />


tar -xvf backup.tar
## OUTPUT
<img width="803" height="210" alt="image" src="https://github.com/user-attachments/assets/d1f4bf1f-44f5-4113-bdbb-97bb6afa9104" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="651" height="50" alt="image" src="https://github.com/user-attachments/assets/75453f70-47ca-4fa5-8ca6-044e49a455c1" />

gunzip backup.tar.gz
## OUTPUT
<img width="801" height="72" alt="image" src="https://github.com/user-attachments/assets/0f101de4-83ed-478b-a764-5c110ef80670" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="903" height="131" alt="image" src="https://github.com/user-attachments/assets/3338d1c5-4cd8-4afc-a164-6cf4dba965d3" />
<img width="717" height="67" alt="image" src="https://github.com/user-attachments/assets/12d0ba68-432f-4207-bfed-3785e5765267" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="651" height="97" alt="image" src="https://github.com/user-attachments/assets/fd4c538d-dc3d-42c1-94af-9a97854f16fb" />


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
<img width="711" height="342" alt="image" src="https://github.com/user-attachments/assets/8511ec83-f5fc-4a0a-a137-795e95cd7fd5" />

 
ls file1
## OUTPUT
<img width="545" height="42" alt="image" src="https://github.com/user-attachments/assets/172b1b7a-ae9e-40a2-928f-ca00c8974a59" />

echo $?
## OUTPUT 
<img width="526" height="42" alt="image" src="https://github.com/user-attachments/assets/5c58b229-df44-4c13-a5ac-036e08e29103" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="552" height="142" alt="image" src="https://github.com/user-attachments/assets/24943441-9383-4963-b938-3a107a494e28" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="595" height="227" alt="image" src="https://github.com/user-attachments/assets/b385c2c4-3bc0-495a-ba3f-9f44619d0083" />


 
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
<img width="637" height="255" alt="image" src="https://github.com/user-attachments/assets/6c0ddf33-d826-44bb-97ee-4a7de27ae543" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="705" height="67" alt="image" src="https://github.com/user-attachments/assets/63936cc2-51fa-4efc-b2a3-c19b5ab5a21a" />


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
<img width="655" height="47" alt="image" src="https://github.com/user-attachments/assets/6ef740cf-46b7-4f43-9b7e-87619b84aa51" />

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

<img width="697" height="143" alt="image" src="https://github.com/user-attachments/assets/266c437a-6af3-47d4-941c-cf2d468400c2" />


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
<img width="710" height="116" alt="image" src="https://github.com/user-attachments/assets/2e3b35c0-9031-4d90-b723-2ceb4a88e2ce" />

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
<img width="710" height="71" alt="image" src="https://github.com/user-attachments/assets/d2261c4f-2720-4720-b9c6-f3ca1203510a" />


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
<img width="712" height="68" alt="image" src="https://github.com/user-attachments/assets/791b0578-6261-4515-bbd4-47b592064fff" />

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
<img width="707" height="66" alt="image" src="https://github.com/user-attachments/assets/09b2fced-f84c-4c79-9035-827d4f869d65" />
 
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
 <img width="707" height="282" alt="image" src="https://github.com/user-attachments/assets/b1e9025e-e42d-4d5a-9ecf-7e54612ab8d4" />

 
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
 <img width="710" height="135" alt="image" src="https://github.com/user-attachments/assets/79678de6-b2fb-4406-b2cc-3bcc612a36dc" />

 
 
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
 <img width="682" height="182" alt="image" src="https://github.com/user-attachments/assets/0205a2ab-d1a8-410a-aa9d-64721a718a44" />

 
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
 <img width="685" height="113" alt="image" src="https://github.com/user-attachments/assets/8660624d-ce0c-4969-a397-0c50aa55c6d8" />

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
<img width="801" height="100" alt="image" src="https://github.com/user-attachments/assets/b67efa68-eaa9-4a60-b5f1-7032a16003b8" />

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
<img width="675" height="227" alt="image" src="https://github.com/user-attachments/assets/29cea01c-a6e0-479f-aa57-f25217885373" />
<img width="720" height="242" alt="image" src="https://github.com/user-attachments/assets/9e62b94f-7b5e-42e0-af0b-3c9dd8eba278" />


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
<img width="707" height="197" alt="image" src="https://github.com/user-attachments/assets/0332a378-9ff6-4369-8d7f-793d914c901f" />

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
<img width="718" height="162" alt="image" src="https://github.com/user-attachments/assets/80b22b8d-db95-44a1-a880-6062375c0720" />

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
<img width="725" height="327" alt="image" src="https://github.com/user-attachments/assets/6b510e86-a912-4550-8171-8e44e91d7015" />

 
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
<img width="730" height="145" alt="image" src="https://github.com/user-attachments/assets/c5a4a853-cfb2-4c58-9e14-2586d061ac6c" />

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
 <img width="737" height="160" alt="image" src="https://github.com/user-attachments/assets/65b9952b-e20a-4e2d-8b8b-7b83a8c86969" />

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
<img width="673" height="117" alt="image" src="https://github.com/user-attachments/assets/ef75f2c0-8b2f-4c8f-97a0-f4ccefc803e4" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="700" height="112" alt="image" src="https://github.com/user-attachments/assets/5b87a0ef-ed8b-40bb-8a82-34e9d3de093f" />


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
 <img width="670" height="70" alt="image" src="https://github.com/user-attachments/assets/cecfd912-5c39-4b7e-af59-ca0f45a94793" />

 
 ./funcex.sh 1 2

 <img width="666" height="48" alt="image" src="https://github.com/user-attachments/assets/664f9ca5-70bf-4f4d-85ff-6414a0f0e6a6" />

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
 
 <img width="767" height="112" alt="image" src="https://github.com/user-attachments/assets/8065713a-fff3-43d6-93fc-4b8fcc79b022" />


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
 <img width="713" height="346" alt="image" src="https://github.com/user-attachments/assets/c0bea498-3b1d-49c0-8245-7e013033a5b7" />

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
<img width="713" height="145" alt="image" src="https://github.com/user-attachments/assets/5c92b6bb-080c-4d25-a5a4-09a60349ea86" />


# RESULT:
The Commands are executed successfully.

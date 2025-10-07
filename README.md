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

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d

cat > file2

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d

### Display the content of the files
cat < file1
## OUTPUT
<img width="578" height="100" alt="image" src="https://github.com/user-attachments/assets/2b7ec286-4562-4cb8-8f8d-7cb9961ea810" />




cat < file2
## OUTPUT
<img width="578" height="118" alt="image" src="https://github.com/user-attachments/assets/a5c3c323-4ad5-45db-86e1-037dba7ddf7a" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="578" height="42" alt="image" src="https://github.com/user-attachments/assets/03915b76-5073-4965-a357-e3979e8b8cac" />
 
comm file1 file2
 ## OUTPUT
<img width="527" height="167" alt="image" src="https://github.com/user-attachments/assets/079539e7-8ee5-466d-beff-2a664185a734" />

 
diff file1 file2
## OUTPUT
<img width="527" height="181" alt="image" src="https://github.com/user-attachments/assets/30e3d224-ec0f-4ffa-8758-486e33513620" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11

Hello world
This is my world
^d

cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d



cut -c1-3 file11
## OUTPUT
<img width="527" height="58" alt="image" src="https://github.com/user-attachments/assets/cc74175e-79cf-4f9b-b062-bdf9f90484f7" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="553" height="78" alt="image" src="https://github.com/user-attachments/assets/5b64693c-6a6b-459e-b94a-3aaaf79d2c13" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="553" height="78" alt="image" src="https://github.com/user-attachments/assets/2255281f-0715-4dda-bbc6-f95bce2cad6e" />


cat < newfile 

Hello world
hello world
^d
`
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="553" height="42" alt="image" src="https://github.com/user-attachments/assets/e92a7280-81de-4aa5-b4ed-934846877f8a" />



grep hello newfile 
## OUTPUT
<img width="553" height="42" alt="image" src="https://github.com/user-attachments/assets/c078335f-76a7-4bd9-b354-9268923ba0f8" />




grep -v hello newfile 
## OUTPUT
<img width="553" height="42" alt="image" src="https://github.com/user-attachments/assets/49902f25-8aa4-49f8-9378-a9e361c9a1db" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="613" height="63" alt="image" src="https://github.com/user-attachments/assets/cb826d60-19a9-4ec0-97a0-1e6755689050" />




cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT
<img width="920" height="326" alt="image" src="https://github.com/user-attachments/assets/695c5f27-3b9d-4efe-b662-e9ce42009fc5" />



grep -w -n world newfile   
## OUTPUT
<img width="610" height="57" alt="image" src="https://github.com/user-attachments/assets/70ce0a10-b96b-49e1-934b-985cd852f15e" />


cat < newfile 

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d


cat > newfile

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="627" height="63" alt="image" src="https://github.com/user-attachments/assets/4c32304a-8969-4268-8dde-50d7409ccc38" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="643" height="60" alt="image" src="https://github.com/user-attachments/assets/1093d957-3201-4c03-bfa1-21f67e6e2677" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="643" height="60" alt="image" src="https://github.com/user-attachments/assets/1d5054d5-1739-42fa-88a3-e1d963abc71a" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="643" height="47" alt="image" src="https://github.com/user-attachments/assets/f2531196-4fa1-442e-804f-a1acee8b6e46" />



egrep '(world$)' newfile 
## OUTPUT
<img width="643" height="59" alt="image" src="https://github.com/user-attachments/assets/2cba11ce-e149-4c45-8520-1a37c2f1838f" />



egrep '(World$)' newfile 
## OUTPUT
<img width="643" height="42" alt="image" src="https://github.com/user-attachments/assets/184f34e7-7034-497f-82e6-ca69a8ea33ee" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="643" height="76" alt="image" src="https://github.com/user-attachments/assets/16839798-c3a9-4a87-a484-04c9e1a8bae0" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="643" height="47" alt="image" src="https://github.com/user-attachments/assets/4eea361b-6c85-425b-81cb-e7885bbc5d8e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="643" height="45" alt="image" src="https://github.com/user-attachments/assets/26e58216-2c90-42b1-a366-e69fb3d6ae46" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="643" height="45" alt="image" src="https://github.com/user-attachments/assets/4a2ccda4-2833-47e1-84ff-4278b857f42a" />


egrep l{2} newfile
## OUTPUT
<img width="643" height="57" alt="image" src="https://github.com/user-attachments/assets/50733e67-f0f4-424b-8f2b-6b0c378e998f" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="643" height="75" alt="image" src="https://github.com/user-attachments/assets/c0737797-ca5f-49c7-ad41-7eb09e7863a9" />


cat > file23

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d



sed -n -e '3p' file23
## OUTPUT
<img width="643" height="46" alt="481358094-01eea23e-2b38-4e42-a3d4-0250fab300b0" src="https://github.com/user-attachments/assets/6340777d-1ae9-4be4-bfc1-13ac1aa978af" />



sed -n -e '$p' file23
## OUTPUT
<img width="643" height="39" alt="481358099-64359668-d6fd-457b-9f17-a49ce6bdbe32" src="https://github.com/user-attachments/assets/81d63883-19df-4b7c-8258-42fc3a0fe8d4" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="643" height="169" alt="481358104-2865290b-ab37-434e-8738-6d4cfd81c03c" src="https://github.com/user-attachments/assets/56aea506-52fa-4863-85c0-3478d1c4e685" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="643" height="169" alt="481358108-18748a9c-ac3d-4279-adb1-447a5733cdcd" src="https://github.com/user-attachments/assets/03d9caf3-50f8-4fd0-b608-dcf2f710ff58" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="643" height="169" alt="481358115-bc4984d3-3ff6-49a6-ac68-f4d0238dd056" src="https://github.com/user-attachments/assets/22810b7a-860e-4737-849a-a30a8b43ebf0" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="643" height="113" alt="481358122-3b210678-1494-4519-9c69-b7986d2e7778" src="https://github.com/user-attachments/assets/160a9873-e111-442c-adc9-8476d04365dd" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="643" height="77" alt="481358127-de770e0d-90c9-4d36-8749-b7ee850cd12a" src="https://github.com/user-attachments/assets/ad5db05d-bed7-4f8b-95c9-bf5704fe90df" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="643" height="60" alt="481358135-f430b640-1c02-4d6e-9b71-499855710b79" src="https://github.com/user-attachments/assets/6780ef1d-4078-41ce-a75f-a3fc20b4f4e8" />


seq 10 
## OUTPUT

<img width="643" height="203" alt="481358140-0b32dbc5-0848-4c19-b5b7-dc97b838f1bc" src="https://github.com/user-attachments/assets/6712c6bc-0980-4e16-bf62-6821e482717c" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="643" height="75" alt="481358143-a7d31636-da34-4669-ae29-95e235fa563d" src="https://github.com/user-attachments/assets/0093092f-486e-4cc8-82bb-338d2aab6633" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="643" height="75" alt="481358149-1f7c1b0f-5e9b-4053-8deb-0b0ceb6d590f" src="https://github.com/user-attachments/assets/f6068dd4-72b0-4441-8fb5-5c28beb00265" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="643" height="94" alt="481358154-85a491b8-562e-4705-96f8-948e5791fd17" src="https://github.com/user-attachments/assets/9ab7bad3-0edd-495b-9b54-77e8bc13fe0a" />



seq 2 | sed '2i hello'
## output
<img width="643" height="83" alt="481358159-b76d42a0-0165-4495-be8b-16b3532682b5" src="https://github.com/user-attachments/assets/40b18bd5-6f63-4f48-b970-0b69228cc567" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="643" height="80" alt="481358167-30a0beec-40af-4b6b-8abd-28f9e351294e" src="https://github.com/user-attachments/assets/61612685-ff88-4c80-89c2-8f88fc765d16" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="643" height="90" alt="481358187-73d81c60-ce43-4d41-834e-cd79e0ec47f2" src="https://github.com/user-attachments/assets/e9390113-e0e5-4dfd-9df3-a18f8dd70d1f" />


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
sort file21
## OUTPUT
<img width="643" height="93" alt="481358191-6bf49e9b-04fc-45bd-8c87-935e9ae0e114" src="https://github.com/user-attachments/assets/fb0237c6-052d-4e3d-b379-d28fa1b7553b" />


cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
uniq file22
## OUTPUT

<img width="643" height="115" alt="481358199-4894679b-dca0-4d18-94ee-f6dc1ad9ef41" src="https://github.com/user-attachments/assets/c4f222d1-3393-4c54-8a29-43c3bc1cd0e2" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="677" height="166" alt="481358211-ca93b037-563a-49b9-b859-3734039cec13" src="https://github.com/user-attachments/assets/2cabba83-c93f-4a03-8eb7-05d2cac93195" />

cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
^d
 
cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
 
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="677" height="85" alt="481358224-760d8a4c-857b-4617-bc7a-6c32d30a3101" src="https://github.com/user-attachments/assets/659cdc90-a949-4a14-a4f8-39bb666e9a6f" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="728" height="79" alt="481358233-7f4c9c96-96d6-4755-ac8b-9cc33a6b98a1" src="https://github.com/user-attachments/assets/fd1c1cd9-ffdf-43c6-a0ea-d7e127333ead" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="863" height="157" alt="481358255-4c790a64-b0e0-4d90-9cf6-7dfe28d90f20" src="https://github.com/user-attachments/assets/58407f35-29a3-4394-949a-55bb1ffd7ac6" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="844" height="204" alt="481358290-0629ac7d-80b0-457d-b634-81de0876589b" src="https://github.com/user-attachments/assets/33c8f726-2490-4b02-8d1e-2440edef56b7" />


tar -xvf backup.tar
## OUTPUT
<img width="518" height="200" alt="481358297-3c51ef5b-41fb-469a-bfa6-c26f94c0a26e" src="https://github.com/user-attachments/assets/365dcb96-75d6-4e6c-a037-a4e5aa959830" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="704" height="308" alt="481358317-77e9942f-f9d8-4db9-8696-e247fed38020" src="https://github.com/user-attachments/assets/9f884b04-fd5e-4016-8ce0-6d68abf1f260" />

gunzip backup.tar.gz
## OUTPUT
<img width="704" height="308" alt="481358317-77e9942f-f9d8-4db9-8696-e247fed38020" src="https://github.com/user-attachments/assets/8825b514-5740-4b6c-affd-40ed2b45937c" />

 
# Shell Script

echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="529" height="48" alt="481358332-8911a329-2edb-4e1b-bee9-ad1fe11ff5a4" src="https://github.com/user-attachments/assets/05eea900-39e2-4179-b1ce-d254f300e5e8" />

 
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop


cat herecheck.txt
## OUTPUT

<img width="532" height="63" alt="481358345-f95efbc1-c4d3-414e-a3e1-bd531cf272c3" src="https://github.com/user-attachments/assets/528aa90e-ddb0-4f95-b676-6d2204ec5ac5" />

cat < scriptest.sh 
bash
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
 

cat scriptest.sh 
bash
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

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="571" height="345" alt="481358353-679e99d5-1492-4664-a40a-0dc3826ed024" src="https://github.com/user-attachments/assets/892da94c-b319-4d3f-a8c8-9a64348d561c" />

 
ls file1
## OUTPUT
<img width="571" height="49" alt="481358361-cd5b0b3a-164a-4c8f-92be-233b9e00219b" src="https://github.com/user-attachments/assets/0e4634d7-1bcd-41e0-b1ed-5e053d504e26" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="571" height="43" alt="481358374-67c17e8d-d98d-49fa-80ea-3da34e4f1bad" src="https://github.com/user-attachments/assets/f933b178-f7bd-4e33-86d6-e4fba7b44244" />

abcd
 
echo $?
 ## OUTPUT
<img width="571" height="43" alt="481358446-6278962e-5be4-42d4-98d9-dc734596dc38" src="https://github.com/user-attachments/assets/bfcb9046-e5eb-4839-90a7-1dfe480a6b1a" />


 
# mis-using string comparisons

cat < strcomp.sh 
bash
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


cat strcomp.sh 
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi

##OUTPUT
<img width="571" height="62" alt="481358531-3595c50c-6eb8-48e7-9b3f-12555868f693" src="https://github.com/user-attachments/assets/c68eb74e-259f-490f-99d9-fc8e8d47a4c3" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="571" height="62" alt="481358531-3595c50c-6eb8-48e7-9b3f-12555868f693" src="https://github.com/user-attachments/assets/c9587f3d-9839-4fb9-a242-d8b344108141" />


# check file ownership
cat < psswdperm.sh 
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d


cat psswdperm.sh 
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 
./psswdperm.sh
## OUTPUT
<img width="593" height="61" alt="481358506-036df755-6149-4319-9766-8b6b826a6c1d" src="https://github.com/user-attachments/assets/4353b605-3df8-44a5-a48a-c62cc1c53cac" />

# check if with file location
cat>ifnested.sh 
bash
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

cat ifnested.sh 

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


./ifnested.sh 
## OUTPUT
<img width="812" height="114" alt="481358622-36d73493-16ff-413e-a01f-328ceb536307" src="https://github.com/user-attachments/assets/fe331b05-1cd1-4954-8dcb-f772eea42dec" />



# using numeric test comparisons
cat > iftest.sh 
bash
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



cat iftest.sh 
bash
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


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="812" height="114" alt="481358642-910f4c78-e5e3-4570-9926-04ebf56fd1cd" src="https://github.com/user-attachments/assets/51355f1b-77b8-4c95-b3d6-929824d7d48e" />

# check if a file
cat > ifnested.sh 
bash
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


cat ifnested.sh 
bash
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


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="812" height="114" alt="481358683-464253fc-5b3a-4b71-ae05-5b6f232bcdf8" src="https://github.com/user-attachments/assets/b943f8cf-6257-4aa5-9c6a-37f321786eff" />

# looking for a possible value using elif
cat elifcheck.sh 
bash
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


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="812" height="79" alt="481358666-7f84f6a5-704f-45a4-9f95-778adaab800f" src="https://github.com/user-attachments/assets/62e8caa4-e44f-42c0-90fe-6c86b513801e" />


# testing compound comparisons
cat> ifcompound.sh 
bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="812" height="79" alt="481358694-c9d4ac81-3395-4ca6-a53a-d88af6b32553" src="https://github.com/user-attachments/assets/b9c07ea1-8da6-4820-8f12-3876a77797eb" />


# using the case command
cat >casecheck.sh 
bash
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

$ chmod 755 casecheck.sh 
 <img width="728" height="79" alt="481358710-13d32690-9b12-49de-adbf-bd42598efbf3" src="https://github.com/user-attachments/assets/a4337a44-af57-4f4f-be43-094f1fef22ac" />

$ ./casecheck.sh 
 
cat > whiletest
bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 <img width="595" height="133" alt="481358735-5e6e97fe-ab88-4dbe-9a26-79a792792ab8" src="https://github.com/user-attachments/assets/edc7a223-5b22-48fa-a672-ea86de34e752" />

cat untiltest.sh 
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
 
$ chmod 755 untiltest.sh
 
 <img width="595" height="133" alt="481358751-c4575de0-dd99-450a-b717-6fdb3fb8d8f0" src="https://github.com/user-attachments/assets/6a337653-ab88-490e-8e6f-0a6828c323e9" />

 
cat forin1.sh 
bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done

$ chmod 755 forin2.sh
 <img width="595" height="167" alt="481358829-895156a0-5321-4a64-a2ed-d7336a57fff5" src="https://github.com/user-attachments/assets/5b9808df-0dda-45d5-9742-7b371a62d9b9" />

$ ./forin2.sh 
 
cat forin3.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done

$ ./forin3.sh 
 
cat forin1.sh 
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done

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
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
`
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
bash
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

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
bash
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

## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
bash
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


 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
bash
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

## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done

$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
bash
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

$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x

## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
bash
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
 
cat>data.dat
bash
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

awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
bash
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

## OUTPUT 


<img width="599" height="112" alt="481359003-4d6da4f2-3757-44fe-bb60-fb298fe3bf9a" src="https://github.com/user-attachments/assets/44139820-e7c6-45b0-abda-1a092e17fb90" />

# RESULT:
The Commands are executed successfully.

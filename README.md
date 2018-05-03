# ShellScripting
pswarna@ubuntu:~/Shell_Scripting$ who am i
pswarna  pts/0        2018-05-03 09:48 (182.72.116.161)

pswarna@ubuntu:~/Shell_Scripting$ pwd
/home/pswarna/Shell_Scripting

pswarna@ubuntu:~/Shell_Scripting$ cal
      May 2018
Su Mo Tu We Th Fr Sa
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
20 21 22 23 24 25 26
27 28 29 30 31

pswarna@ubuntu:~/Shell_Scripting$ cal Nov 1993
   November 1993
Su Mo Tu We Th Fr Sa
    1  2  3  4  5  6
 7  8  9 10 11 12 13
14 15 16 17 18 19 20
21 22 23 24 25 26 27
28 29 30

pswarna@ubuntu:~/Shell_Scripting$ date
Thu May  3 10:14:41 UTC 2018

pswarna@ubuntu:~/Shell_Scripting$ date '+DATE:%d-%m-%y%nTIME:%H-%M-%S'
DATE:03-05-18
TIME:10-18-06

pswarna@ubuntu:~/Shell_Scripting$ touch test1 test2 test3
pswarna@ubuntu:~/Shell_Scripting$ ls -l
total 0
-rw-rw-r-- 1 pswarna pswarna 0 May  3 10:19 test1
-rw-rw-r-- 1 pswarna pswarna 0 May  3 10:19 test2
-rw-rw-r-- 1 pswarna pswarna 0 May  3 10:19 test3

pswarna@ubuntu:~/Shell_Scripting$ mkdir Test
pswarna@ubuntu:~/Shell_Scripting$ ls -l
total 4
drwxrwxr-x 2 pswarna pswarna 4096 May  3 10:21 Test
-rw-rw-r-- 1 pswarna pswarna    0 May  3 10:19 test1
-rw-rw-r-- 1 pswarna pswarna    0 May  3 10:19 test2
-rw-rw-r-- 1 pswarna pswarna    0 May  3 10:19 test3

pswarna@ubuntu:~$ pwd
/home/pswarna
pswarna@ubuntu:~$ cd Shell_Scripting/
pswarna@ubuntu:~/Shell_Scripting$

pswarna@ubuntu:~/Shell_Scripting$ cat > testFile
This is the testFile created with cat command
pressing ctrl+d will save and exit this file

pswarna@ubuntu:~/Shell_Scripting$ cat < testFile
This is the testFile created with cat command
pressing ctrl+d will save and exit this file

pswarna@ubuntu:~/Shell_Scripting$ cat > testFile2
This is the second file

pswarna@ubuntu:~/Shell_Scripting$ cat testFile testFile2 > mergedFile

pswarna@ubuntu:~/Shell_Scripting$ cat mergedFile
This is the testFile created with cat command
pressing ctrl+d will save and exit this file
This is the second file

pswarna@ubuntu:~/Shell_Scripting$ ls
Test  mergedFile  test1  test2  test3  testFile  testFile2
pswarna@ubuntu:~/Shell_Scripting$ mv test1 test4
pswarna@ubuntu:~/Shell_Scripting$ ls
Test  mergedFile  test2  test3  test4  testFile  testFile2

pswarna@ubuntu:~/Shell_Scripting$ ls
Test  mergedFile  test2  test3  test4  testFile  testFile2
pswarna@ubuntu:~/Shell_Scripting$ rm test2
pswarna@ubuntu:~/Shell_Scripting$ ls
Test  mergedFile  test3  test4  testFile  testFile2

pswarna@ubuntu:~/Shell_Scripting$ rm Test
rm: cannot remove 'Test': Is a directory

pswarna@ubuntu:~/Shell_Scripting$ rm -r Test
pswarna@ubuntu:~/Shell_Scripting$ ls
mergedFile  test3  test4  testFile  testFile2

pswarna@ubuntu:~/Shell_Scripting$ mkdir Test
pswarna@ubuntu:~/Shell_Scripting$ ls
Test  mergedFile  test3  test4  testFile  testFile2
pswarna@ubuntu:~/Shell_Scripting$ rmdir Test
pswarna@ubuntu:~/Shell_Scripting$ ls
mergedFile  test3  test4  testFile  testFile2

pswarna@ubuntu:~$ cp ~/Shell_Scripting/mergedFile ~/Music/

pswarna@ubuntu:~/Shell_Scripting$ ln mergedFile mergedFileLink
# It is a hard link which is nothing but creating an another file and both the files will be in sync always

pswarna@ubuntu:~/Shell_Scripting$ ln -s mergedFile mergedFileSLink
# It is a soft link which is nothing but creating a reference to the existing file
lrwxrwxrwx 1 pswarna pswarna  10 May  3 10:43 mergedFileSLink -> mergedFile

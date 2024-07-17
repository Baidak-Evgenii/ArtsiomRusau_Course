# 📌 bash

Иногда нам необходимо работать с удаленными серверами, у которых нет графического интерфейса. В этом случае полезно иметь возможность использовать команды bash. Они позволяют нам выполнять обычные действия, такие как создание, редактирование, удаление файлов и папок через CLI. 

Я рад поделиться некоторыми командами bash, которые я использовал для выполнения задач во время обучения в области обеспечения качества.

## Navigation

- [Работа с файлами и каталогами](#task-1)
- [Редактирование файлов, проверка и завершение процессов, работа с сайтами](#task-2)

## Task 1

##### Working with files and directories
```bash
~                                     # Home directory 
pwd                                   # Show current directory path
mkdir test1                           # Create a directory named test1
cd test1                              # Go to directory test1 (also possible to write the path to needed directory)
touch file{1,2,3}.txt.                # Create file 1,2 and 3 inside directory test1
ls                                    # Check directory test1 content (ls -la if there are any hidden files) 
cd                                    # Go home directory 
mkdir test2                           # Create directory test2 inside home directory
rmdir test2                           # Delete directory test2 
cd mv ~/test1                         # Go back to directory test1
rm file2.txt                          # Delete file 2 
mkdir test3                           # Create directory test3
touch file{4,5}.txt                   # Add two files to directory test3
cd ..                                 # Go back to parent directory
rmdir -rf test3                       # Delete directory test3  
ls                                    # Make sure directory test3 was deleted
mkdir test4                           # Create directory test4
mv ~/test1/file{1,3}.txt ~/test4      # Move file1.txt and file3.txt from directory test1 to directory test4
echo line11 >> file1.txt              # Add 3 lines to file1.txt
echo line12 >> file1.txt            
echo line13 >> file1.txt
cat file1.txt                         # Check content of file1.txt
echo line31 >> file3.txt              # Add 3 lines to file3.txt
echo line32 >> file3.txt
echo line33 >> file3.txt
cat file1.txt file3.txt               # Check contents of file1.txt and file3.txt at once
nano file1.txt + manual replacement   # Using one of the editors, replace all lines in file1.txt and file3.txt
nano file3.txt + manual replacement 
```
## Task 2
##### Editing files, checking and killing proccesses, pinging websites
```bash
mkdir test3                                   # Create directory test3 
cd test3                                      # Open directory test3 
echo -e "row1\nrow2\nrow3\nrow4" > file4.txt  # Add 3 files to test3, each of which should contain 4 lines
echo -e "row1\nrow2\nrow3\nrow4" > file5.txt  
echo -e "row1\nrow2\nrow3\nrow4" > file6.txt 
grep "row2" file5.txt                         # Find the line "row2" in file5.txt 
grep -R "row" .                               # Find the line "row" in the test3 directory
grep -c "row" file6.txt                       # Count number of lines containing word "row" in file6.txt
find . -name "file5.txt"                      # Find file5.txt in test3 directory
find . -name "file5.txt" -delete              # Using find command delete file5.txt
echo test > file4.txt                         # Using the echo command, add the word "test" to file4.txt
sed 's/test/fail/g' file4.txt                 # Change the word "test" in file4.txt to "fail"
echo test >> file4.txt                        # Add the word "test" to file4.txt so that the content is preserved
ps aux                                        # View all processes in the system
kill 666                                      # Kill process 666 in console
ping artsiomrusau.com                         # Check the availability of the website artsiomrusau.com using ping
ping -c 5 artsiomrusau.com                    # Send 5 packages to artsiomrusau.com  
curl https://petstore.swagger.io/v2/pet/      # Using GET and cURL command, get info about registered pets at petstore.swagger.io
findByStatus?status=registered                
curl -X POST https://petstore.swagger.io/     # Using POST and cURL command, create a new user at petstore.swagger.io
v2/user --data "id=1" 
--data "username=Darrel_Volkman80" 
--data "firstName=Darrel" 
--data "lastName=Volkman" 
--data "email=Darrel_Volkman80@gmail.com" 
--data "password=g8kq2W1z_utLEBs" 
--data "phone=7442783865" 
--data "userStatus=0"
```

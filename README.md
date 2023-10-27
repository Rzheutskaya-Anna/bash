# 📌 bash

Sometimes we need to work with remote servers that don't have any graphic interface. In this case it's good to be able to use bash commands. They allow us to perform regular actions such as creating, editing, deleting files and folders via CLI. 

I am happy to share some bash commands that I used to do tasks during my Quality Assurance studies. 

## Easy navigation
- [Working with files and directories](#task-1)
- [Editing files, checking and killing proccesses, working with websites](#task-2)

## Task 1

##### Working with files and directories
pwd -                                                              Show current directory path  
mkdir test1 -                                                      Create a directory test1  
cd test1 -                                                         Go to directory test1  
touch file1.txt file2.txt file3.txt -                              Create file 1,2 and 3 inside directory test1  
ls file1.txt  file2.txt  file3.txt - Check directory test1 content
cd .. - Go home directory 
mkdir test2 - Create directory test2 inside home directory
rmdir test 2 - Delete directory test2 
cd test1 - Go back to directory test1
rm file2.txt - Delete file 2 
mkdir test3 - Create directory test3
touch file4.txt file5.txt - Add two files to directory test3
cd .. - Go back to parent directory
rm -rf test3 - Delete directory test3 
mkdir test4 - Create directory test4
mv test1/file1.txt test4 - Move file1.txt from directory test1 to directory test4
mv test1/file3.txt test4 - Move file3.txt from directory test1 to directory test4
echo line>file1.txt - Add 3 lines to file1.txt
echo line>>file1.txt
echo line>>file1.txt
cat file1.txt - Check content of file1.txt
echo line>file3.txt - Add 3 lines to file3.txt
echo line>>file3.txt
echo line>>file3.txt
cat file1.txt file3.txt - Check contents of file1.txt and file3.txt at once

## Task 2
##### Editing files, checking and killing proccesses, pinging websites

mkdir test3 - Create directory test3
cd test3 - Open directory test3
echo -e "row1\nrow2\nrow3\nrow4" >> file4.txt - Add 3 files to test3, each of which should contain 4 lines
echo -e "row1\nrow2\nrow3\nrow4" >> file5.txt
echo -e "row1\nrow2\nrow3\nrow4" >> file6.txt
grep "row2" file5.txt - Find the line "row2" in file5.txt
grep -c "row" file6.txt - Count number of lines containing word "row" in file6.txt
find test3 -name "file5.txt" - Find file5.txt in test3 directory
echo "test" >> file4.txt - Add the word "test" to file4.txt so that the content is preserved
sed -i 's/test/fail/g' file4.txt - Change the word "test" in file4.txt to "fail"
ps aux - View all processes in the system
kill 666 - Kill process 666 in console
ping artsiomrusau.com - check the availability of the website artsiomrusau.com using ping
ping -n 5 artsiomrusau.com - Send 5 packages to artsiomrusau.com  
curl https://petstore.swagger.io/v2/pet/findByStatus?status=registered - Using GET and cURL command, get info about registered pets at petstore.swagger.io
curl -X POST -H "Content-Type: application/json" -d '{   - Using POST and cURL command, create a new user at petstore.swagger.io
  "id": 2350,
  "username": "user32655",
  "firstName": "Anna",
  "lastName": "John",
  "email": "anna3264851@gmail.com",
  "password": "862855858",
  "phone": "5646756457864"
}' https://petstore.swagger.io/v2/user
{"code":200,"type":"unknown","message":"2350"}




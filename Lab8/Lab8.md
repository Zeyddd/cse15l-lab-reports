# Lab 5

## Grade.sh code
```
rm -rf student-submission

CP=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"
CP2=.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore"
SCORE=" "

git clone $1 student-submission

echo "Cloned Successfully"

cp TestListExamples.javas student-submission
cp -r lib student-submission
cd student-submission

if [[ -f "ListExamples.java" ]]
then
    echo "File Found"
else
    SCORE="Wrong file submitted. Failed"
    echo $SCORE
    exit
fi

javac -cp $CP *.java
if [[ $? -eq 0 ]]
then
    echo "Compiled Successfully"
else
    SCORE="Failed compilation. Failed"
    echo $SCORE
    exit 0
fi

java -cp $CP2 TestListExamples

if [[ $? -eq 0 ]]
then
    SCORE="Pass"
else
    SCORE="Partial Pass"
fi
echo $SCORE
```

## Screenshots


**First student submission**

![1](https://user-images.githubusercontent.com/53220531/204067017-40938952-70d4-446c-a5cb-6b6ef5795d10.png)

**Second student submission**

![2](https://user-images.githubusercontent.com/53220531/204067019-b246eeab-0c3c-4c11-a12e-798ccdf8889b.png)

**Third student submission**

![3](https://user-images.githubusercontent.com/53220531/204067024-c0437f4f-d727-4c6a-9efe-926d608e417c.png)

## Code trace

I will trace the third student submission, where there is a compilation error.

- Line 1: *STDOUT* would be nothing, as there would be no console output when successfully removing a file/folder. 
*STDERR* would be nothing, as there would be no console output when unsuccessfully removing a file/folder that doesnt exist. Return code 0.
- Line 3-5: No *STDOUT* or *STDERR* as its just assigning variables. Return code 0.
- Line 7: *STDOUT*  would be the entire text of the cloning process. No *STDERR*. Return code 0.
- Line 9: No *STDERR*. Only an *STDOUT* stating that the cloning was successful. Return code 0.
- Line 11-12: *STDOUT* of nothing if successful. No *STDERR* either, as it wouldn't be possible for the directory to not exist if the above code works. Return code 0.
- Line 13: No *STDOUT* or *STDERR* as you're just moving into a directory. Return code 0.
- Line 15: True if statement as the file was found. Return code 0.
- Line 17: *STDOUT* of "File Found" due to the echo. No *STDERR*. Return code 0.
- Line 24: *STDERR* of the compilation error. Return non-zero code.
- Line 25: False as error code is non-zero.
- Line 29: No *STDERR* or *STDOUT* as assigning a value to a variable. Return code 0.
- Line 30: *STDOUT* of the variable value. Return code 0.
- Line 31: Exits script.
- Lines 18-21, 25-26, 32-52: Don't run.

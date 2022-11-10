# Grep command

## Command options

- -w

The -w command only searches for exact matches. With the first example, the power of -w is shown. The command is extremely useful when you have a large amounts of data, and you'd like to find a very specific file/text within the data, then -w is very useful.

As we can see here, when searching for "Hell", without the -w, it shows Hello World in the file, as "Hell" is contained in "Hello", whereas with -w, it wouldn't show up as grep would then search for the exact word "Hell", which isn't contained in the file. 

![1](https://user-images.githubusercontent.com/53220531/198898717-4b011a8b-55d4-4229-8c9b-8de7fe6b26ec.png)

`grep -w "Hello" file.txt`

`grep -w "Hell" file.txt`

`find > find.txt`
`grep "Hell" file.txt`


In this example, I only wanted to find the files/directories that matched exactly with **Test**, so I used -w

![5](https://user-images.githubusercontent.com/53220531/198898723-35f1bb70-413f-41f5-95fd-d09a7534d4bd.png)

`grep -w "test" Test.txt`


Here, I wanted to find where the file, "chapter-1" was, and exactly that file. I did so by placing every file within technical into a .txt file, then used grep on it.

![9](https://user-images.githubusercontent.com/53220531/198898726-033da61f-04eb-4286-aa79-91ed769d09e4.png)

`grep -w "chapter-1.txt" find.txt`


- -i

The -i command ignorse case sensitivity within the search. This becomes very useful when you want to try narrowing down what you're searching for. For example, in technical, you may want to search for some data in the bio research papers, but you're unsure of the exact syntax. Using -i greatly helps narrow down what you're looking for.

As we can see here, we can search for "hello" with the -i command, it "Hello world2" shows up, whereas without it nothing shows up.


![2](https://user-images.githubusercontent.com/53220531/198898729-6a96c730-327f-4a7d-806c-4fd9c0d417cf.png)

`grep "hello" file.txt`
`grep -i "hello" file.txt`

In this example, I used the find command to pull all the files inside the **Test** directory inside of a file, then used `grep -i "test" Test.txt` to find out how many Test files or directories I had.


![4](https://user-images.githubusercontent.com/53220531/198898732-47544df8-299f-43a2-9690-fb345bdb3cf0.png)

`find > test.txt`
`grep "hello" file.txt`


In this example, I wanted to find the all the pbio file names, regardless of capitalization, so I placed all the technical filest in it, and searched that file using grep.

![6](https://user-images.githubusercontent.com/53220531/198898737-07a31aa9-c0bc-4c07-90a6-5f483de0cf14.png)

`find technical > technical.txt`
`grep -i "pbio.003" technical.txt`


- using pipe

Using the pipe command along with grep, you can search for extensions of files or file names. As shown here, we can see the extension ".txt" shows up with the command. This command is extremely useful for saving time. Using the second example
`find * > find.txt`
`grep -i "hello"`
is all condensed to `find * | xargs grep -i "hello"`. Although doing it once may save a few seconds, over time with many hundereds of commands, it saves hours worth of time.

![3](https://user-images.githubusercontent.com/53220531/198898746-08c2fe1e-603a-4652-b17b-0fe062f9095b.png)

`ls | grep ".txt"`

In this example, we combined the find, pipe and xargs command to search for the word "hello" inside of all the files within the directory.

![8](https://user-images.githubusercontent.com/53220531/198898751-bb69bb0a-882d-4599-a50b-04290802933c.png)

`find * | xargs grep -i "hello"`


Here, instead of placing the file names inside of a .txt file first, and then using grep, we can simply use the pipe command to do it all on one line

![7](https://user-images.githubusercontent.com/53220531/198898753-c69cc779-484b-47e1-9a57-8716303426b1.png)

`ls * | grep -w "pmed"`

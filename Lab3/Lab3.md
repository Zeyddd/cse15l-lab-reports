# Grep command

## Command options

- -w

The -w command only searches for exact matches.

As we can see here, when searching for "Hell", without the -w, it shows Hello World in the file, as "Hell" is contained in "Hello", whereas with -w, it wouldn't show up as grep would then search for the exact word "Hell", which isn't contained in the file. 

[Image1]

In this example, I only wanted to find the files/directories that matched exactly with **Test**, so I used -w

[Image5]

Here, I wanted to find where the file, "chapter-1" was, and exactly that file. I did so by placing every file within technical into a .txt file, then used grep on it.

[Image9]

- -i

The -i command ignorse case sensitivity within the search

As we can see here, we can search for "hello" with the -i command, it "Hello world2" shows up, whereas without it nothing shows up.


[Image2]


In this example, I used the find command to pull all the files inside the **Test** directory inside of a file, then used `grep -i "test" Test.txt` to find out how many Test files or directories I had.


[Image4]

In this example, I wanted to find the all the pbio file names, regardless of capitalization, so I placed all the technical filest in it, and searched that file using grep.

[Image6]

- using pipe

Using the pipe command along with grep, you can search for extensions of files or file names. As shown here, we can see the extension ".txt" shows up with the command.

[Image3]

In this example, we combined the find, pipe and xargs command to search for the word "hello" inside of all the files within the directory.

[Image8]

Here, instead of placing the file names inside of a .txt file first, and then using grep, we can simply use the pipe command to do it all on one line

[Image7]
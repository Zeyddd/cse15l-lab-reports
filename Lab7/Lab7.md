# Part 1

## Task: Adding a new line to print before File[] paths = f.listfiles()

In order to do this task in under 30 key strokes, I had to prepare and copied the following code beforehand: `Adding a new line to print before File[] paths = f.listfiles()`
Without doing so, I could not find a way to do this below 30 key strokes.

**Commands used with paste**

`15gg, <SHIFT> 4, p, :wq`

**Commands used without paste**
`15gg, <SHIFT> 4, a, <ENTER>, S, y, s, t, e, m, ., o, u, t, ., p, r, i, n, t, (, f, ., t, o, S, t, r, i, n, g, (, ), ), <ESC>, :wq`

**What the commands do**
- `15gg` Moves the the 15th line, 15 being the line number, gg stating that we want to move to the next line
- `a` Appends/Inserts at the character next to the cursor
- `wq` Saves and exits vim mode

![1](https://user-images.githubusercontent.com/53220531/201223306-ccdb071b-046d-4c5b-8067-8585e15133bc.png)
![2](https://user-images.githubusercontent.com/53220531/201223353-9b5ca586-f3d1-42a1-9fc1-668856cda1ba.png)
![4](https://user-images.githubusercontent.com/53220531/201223362-7df4eac6-0895-42de-811f-84b4905ea34c.png)
![3](https://user-images.githubusercontent.com/53220531/201223372-d8e852b5-32bd-4337-b822-9db43512bb72.png)



# Part 2

- Time with local: 33s
- Time remotely: 24s

## Difficulties

I struggled more with the vim, as it took me a couple of tries to get a decent time. I think the reason for this is that I'm not used to the vim commands. Having to move the cursor soley through the keyboard and having the cursor look weird is still new to me, in comparison to locally where you can just use your mouse and select the line that you want to edit. 

I also ran into a problem locally, where it takes some time to scp the file, then ssh'ing due to my keyphrase, which I can see to be very frustrating if I were to have to keep doing this repetitively for edits.

## Questions

I personally much prefer editing locally over remotely. However, if I were required to run programs remotely, I would probably work on the program remotely, as the hassle of copying and logging into the remote server every couple of minutes to test some code is very frustrating.

If we had the option to push to github, then simply clone the repository onto the remote and just run it there, I would much rather use that method and simply work on the program locally, as I find it much more comfortable. However, if I were forced to manually copy the files over for every edit, I would work on the program remotely.

# Part 1

## Task: Adding a new line to print before File[] paths = f.listfiles()

In order to do this task in under 30 key strokes, I had to prepare and copied the following code beforehand: `Adding a new line to print before File[] paths = f.listfiles()`
Without doing so, I could not find a way to do this below 30 key strokes.

**Commands used with paste**

`15gg, <SHIFT> 4, p, :wq`

**Commands used without paste**
`15gg, <SHIFT> 4, a, <ENTER>, S, y, s, t, e, m, ., o, u, t, ., p, r, i, n, t, (, f, ., t, o, S, t, r, i, n, g, (, ), ), <ESC>, :wq`

[1]
[2]
[4]
[3]

# Part 2

- Time with local: 33s
- Time remotely: 24s

## Difficulties

I struggled more with the vim, as it took me a couple of tries to get a decent time. I think the reason for this is that I'm not used to the vim commands. Having to move the cursor soley through the keyboard and having the cursor look weird is still new to me, in comparison to locally where you can just use your mouse and select the line that you want to edit. 

I also ran into a problem locally, where it takes some time to scp the file, then ssh'ing due to my keyphrase, which I can see to be very frustrating if I were to have to keep doing this repetitively for edits.

## Questions

I personally much prefer editing locally over remotely. However, if I were required to run programs remotely, I would probably work on the program remotely, as the hassle of copying and logging into the remote server every couple of minutes to test some code is very frustrating.

If we had the option to push to github, then simply clone the repository onto the remote and just run it there, I would much rather use that method and simply work on the program locally, as I find it much more comfortable. However, if I were forced to manually copy the files over for every edit, I would work on the program remotely.
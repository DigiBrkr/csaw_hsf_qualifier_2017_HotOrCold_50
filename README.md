# HotOrCold  
50 Points

>This site is another suspicious site you found in his (sic) Herbert's browser history.
>This .class file was dumped in the OwnForAll leaks.
>What is it doing?
>We've uploaded it here for your convenience.

## Solving it

We are given a java .class file. We run it in our terminal with this command
`# java HotOrCold`.  Don't include the extension, lesson I learned the hard way!
Then we see the following:
```
Let's play hot or cold! What is the passcode?
>>>
```
Now we could try and guess the passcode but that would just be a waste of time.
Let's use the "hacker" approach to solve this problem, which is to decompile the file.
The easiest way to do that is too use an online Java decompiler like [www.javadecompilers.com](http://www.javadecompilers.com/). We simply upload the file and let it do the hard work.
Copy it into the text editor of your choice (I like Atom) and start going though the file.
After looking at it for a minute or two, your attention should be drawn to line 4:
`private static String PASSCODE = "Java coffee";`.
We can see that `PASSCODE = "Java coffee"`, so lets enter it in our terminal.
```
# java HotOrCold
Let's play hot or cold! What is the passcode?
>> Java coffee

Java coffee IS "hot"!! Haha, get it? Anyway, here's the flag:
flag{it_is_byt3c0ld_in_th3_s0uth_p0l3}
```
`flag{it_is_byt3c0ld_in_th3_s0uth_p0l3}`



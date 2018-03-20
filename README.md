# QuickNotes Mac workflow

How I take notes in class (developers edition)

Ok so the gist of the matter is, MacBooks or really any laptop having to run a browser is inevitably going to slow down its processing speed since resources are being allocated to rendering graphics through the GPU and virtual memory being taken up due to RAM constraints. This becomes extremely violate once I begin using Google drive which is the focus of this discussion. 

As I suspect, many students and programmers alike end up using Google drive for personal convenience and the resources it seize can act as a determent to your productivity and time. 

Fortunately I have developed a simple procedure to remedy this using tools available to all programmers. Lets begin...

### Prerequisites

What things you need to install the software: 
* MacOS
* [iTerm](https://www.iterm2.com/) - terminal simulator
* [Homebrew](https://brew.sh/) - Mac package manager
* Vim 

### Getting Start

Ok heres where the fun begins - please bear with me. 

### Installing

Open up iTerm and ssing Homebrew you will need to install [gdrive](https://github.com/prasmussen/gdrive)

```
$ brew install gdrive
```

Now unfortunately some of the feature gdrive offers are not entirely fleshed out like their sync options which I have struggled with. This is a handy [resource](https://github.com/cyhsu/gdrive_doc) if you are having issues.

Once completed what you should do is make a directory using gdrive

```
$ gdrive mkdir DIRECTORY_NAME
```

cd into that directory and make the files needed I typically save them under as either .rmd, .md, .pdf

Typically to upload the files you would just upload that enclosed directory 

```
$ gdrive sync upload . DIRECTORY_NAME
```
but because I use vim we are going to proceed a bit differently


Opening up Iterm preferences and scrolling over to the profile section you can see a couple of option available. 
How I like to proceed is buying adding a new profile and adding these options:
* set name to whatever you would like 
* Change command to the command subheading and change set text at start to a command you would prefer the file to be opened with. 
```
nvim Friendship.md
```
* and change directory to advanced configuration and set it to wherever your file is located. 

![](https://github.com/derekacosta/QuickNotes/blob/master/Screen%20Shot%202018-03-13%20at%206.26.50%20PM.jpg)

Now that is completed go to keys tab and add a new key. 
I have my keyboard shortcut set to ⌘s (command s) and change the action to "Send Text with "vim" Special Chars" to which I have added 

```
:wa | !gdrive sync upload . DIRECTORY_NAME
```
![](https://github.com/derekacosta/QuickNotes/raw/master/Screen%20Shot%202018-03-13%20at%206.26.20%20PM.jpg)

From there in the Key tab check on the Hotkey window and Configure Hotkey window and now you can adjust it to whatever you amy like. 

![](https://github.com/derekacosta/QuickNotes/raw/master/Screen%20Shot%202018-03-13%20at%206.26.07%20PM.jpg)

Play around with the windows option to customize it to your liking. 

![](https://github.com/derekacosta/QuickNotes/raw/master/Screen%20Shot%202018-03-13%20at%206.26.32%20PM.jpg)

Lastly, and most importantly, to prevent closing a window accidentally and losing your notes please do the following: 
* go to session and choose "Always prompt before closing"

![](https://github.com/derekacosta/QuickNotes/blob/master/Screen%20Shot%202018-03-20%20at%2011.20.53%20AM.jpg)

And you're done! 

[![](https://github.com/derekacosta/QuickNotes/raw/master/Screen%20Shot%202018-03-13%20at%2011.40.06%20PM.jpg)](https://www.youtube.com/watch?v=C4GSWgluf1I)
https://www.youtube.com/watch?v=C4GSWgluf1I

## Authors

[**Derek Acosta**](https://github.com/derekacosta)

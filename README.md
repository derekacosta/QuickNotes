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
is my set up 
* and change directory to advanced configuration and set it to wherever your file is located. 

Now that is completed go to keys tab and add a new key. 
I have my keyboard shortcut set to ⌘s (command s) and change the action to "Send Text with "vim" Special Chars" to which I have added 

```
:wa | !gdrive sync upload . DIRECTORY_NAME
```

From there in the Key tab check on the Hotkey window and Configure Hotkey window and now you can adjust it to whatever you amy like. 

Play around with the windows option to customize it to your liking. 



And you're done! 

All you need to do now is 


```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc


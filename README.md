# songbook

This is the songbook template used by my local scout group. You are free to use and modify it.
Because this songbook is using the [LaTeX Songs Package](http://songs.sourceforge.net/), it is licensed under the GPL v2.0. 
The original songs package itself has not been modified for this purpose. 
If you are using this as your template please be sure to share your sources as well. 
Happy singing :)

## How to Install

### prerequisites

The chordbook assumes that you have installed a view general latex-packages for using latex. 
Especially `pdflatex` and `luatex` are a must have. 
Windows users can get access to these via installing [MikTex](https://miktex.org/). 
I assume that UNIX-users know how to install software (or at least how to search for the information on google or duckduckgo) since they are superior ;)

You should also have installed the Latex-Songs-Package (see link above for more instructions). 

It is not really required but highly recommended to have a somewhat useful text editor installed. 
For non-keyboard-wizards, [TexMaker](https://www.xm1math.net/texmaker/) works just fine. 
Some however might prefer to use [Vim](https://www.vim.org/). 

### general build instructions

On Linux (Mac should work the same) just run `make` inside the build directory. 

On Windows just run `make.bat` inside the build directory. 

## How I like to use this template

Generally I prefer the following layout: 
 - Every verse should be in one line of code. That way, the songs package can work it's magic and put everything on the paper using a close-to-minimum amount of space. Now notice, I said "should". Your job is to be on the lookout for sketchy parts of a song where it makes more sense to make a new line instead. For Instance, have a look at the following lyrics from "Junge" by "Die Ärzte": 
   ```
   ...
                 Dm                      Am
   Löcher in der Hose und ständig dieser Lärm
                   C
   (was sollen die Nachbarn sagen?)
   ...
   ```
   In the given example it makes a lot of sense to put the part in parenthesis in their own line of song lyrics. For one, because it is sung as an echo to the first part, and secondly because it does not increase readability if it would not have its own line of song text. The other lyrics should be on the very same line of text, because the savings in space you get is worth the sacrifice of readability here.  
 - Each song has an even amount of pages (2, 4, 6 or in extreme cases 8 and above)
 - Every song comes with `\gtab`s, meaning every song contains **all** guitar chords _used in that song_ as a picture like the one below: 

   ![Picture of a G-Major](build/img/gmaj.png) 

   Luckily, pictures like this can be generated using the songs package. For instance, the G-major-chord shown here can be created using the following code: `\gtab{G}{320033}`. For further information please see the documentation of the songs package itself [LaTeX Songs Package Documentation](http://songs.sourceforge.net/songsdoc/songs.html). 
 - Please please please sort all guitar chords alphanumerically. As an example, assume we had a song using an A-Major, A-Minor-7th, C-Major, D, D7, D# and D/F#. Then the order in which those chords ought to be listed is as follows: A, Am7, C, D, D7, D/F#, D#. Notice that the D# is at the very end, this is because the D-chord family is listed before the D#-chord family. Similarly, D/F# will be sorted _after_ D7, because alphanumerically, the 7 outranks the F#. Keep in mind that it does not really matter functionally how the chords are sorted, but it will be nicer if it is _consistent across all songs_.
 - Also as a quick side-note (pun intended), for the time beeing, we will not include intros and outros and no bridges in the songbook. If a song really needs a bridge, make it part of the chorus or part of the verse (for now). 

## Videos and documentation are inconsistent! 

If you don't know what this passage is, in short: I made a view videos where I talk about this stuff, showing examples. The videos are on YouTube, however they are not listed and I will not share the link publically. 
Now that you know, re-read the title of this section. 

In this case, the documentation here is right. This is because it takes a lot longer to make and re-make a video than to change up some words in a document like this. 


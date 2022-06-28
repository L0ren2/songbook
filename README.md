# songbook

This is the songbook template used by my local scout group. You are free to use and modify it.
Because this songbook is using the [LaTeX Songs Package](http://songs.sourceforge.net/), it is licensed under the GPL v2.0. 
The original songs package itself has not been modified for this purpose. 
If you are using this as your template please be sure to share your sources as well. 
Happy singing :)

## How to Install

### prerequisites

The chordbook assumes that you have installed a few general latex-packages for using latex. 
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

## Styleguide 

Generally I prefer the following layout: 
 - Every verse should be one line of code. This is why: That way, the songs package can work it's magic and put everything on the paper using a close-to-minimum amount of space. Now notice, I said "should". There are exceptions to the rule. For Instance, have a look at the following lyrics from "Junge" by "Die Ärzte": 
   ```
   ...
                 Dm                      Am
   Löcher in der Hose und ständig dieser Lärm
                   C
   (was sollen die Nachbarn sagen?)
   ...
   ```
In the given example it can make more sense to put the parenthesised part in its own line. For one, because it is sung as an echo to the first part, and secondly because it does not increase readability if it would not have its own line of song text, because the line would be too long and it would be broken up in two parts anyways. However, please note that in some songs it makes more sense to put such passages in one line with the rest. As an example consider this part from "Hit the road, Jack": 
```
 F        E7                 Am             G
Don't you come back no more. (aah! what you say)
 F        E7                 Am             G
Don't you come back no more. (I didn't understand you)

```
Here one line makes a lot of sense, because the line is short enough that it will not be broken in two. Also you have the same chords throughout the song in this exact sequence. Disrupting it by splitting it in two feels unnatural. As you can see it very much depends on the song. As a gerneral rule of thumb for most songs, putting every verse in one line is good advice. 

 - Each song has an even amount of pages (2, 4, 6 or in extreme cases 8 and above)
 - *Every* song comes with `\gtab`s, meaning ***every*** song contains ***all*** guitar chords *used in that song* as a picture like the one below: 

   ![Picture of a G-Major](build/img/gmaj.png) 

   Luckily, pictures like this can be generated using the songs package. For instance, the G-major-chord shown here can be created using the following code: `\gtab{G}{320033}`. Barchords can be produced like this: `\gtab{F}{(133211)}`. If you are using a barchord that is played in the 3rd, 5th or even above fret, use the following notation: `\gtab{Am}{5:(133111)}`. For further information please see the documentation of the songs package itself [LaTeX Songs Package Documentation](http://songs.sourceforge.net/songsdoc/songs.html). 
 - Please please please sort all guitar chords alphanumerically. As an example, assume we had a song using an A, Am7, C, D, D7, D# and D/F#. Then the order in which those chords ought to be listed is as follows: A, Am7, C, D, D7, D/F#, D#. Notice that the D# is at the very end, this is because the D-chord family is listed before the D#-chord family. Similarly, D/F# will be sorted _after_ D7, because alphanumerically, the 7 outranks the F#. Keep in mind that it does not really matter functionally how the chords are sorted, but it will be nicer if it is _consistent across all songs_.
 - Also as a quick side-note (pun intended), for the time beeing, we will *not* include intros and outros and no bridges in the songbook. If a song really needs a bridge, make it part of the chorus or part of the verse (for now). 
 - If your song has a really long chorus, please make it an additional verse instead, because the songbook is better at correctly breaking pages with verses than with choruses. 
 - If your song has more than one chorus (e.g. pre-chorus and chorus), either merge both choruses to one chorus or merge the relevant verses with the first part of the chorus and then use the rest of the chorus normally. That way, we end up with a practical amount of used ink and paper. 
 - If your song is longer than two pages, please make sure that the guitarist can still play the chorus without having to flip pages every verse. This means that you should have your chorus printed on every 1st, 3rd, 5th and so on page. 

## Videos and documentation are inconsistent! 

If you don't know what this passage is, in short: I made a few videos where I talk about this stuff, showing examples. The videos are on YouTube, however they are not listed and I will not share the link publically. 
Now that you know, re-read the title of this section. 

In this case, the documentation here is right. This is because it takes a lot longer to make and re-make a video than to change up some words in a document like this. 


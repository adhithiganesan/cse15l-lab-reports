# **Week 4 Lab Report**
*By: Adhithi Ganesan*



## Bug 1 ##

![Image](vscode6.1)


[Link to test file](testfile1)

Output was "facebook.com, instagram.com, url.com" but this is incorrect because url.com is a link for an image not an actual link.

The program would return links for images along with the actual links it was supposed to return. This showed that there was a bug in the code with identifying regular links versus image links. 

## Bug 2 ##

![Image](vscode6.2)

[Link to test file](testfile2)

Output was "ucsd.edu" but this is incorrect because "canvas.ucsd.edu" should've also been included. 

The program skipped over links that are in quotation marks. This revealed a bug in how it cannot detect links that are in quotation marks. 

## Bug 3 ##

![Image](vscode6.3)

[Link to test file](testfile3)

Output was something.com but this is incorrect because something.com should have been outputted twice since there are two links present.

The program skips over links that aren't properly enclosed in parentheses. This revealed a bug in how the program identifies links (by looking for brackets and parentheses) and changes were made. 


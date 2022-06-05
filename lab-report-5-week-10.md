# Week 10 Lab Report
*By: Adhithi Ganesan*

I found the tests by manually searching through the testfiles file in the MarkdownParse github repository and choosing ones I know would reveal bugs in my code. 

Test #223:
[Link to the first test file in repository](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/223.md)

Test #548:
[Link to second test file in repository](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/548.md) 

## Test #223: ##

Nidhi's MarkdownParse had the correct implementation and my MarkdownParse did not. 

Nidhi's MarkdownParse implementation output:
![Image](week10)
My MarkdownParse implentation output:
![Image](week10.1)
Expected Output:
``` [] ``` 

My implementation failed because I did not include an if statement on what to return if it were to encounter a file that doesn't have "!" since that is used as an indicator as to where the link begins. I could fix my code by including an if statement that says if the indexOf("!") < 0, return toReturn. 

![Image](week10.2)
I could include the if statement right before or after the first if statement within the while loop. 

## Test #548: ##

Nidhi's MarkdownParse had the corrrect implementation and my MarkdownParse did not. 

Nidhi's MarkdownParse implementation output:
![Image](week10.3)

My MarkdownParse implentation output:
![Image](week10.4)

Expected Output:
``` [] ``` 

My implementation failed because I didn't include an if statement on what to reutrn if it didn't encounter a "!" or when to stop parsing. Because there was no "!" in the test file, it kept parsing and ran into an index out of bounds error. I could fix my code by including an if statement that says if the indexOf("!") < 0, return toReturn. 

![Image](week10.2)
I could include the if statement right before or after the first if statement within the while loop. 
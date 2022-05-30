# Week 8 Lab Report
*By: Adhithi Ganesan*

[Link to my Markdown-Parse repository](https://github.com/adhithiganesan/markdown-parser)

[Link to repository I reviewed during week 7](https://github.com/KristinEbu/markdown-parser)

# Expected Results of Test of Each Snippet:

Snippet 1: 
![Image](snippet1expected)

Expected Output for Snippet 1:
```[`google.com, google.com, ucsd.edu]```

Snippet 2: 
![Image](snippet2expected)

Expected Output for Snippet 2: 
```[a.com, a.com(()), example.com]```

Snippet 3:
![Image](snippet3expected)

Expected Output for Snippet 3:
```[https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]```

# Code in ```MarkdownParseTest.java``` for tests:
![Image](snippettestscode)

I created new md. files with the snippets and called the ```getLinks()``` method on the file and compared it to the expected String List using a JUNIT test. 

# JUnit Tests on my MarkdownParse Implementation:
![Image](Junit8mine)

# JUnit Tests on the implementation I reviewed:
![Image](Junit8other)


# Questions
## **Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.**

Yes, you create a variable to keep count of the backticks and if there is an even number of backticks, or if for every open backtick there is a closing backtick, then you can ignore them. If not, you can choose to increment the currIndex a backtick. 

## **Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.**

I think this would require more than 10 lines and would be a more involved change since there are a lot fo combinations that nest parentheses, brackets, and escaped brackets. And seeing that the current code uses openParen and closeParen to identify the start and end of links, dealing with nested parentheses might prove to be difficult since we don't know which ones to skip over. 

## **Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.**

Yes, I think an if statement could be used so that the program goes to the next line if it encounters newlines in brakcets and parantheses. It could just skip lines until it identifies the index of the first openParen and then start reading links from there. 





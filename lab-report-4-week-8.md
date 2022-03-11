[My markdown-parse repository](https://github.com/eunkjm/CSE15L-RoseateSpoonbill)
<br />[Reviewed repository](https://github.com/Shree-G/markdown-parse)

# snippet 1
According to the [CommonMark demo site](https://spec.commonmark.org/dingus/), 
<br />``[another link](`google.com)`, [`cod[e`](google.com), [`code]`](ucsd.edu)``
<br />are considered as links.

**Test implemented in my markdown-parse:**

![image](snippet1.jpg)
![image](failedsnippet1.jpg)

**code fix**:
For snippet 1, I think there is a way to make the test to pass with less than 10 lines of code change. It seems like the difference between the valid and invalid links is whether or not the pair of backticks is enclosed within the openbracket and closebracket, which my codes failed to recognize. Using the if statement with indexes of the backticks and the brackets, I could check if the backticks are inside of the brackets. Pair of matching backticks are needed if there is any additional brackets inside of the openbracket and closebracket. Otherwise, it seems like the number of backticks and whether or not it has a matching pair don't matter as long as they are all enclosed by the openbracket and closebracket(else statement).

**In the reviewed repository:**

![image](snippet1.1.jpg)
![image](snippet1failure.jpg)

# snippet 2
According to the CommonMark demo site,
<br />`[nested link](a.com), [a nested parenthesized url](a.com(())), [some escaped \[ brackets \]](example.com)`
<br />are considered as links.

**Test implemented in my markdown-parse:**

![image](snippet2.jpg)
![image](failedsnippet2.jpg)

**In the reviewed repository:**

![image](snippet2.1.jpg)
![image](snippet2failure.jpg)

# snippet 3
According to the CommonMark demo site, only
<br />`[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)`
<br />is considered as a link

**Test implemented in my markdown-parse:**

![image](snippet3.jpg)
![image](failedsnippet3.jpg)

**In the reviewed repository:**

![image](snippet3.1.jpg)
![image](snippet3failure.jpg)



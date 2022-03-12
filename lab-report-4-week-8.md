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
<br />For snippet 1, I think there is a way to make the test to pass with small code change. It seems like the difference between the valid and invalid links is whether or not the backtick is enclosed within the nextOpenBracket and nextCloseBracket, which my codes failed to recognize. Using the if statement with the indexes, I could check if the backticks are inside of the brackets. If there is additional non-matching brackets inside of the nextOpenBracket and nextCloseBracket, matching pair of backticks need to enclose it. Otherwise, it seems like the number of backticks and whether or not it has a matching pair don't matter as long as they are all enclosed by the nextOpenBracket and nextCloseBracket(else statement).

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

**code fix:**
<br />For snippet 2, I think it can be fixed with small code change. Similar to the test failure for the last link from snippet 1, it seems like my code failed to recognize a valid link that contains closebrackets inside of the nextOpenBracket and nextCloseBracket: `[some escaped \[ brackets \]](example.com)`. The difference between this link and the link from snippet 1 is that snippet 2's link has a matching pair of close and openbrackets instead of one closebracket. Using the if statement, I could check if there is matching pair of brackets inside and recognize the valid link.
Also, for the nested parentheses fix, I could add another if statement to check if there is additional closing parenthesis, so it would be involved in the url list instead of being cut off after the code finds its first closeParen.

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

**code fix:**
<br />For snippet 3, I think it can be fixed with a small code change. It seems like my code fails to recognize two seperate invalid links(third and the last) but rather combined them into one url with valid link. This issue can be fixed by checking if there is more than one newline inbetween the openParen, url and closeParen(which results in an invalid link.) The links without the closing parenthesis after more than one newline will also be invalidated with this fix.

**In the reviewed repository:**

![image](snippet3.1.jpg)
![image](snippet3failure.jpg)



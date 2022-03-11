[My markdown-parse repository](https://github.com/eunkjm/CSE15L-RoseateSpoonbill)
<br />[Reviewed repository](https://github.com/Shree-G/markdown-parse)

# snippet 1
According to the [CommonMark demo site](https://spec.commonmark.org/dingus/), 
<br />`[another link](`google.com)`, [`cod[e`](google.com), [`code]`](ucsd.edu)``
<br />are considered as links.

**Test implemented in my markdown-parse:**

![image](snippet1.jpg)
![image](failedsnippet1.jpg)

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



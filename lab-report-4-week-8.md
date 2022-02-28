[My markdown-parse repository](https://github.com/eunkjm/CSE15L-RoseateSpoonbill)\
[Reviewed markdown-parse repository](https://github.com/Shree-G/markdown-parse)\

# snippet 1
According to the [CommonMark demo site](https://spec.commonmark.org/dingus/), 
> [another link](`google.com)`
> [`cod[e`](google.com)
> [`code]`](ucsd.edu)

are considered as links.

**Test implemented in my markdown-parse:**
![image](snippet1.jpg)
![image](failedsnippet1.jpg)

# snippet 2
According to the CommonMark demo site,
> [nested link](a.com)
> [a nested parenthesized url](a.com(()))
> [some escaped \[ brackets \]](example.com)

are considered as links.

**Test implemented in my markdown-parse:**
![image](snippet2.jpg)
![image](failedsnippet2.jpg)



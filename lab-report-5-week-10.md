# Different Results

Using the diff command, I compared and contrasted the two url lists:

![image](diff.jpg)

After looking through the output, I chose 495.md and 577.md for the evaluation.

## 495.md
According to the [CommonMark demo site](https://spec.commonmark.org/dingus/), the expected output for 495.md is `[foo(and(bar))]`

![image](880.jpg)

The provided markdown-parse had the correct output while my MarkdownParse implementation returned an empty list.

**Bug:**
<br />I found out that my implementatation returned the empty list as an output because it didn't reach line 40.
The index of the first OpenBracekt was 0 and the index of "!" was -1 since it wasn't found in the file. One of the conditions for if statement in line 37 specified that the index of "!" shouldn't equal 0 - 1 = -1 which was not met, hence the output was '[]'
However, the output would still not be correct even if the index bug was fixed, because the 



## 577.md

Since the format of the file was an image, the expected out is an empty list, `[]`

![image](880.jpg)

This time, my MarkdownParse returned the correct output while the provided markdown-parse failed to differentiate an image format from a link format.

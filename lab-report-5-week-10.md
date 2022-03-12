Since I coudln't figure out how to access an individual file in different directory 'test-files', I used the whole directory to run the MarkdownParse java file.
The url list output was saved into a results.txt file so I could access the list anytime after it was created. I picked two test files by looking through the results.txt which were 493.md and 494.md.

Then, I created the two test files with the same content in my repository, so I could read in the files and run my MarkdownParse java file.
Since I only had two files to check, I manually compared and contrasted the two outputs from 493.md and 494.md.

I wasn't sure of what was considered as valid link to implement a Junit test, so I used https://spec.commonmark.org/dingus/ to verify the valid links.
For 493.md, both implementations failed to only list valid link: `[a](c)`
For 494.md, only the provided markdonw-parse successfully recognized the valid link: `[link](\(foo\))`
 My markdown-parse implementation returned an empty list.

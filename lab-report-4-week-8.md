# Lab Report 4
---
## Repository Links
- [My markdown-parse](https://github.com/rinakaura/markdown-parse)

- [Reviewed markdown-parse](https://github.com/Darrengn/markdown-parse)

---
## Snippet 1

According to VSCode Preview, this file should produce `google.com, google.com, and ucsd.edu. The first line should not be a valid link.
Test:

![Image](snip1test.png)

JUnit output for my markdown-parse(failure):
![Image](snip1junit.png)

JUnit output for reviewed markdown-parse(failure):
![Image](r-snip1junit.png)

---
## Snippet 2

According to VSCode Preview, this file should produce a.com, a.com(()), and example.com.
Test:

![Image](snip2test.png)

JUnit output for my markdown-parse(failure):
![Image](snip2junit.png)

JUnit output for reviewed markdown-parse(failure):
![Image](r-snip2junit.png)

---
## Snippet 3

According to VSCode Preview, this file should produce https://www.twitter.com, https://ucsd-cse15l-w22.github.io/, and https://cse.ucsd.edu/.
Test:

![Image](snip3test.png)

JUnit output for my markdown-parse(failure):
![Image](snip3junit.png)

JUnit output for reviewed markdown-parse(failure):
![Image](r-snip3junit.png)

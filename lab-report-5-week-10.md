# Lab Report 5
---
## Tests With Different Results
- To find the tests with different results, I cd'ed into my markdown-parse directory (named 'md4') and directed the bash output to a file called results.txt, then repeated those steps for the lab 9 markdown-parse directory (named 'lab9'). After that, I used diff to find the tests with different outputs. The commands were as follows:
```
$ cd md4
$ bash script.sh > results.txt
$ cd
$ cd lab9
$ bash script.sh > results.txt
$ cd
$ diff md4/results.txt lab9/results.txt
```

The results from diff were as follows:
![Image](newdiff.png)

## Test 1: 194.md
![Image](newdiff1.png)
Difference on line 212 of the results.txt files which corresponds with 194.md
![Image](194md.png)
My Output: []
The Professor's Output: [url]

To find the expected output, I used the [Commonmark Parser](https://spec.commonmark.org/dingus/) and looked at the HTMl tab to find the link destination.
![Image](linkdest.png)

Expected Output: [my_(url)]

Neither markdown-parse directory produced the correct output.
Bug:

## Test 2: 201.md
![Image](newdiff2.png)
Difference on line 230 of the results.txt files which corresponds with 201.md
![Image](201md.png)
My Output: []
The Professor's Output: [baz]

To find the expected output, I used the [Commonmark Parser](https://spec.commonmark.org/dingus/) and looked at the HTMl tab to find the link destination.
![Image](nolinkdest.png)

Expected Output: []
My markdown-parse directory produced the correct output.
Bug: 

For each test:
Describe which implementation is correct, or if you think neither is correct, by showing both actual outputs and indicating what the expected output is.
For the implementation that’s not correct (or choose one if both are incorrect), describe the _bug (the problem in the code). You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed.

## Change 1

![Image](change1.png)

[Test-file with no parentheses](woohoo.md)

Symptom:
![Image](symptom1.png)

This file contains a link without parentheses (failure-inducing input), so MarkdownParse should have returned an empty arraylist, given that the link was not formatted properly. Instead, MarkdownParse returned a StringIndexOutOfBoundsException (symptom). We found that the cause of the symptom was that the .indexOf() function returned -1 because it could not find the opening parenthesis (bug), so we added an if statement to ensure that the code would only search for a link if the markdown file had an opening parentheses.

---
## Change 2

![Image](change2.png)

[Test-file with no brackets](ms.md)

Symptom:

![Image](symptom2.png)

This file contains a link without brackets (failure-inducing input), so MarkdownParse should have returned an empty arraylist, given that the link was not formatted properly. Instead, MarkdownParse returned the given link (symptom). We found that the cause of the symptom was that the code still looked for the link, regardless of whether brackets were present or not (bug), so we added an if statement to ensure that the code would only search for a link if the markdown file had an opening bracket.

---
## Change 3

![Image](change3.png)

[Test-file with spacing](cs1.md)

Symptom:
![Image](symptom3.png)

This file contains a link with a large space between the link tag and the parentheses with the link (failure-inducing input), so MarkdownParse should have returned an empty arraylist, given that the link was not formatted properly. Instead, MarkdownParse returned the given link (symptom). We found that the cause of the symptom was that the code did not account for the presence of spaces (bug), so we added an if statement around toReturn.add() to ensure that the code would only add a link to the arraylist if there was no space between the closing bracket and open parentheses.

---
layout: essay
type: essay
title: "Coding Standards"
# All dates must be YYYY-MM-DD format!
date: 2024/9/25
published: true
labels:
  - ESLint
  - VSCode
  - Typescript
---

## My Thoughts On Coding Standards And ESLint

I think coding standards as a whole are very hit or miss in their usefulness and something like ESLint which enforces those standards is more harmful than helpful. Some standards such as starting on new line after each action (i.e. Hitting enter after a semicolon in Java) make a lot of sense and should be universally used because they help with readability of the code. On the other hand some of the coding standards enforced by ESlint such as spaces between something and parenthesis or brackets do nothing to improve the readablity of the code and can actually make it harder to find real errors in the code. Looking down at the picture below the first one complies with ESLint standards and the second one breaks those standards in 3 places. The code will run if compiled for both pictures. The least egregious error is on line 25 with a one space wide red squiggle because there is no empty line at the end of the code. This error is not really causing any problems with finding real errors but on the flipside adding that empty line does nothing to actually improve readability. Looking at line 19 the entire comment has a red squiggle because there is not a space between the // and the text. Adding that space really does nothing to change the readability of the comment so one could argue that there is no real problem with adding the space but as someone who has been coding for at least 5 years without adding spaces between the // and the text of a comment it is annoying that I am now required to add the space if I want to get rid of the squiggle. The final error is where I have a real problem with ESLint. Everything between the curly brackets on lines 20 and 23 has a red squiggle because there is not a space between the first curly bracket and the parenthesis in front of it. So there could be a multitude of errors in that function and you would never know because of that one missing space. 

<img width="500px" class="rounded float-start pe-4" src="../img/Screenshot 2024-09-25 102632.png">

<img width="500px" class="rounded float-start pe-4" src="../img/Screenshot 2024-09-25 102700.png">

All of these errors could be fixed in less than 5 seconds and at least for VSCode, one could simply hover over the squiggles and click the button fix all auto-fixable errors and it would fix all 3 things at the same time. So one might ask, what is the problem? The problem is every person who has ever coded has a different preference for how they like their code to look and these examples are just the tip of the iceberg for ESLint. I like seperating code with empty lines especially when working with very large amounts of code and ESLint has a big problem with extra empty lines (except the empty lines they want in places they are unneeded). Someone else might think there should be no empty lines anywhere in a piece of code. So who determines which preference is correct? And this is where the real problem with ESLint lies. Since the code will run fine no matter what I could just let the errors exist in my code but as mentioned earlier then I can't see when actual code breaking errors occur. But if I keep my code ESLint compliant it could be harder for me to read it. To sum things up yes coding standards can be helpful but no they should not be enforced by things like ESLint. 

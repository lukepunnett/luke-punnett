---
layout: post
title: A strategy for solving algorithmic problems
description: When stuck how on how to tackle problems - follow these steps.
image: assets/images/pic03.jpg
---

**PreReq:** As a start be comfortable with the very basics of your chosen programming language. Some good things to know really well:
- Conditionals
- Looping
- String Manipulation
- Arrays and other collections, particuarly lists and maps

**Requirements Phase:**

**Design Phase:**
1) Think through the general case - can you write it out in pseudocode or explain it to somebody. 
2) Think through the edge cases that might not fit your general solution. This will largely be nulls, lists with only one item in, when you get to the last item of lists etc. Once you know these cases you can think through how to handle them. Most often this will be additional additionals at the beginning or end of your solution to catch these special cases and it shouldn't necessarily cause significant change to your design. 

**Implementation Phase:** 
1) Functions and Data Structures
2) Take time to check code. 
3) Test / Check / Run
4) Debug, Adjust and Repeat.
5) Optimise - As you get more confident you can move this step earlier in the process and you can optimise it as part of the design. Nearly all problems within IT are a trade off and recognising this really helps when optimising - these optimisations can be broken down into 2 broad categories:
    - General Optimisation: This is essentially following general, clean code best practices. Making sure you haven't unessecarily complicated the code, that naming conventions have been adhered too. 
    - Specific Optimisations: Here we come back to the trade offs. The two most common trades off are optimising for time or space. Sometimes iterating an array and storing the indices, values and more in a more complex data structure may take a lot of memory but it really allows you to optimise for time and not loop through an array many many times. 

Trick for optimising: 
- Try take things to an extreme in your head to really stretch the algorithm and then pretend you had to do it by hand. The following example shows a smart way of breaking early:

Palindrome first pass:
*"To check a word is a palindrome, I would start with the first letter and check that matches the last letter, then I would check the second letter and second to last. I would do this until I reached the middle of the word and then I could definitely prove whether or not it was a palindrome."*

This approach certainly works, and for simple test words even humans could do it quickly. However when stretched to a dictionary it can take a very long time if the loop isn't broken on finding the first mismatch. In theory you could prove the entire works of shakespeare isnt a palindrome with a single check. When interviewing junior and mid developers, I would say some 30% of individuals made the mistake of not breaking in time, even with this simple problem.

**Post:**
1) Time to do final review


**Other**
- TDD, Test Driven Development
- Clean Code or Best Practices when Coding.


# Lab Report 5
## Part 1 – Debugging Scenario


## 1.Student Piazza Post 
![Image](studentpiazzaa.jpg)


The code and error jpg's attached in the Piazza post
![Image](studenterrorcode.jpg)
![Image](studenterror.jpg)




## 2.Response from a TA 
![Image](piazza.jpg)

## 3.  Terminal output showing what information the student got and clear description of the bug
![Image](fixbug.jpg)
I identified the bug was caused by the merge method being called on the incorrect class. The bug inducing `TestListExamples` was  calling the merge method on `TestListExamples`. To fix this, I change line 17 to ` List<String> merged = ListExamples.merge(left, right);`. Here, the merge method is being called on `ListExamples`. It is correct to call `merge` on the `ListExamples` class because that is where it is defined. 


## 4. Information needed about the setup

```
              list-examples-grader
              │
              ├── GradeServer.java
              ├── Server.java
              ├── TestListExamples.java
              ├── grade.sh
              │
              ├── grading-area
              │   ├── IsMoon.class
              │   ├── ListExamples.java
              │   ├── ListExamples.class
              │   ├── StringChecker.class
              │   ├── TestListExamples.class
              │   ├── TestListExamples.java
              │   └── lib
              │
              └── student-submission
```

-The contents of each file before fixing the bug
![Image](testlist.jpg)
![Image](list-examples-grader.jpg)
![Image](Server.jpg)
![Image](ListExamples.jpg)




-The full command line (or lines) you ran to trigger the bug: `bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-corrected`

-A description of what to edit to fix the bug: I edited line 17 in the `TestListExamples`  file from week 6. The failure inducing code was `List<String> merged = TestListExamples.merge(left, right);`. Which I then edited to be, `List<String> merged = ListExamples.merge(left, right);`

## Part 2 - Reflection 
Something cool I learned is that I can use `man` or `--help` in the command line to learn more about a specific command. I used this for vim and `grep` in the second half of the quarter. I think that this is a really quick and useful way of learning more about commands. 

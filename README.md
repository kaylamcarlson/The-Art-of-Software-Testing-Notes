# The Art of Software Testing Notes
## Chapter 2
- QA testing is about rasing the quality and reliability of the program.
- Always start with an assumption there will be errors.
- Best defined as "Testing is the pprocess of executing a program with the intent of finding errors.
- Due to human psychology, if our goal is to show no errors we are less likely to find error, or try tests that will provide errors.
- Calling a test that finds no errors sucessful is backwards thinking. You wouldnt call a visit to a doctor where they preform a test that gives no results a sucess. A better way of looking at it is that a test that resuts in errors is a sucess.
- It is impossible to catch all errors and people are less motivated to try things they know are impossible, look at it as a process of uncovering as many errors as possible.
- Programs that seem to be working can still havce bugs with them.
- Use testing to have a degree of confidence that a program doesnt have bug, but also does what it is intended to do.
- Always have a defined expected outcome as well as input.

#### Black Box Testing
This is input output driven testing. You are not focued on the inner workings of the program. Test data is centered around the specifications of the program. Maxamise the number of errors found with a finite number of tests as it is impossible to test till 100% error free.

#### White Box Testing
This is looking at the internal structure of a program. Program paths are important to test. A program can work however it maybe using paths not intended or paths could be missing. 

#### Key Testing Guidelines
1. You have to define for each test case an expected outcome/result.
dont define expected outcomes and results.
1. Whoever wrote the program is better off not being the one to test it.
1. If possible a company should not test their own programs, so as to be as netural as possible.
1. Each result should be inspected as it can lead to other errors.
1. Test cases need to be preformed on not only unexpected conditions but also for ones the program is meant to produce.
1. It is a 2 sided battle. One side is testing for errors. The other side is testing to see it does what it was designed for.
1. Do not plan testing around an assumption you will find no errors.
1. The probability of more errors in a program is usually in line with the number of errors already found.


## Chapter 3
- Human testing techniques are quite effective.
- The earlier errors are found the easier and less costly they are to fix.

#### Inspections and Walkthroughs
- They invole a team of people reading through the code with a goal to find errors, not fix them.
- Advantages include being able to locate an error precisely in the code instead of waiting till the testing stage where errors are thrown and you then need to search the code to find the issue.
- Human testing can be more effiencet at find errors then computer based testing expect for high level design errors etc. errors in requirements analysis process.
- Program modification is often more error prone then writing a new program so modifications should always be tested. 
- Reading code aloud, line by line is an effective error detection method. 
- Errors found are used to improve on an error checklist.
- 90-120 minutes is the optimal time spent reviewing code.
- The human attitude is very important. If ego is not put aside then the work will not be improved upon.
- Many errors are found through questioning the programmer in a walkthough instead of through the test cases.
- Peer reviews are useful to improve upon programs and test for errors. People volunteer programs to be tested and they each test each others for 30 minutes then fill out a feedback form.
- Any errors are not seen as a weakness on the programmers part, they should be looked at as just a result of the difficulty of the program itself.


## Chapter 4
- Branch coverage, each test case has a true and false outcome at least once. Otherwise described as each branch direction being travelled twice.
- Decision/ condition coverage does not exercise all outcomes of all conditions.
- All points of entry need to be invoked at least once.
- Each test case should test as many different input considerations as possible to minimize the total number of tests needed. 

#### Equivalence
- Fair assumption errors will be handled the same for test cases within the same class
- Divided up by taking the inputs and dividing them between 2 groups or more
- 2 types of classes are valid and invalid.
- Form of Black Box testing.
- Make sure to test all areas of the program as if it fails at the first check, it is unlikely to check for other errors. E.G if 1==1
else 3==3. If 1 is not equal to 1 then it might throw and error and not check what 3 is equal too.

#### Boundry Value Analysis
- Testing the outer bounds of a range
- If a program has ranges, test both the ends (maximum and minimum) and just beyond eg -1 and 1 or -1.01 and 1.01
- If used correctly it is one of the most useful test case design methods.

#### Cause-Effect Graphing
- Explores combinations of input circumstances e.g. 2 inputs excede a maximum limit of something like memory. 
- Must divide it into workable pieces as otherwise is can get out of uncontrol for large scale programs.

#### Error Guessing
- No method to this, just using experience and intuition to seek out errors. Normally commonly occuring ones.

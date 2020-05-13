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

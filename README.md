# The Art of Software Testing Notes
## Chapter 2
- QA testing is about raising the quality and reliability of the program.
- Always start with an assumption there will be errors.
- Best defined as "Testing is the process of executing a program with the intent of finding errors".
- Due to human psychology, if our goal is to show no errors we are less likely to find errors, or try tests that will provide errors.
- Calling a test that finds no errors successful is backwards thinking. You wouldn't call a visit to a doctor where they perform a test that gives no results a success. A better way of looking at it is that a test that results in errors is a success.
- It is impossible to catch all errors and people are less motivated to try things they know are impossible, look at it as a process of uncovering as many errors as possible.
- Programs that seem to be working can still have bugs with them.
- Use testing to have a degree of confidence that a program doesn't have bugs, but also does what it is intended to do.
- Always have a defined expected outcome as well as input.

#### Black Box Testing
This is input output driven testing. You are not focused on the inner workings of the program. Test data is centered around the specifications of the program. Maximize the number of errors found with a finite number of tests as it is impossible to test until the program is 100% error free.
 
#### White Box Testing
This is looking at the internal structure of a program. Program paths are important to test. A program can work however it may be using paths not intended or paths could be missing.
 
#### Key Testing Guidelines
1. You have to define for each test case an expected outcome/result.
1. Whoever wrote the program is better off not being the one to test it.
1. If possible a company should not test their own programs, so as to be as neutral as possible.
1. Each result should be inspected as it can lead to other errors.
1. Test cases need to be performed on not only unexpected conditions but also for ones the program is meant to produce.
1. It is a 2 sided battle. One side is testing for errors. The other side is testing to see it does what it was designed for.
1. Do not plan testing around the assumption that you will find no errors.
1. The probability of more errors in a program is usually in line with the number of errors already found.

## Chapter 3
- Human testing techniques are quite effective.
- The earlier errors are found the easier and less costly they are to fix.
 
#### Inspections and Walkthroughs
- They involve a team of people reading through the code with a goal to find errors, not fix them.
- Advantages include being able to locate an error precisely in the code instead of waiting till the testing stage where errors are thrown and you then need to search the code to find the issue.
- Human testing can be more efficient at finding errors than computer based testing except for high level design errors etc. errors in the requirements analysis process.
- Program modification is often more error prone then writing a new program so modifications should always be tested.
- Reading code aloud, line by line is an effective error detection method.
- Errors found are used to improve on an error checklist.
- 90-120 minutes is the optimal time spent reviewing code.
- The human attitude is very important. If ego is not put aside then the work will not be improved upon.
- Many errors are found through questioning the programmer in a walkthrough instead of through the test cases.
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
else 3==3. If 1 is not equal to 1 then it might throw an error and not check what 3 is equal to.
 
#### Boundary Value Analysis
- Testing the outer bounds of a range
- If a program has ranges, test both the ends (maximum and minimum) and just beyond eg -1 and 1 or -1.01 and 1.01
- If used correctly it is one of the most useful test case design methods.
 
#### Cause-Effect Graphing
- Explores combinations of input circumstances e.g. 2 inputs exceed a maximum limit of something like memory.
- Must divide it into workable pieces as otherwise it can get out of uncontrol for large scale programs.
 
#### Error Guessing
- No method to this, just using experience and intuition to seek out errors. Normally commonly occurring ones.

## Chapter 5
- Large programs require a different approach. Something called Module Testing.
- You focus on testing sub programs, routines, classes and procedures.
- It is largely a Whitebox testing method.
 
#### Incremental Testing
- Testing each module independently then combining them is called nonincremental.
- Combining modules together both to be tested and previously tested ones is called incremental testing and it is superior.
- Debugging is easier if incremental testing is used and testing is more thorough.
- It can be unwise to test early modules in a program if it is still being developed. As they program further they may decide to change areas of the top code and it may not be tested again if it was already tested at an earlier stage.
Top down vs bottom up testing each have advantages and flaws, however bottom up has the advantage due easier observations and creation of test conditions.

## Chapter 6
- Many software errors are caused by breakdowns, mistakes or noise during the communication and translation of information.
- The software development process goes through 7 stages:
1. End user: Define users needs into written requirements. This is the goal of the program.
1. Requirements: Requirements become specific objects. Feasibility, cost, time, conflicts, trade-offs and priorities are taken into account.
1. Objectives/ External Specification: Translate objects into precise product specifications. Only looking at interfaces and interactions with the end user.
1. System Design: If it is a database system instead of an application then it needs to be divided into individual programs, components and sub-systems. Defining their interfaces.
1. Program Structure Design: specify the function of each module, the hierarchy and the interfaces between modules.
1. Module Interface Specifications: Define the interface and function of each module.
1. Code: Translate all this into code.
 
Requirements: Specify why a program exists

Objectives: What the program should do and how well.

External Specifications: Define representation of the program to users.

Documentation: Subsequent processes have documentation in high detail, how the program is constructed.

- Three methods can be used during this to prevent and detect errors. More precision in development. Verification step at the end of processes before moving on or orient distant testing process to distant development processes.
#### Module tests
- Find discrepancies between modules and their interface specifications
- Black box testing on small programs.
- Analyze the specs to come up with test cases.
#### System Testing
- Compare the system to its original objectives.
 
#### Facility Testing
- Look to see if each function or objective that was specified was implemented.
 
#### Volume Testing
- Subject the program to a heavy amount of data at one time.
- Don't go overboard as it takes a lot of resources but you should still do a few volume tests to make sure it performs as well as specified during design.
 
#### Stress Testing
- This is subjecting the program to a heavy load for a short amount of time.
- Testing at what would be peak volume.
- Because it involves an element of time, it is not possible for many programs.
- E.g. Testing air traffic systems if designed for tracking 200 airplanes at once, test it further.
- For websites and web based applications during design you need to specify the volume of users you expect to be using it at any one time then design a test around that number.
 
#### Usability Testing
- This has become more important with GUI based systems.
- Focus on the user experience and what errors they could cause when interacting with an application or software.
 
#### Security Testing
- This centers around creating tests that bypass security.
- Study known security issues in similar systems and try to recreate them.
 
#### Performance Testing
- This checks the performance of software such as response times.
 
#### Storage Testing
- If a project has storage objectives it is important to test them.
- How much memory does it use? What is the size of the logs or files?
- Verify the program can control its memory usage.
 
#### Configuration Testing
- Does it run on all operating systems and devices?
 
#### Compatibility/Conversion Testing
- Most programs are not new, they are replacing an older version.
- You try to generate errors while trying to move data from one system to another.
- E.G. Does your new release support your existing data?
 
#### Installation Testing
- Making sure when an install occurs, no errors happen as first experiences can be everything for an end user.
 
#### Recovery Testing
- Testing the speed at which data can be recovered and making sure it brings everything back.
 
#### Documentation Testing
- Check accuracy and clarity of user documentation.
- Use the guide to write test cases.
 
#### Test Completion Criteria
- Two most common criteria is when testing time expires or all test cases are executed without detecting errors.
- Stopping after a certain amount of time is useless as you can do nothing and still satisfy that criteria. It does not mean the quality of testing is any good.
- We are goal orientated so testing all cases till no errors are detected will produce better tests.
- Another way to motivate through goal orientation is to look at testing not being complete until 70 errors are found or 3 months have passed. (However it is hard to estimate how many errors a program will have)
 
 
 
 

 
 
 
 
 
 
 
 
 
 


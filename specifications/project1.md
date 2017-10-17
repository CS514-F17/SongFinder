Project: Release 1 - Thread-Safe Music Library
==============================================

### Suggested Deadline Friday 11/10/2017

There is no specific deadline for release 1 of this project. When you are passing all test cases and believe you are ready for a code review you must *create a new release* on github. You will then undergo code review and will be asked to revise and resubmit your work until mastery is demonstrated. 

:warning: If you do not make early progress on this assignment you will not be able to complete the following requirements in order to pass this class:

1. You must demonstrate mastery of release 1 before moving on to release 2.
2. You must demonstrate mastery of releases 1 and 2 *and* complete all functionality requirements of release 3 in order to pass this course.
3. You may resubmit solutions *at most* once per week. 

## Overview ##

For release 1 of the project, you will extend Lab 3 to support concurrency. You must implement a thread-safe music library and use a work queue to build the library using multiple threads. Note that you will extend this to support search functionality in release 2.

The input and output requirements of this project are identical to Lab 3. In addition to the normal testing of Lab 3, you must also compare the execution time of this project to your previous code.

## Functionality ##

For this project, your code must pass all of the previous project requirements and support the following additional functionality:

- Create a custom lock class that allows multiple concurrent read operations, but does not allow concurrent write or concurrent read/write operations.

- Create a thread-safe music library using the custom lock class above.

- Use a work queue to build your music library from a directory of files using multiple worker threads. Each worker thread should parse a single json file.

- Exit gracefully without calling `System.exit()` when all of the building operations are complete.

- You may NOT use any of the classes in the `java.util.concurrent` package.

Consider extending your classes from previous projects for this project.

## Configuration ##

**Arguments - threads** - The value following the `-threads` flag will be an integer specifying the number of threads to use to build your music library. If `-threads` is not specified use a default value of 10. If it is specified, verify that it is an integer between 1 and 1,000. If it is a floating point number, `String`, or integer less than 1 or greater than 1,000 you may use a default value of 10. In no case should your program throw an exception as a result of an invalid value for the `-threads` argument.

An example run of your program would look as follows:

```
java Driver -input input/lastfm_subset
			  -output results/songsByArtistSubset.txt 
			  -order artist 
			  -threads 5
```			

## Output ##

The output of your program should be the same as Lab 3. 

## Hints ##

It is important to develop the project **iteratively**. One possible breakdown of tasks are:

- Consider extending your previous classes (e.g., `MusicLibrary`) to create multithreaded versions. You may need to add additional functionality to your single-threaded versions, but this tends to make the debugging process simpler.

- Create a thread-safe music library using the `synchronized` keyword. (Do not worry about efficiency yet.)

- Modify how you build your library to use multithreading and a work queue. Make sure you still pass the unit tests.

- Once you are sure this version works, convert your music library to use a custom lock class. Make sure you still pass the unit tests.

- Start worrying about efficiency. Make sure you are not under or over synchronizing, and that your multithreaded code is faster on average than your single-threaded code.

- Test your code in a multitude of settings and with different numbers of threads. Some issues will only come up occasionally, or only on certain systems.

- Lastly, do not start on this project until you understand the multithreading code shown in class. If you are stuck on the code shown in class, PLEASE SEEK HELP. You do not need to figure it out on your own—you can ask the CS tutors, the teacher assistants, or the instructor for help.

  :confused: I cannot stress this enough! If you do not understand the simpler examples shown in class, you will get sucked into a black hole of debugging for the project. We are here to help prevent this from happening.

The important part will be to **test your code as you go**. The JUnit tests provided only test the entire project as a whole, not the individual parts. You are responsible for testing the individual parts themselves.

:bulb: These hints may or may _not_ be useful depending on your approach. Do not be overly concerned if you do not find these hints helpful for your approach for this project.

## Benchmarking ##

The expected output files are identical to Lab 3.

You _must_ pass `Project1Test.java` to be eligible for code review. You may sign up for code review even if you are not passing `Project1ComplexTest.java`, but know that this means your code has efficiency issues.

## Submission ##
You must pass all of the `Project1Test` tests in order to qualify for code review.

Follow these instructions *carefully* in order to submit your project: [Project Submission Procedure](https://github.com/CS514-F17/notes/blob/master/Admin/projectsubmission.md)

### Submission Requirements

1. Use the `SongFinder` project you create for Lab 3 for this assignment. You do not need to create a new Eclipse project.
2. For full credit, make sure to follow all [Style Guidelines](https://github.com/CS514-F17/notes/blob/master/Admin/style.md). Points will be deducted for each violation.


### Grading Rubric

You may not move on to release 2 of this project until you have demonstrated mastery. 

:warning: As noted in the [Project Submission Procedure](https://github.com/CS514-F17/notes/blob/master/Admin/projectsubmission.md), you *may* receive deductions for failing to follow instructions or fix issues before resubmission.

In order to pass this class you **must** demonstrate mastery for Release 1 and Release 2 and you must pass all of the functionality tests for Release 3.


### Academic Dishonesty

Any work you submit is expected to be your own original work. If you use any web resources in developing your code you are strongly advised to cite those resources. The only exception to this rule is code that is posted on the class website. The URL of the resource you used in a comment in your code is fine. If I google even a single line of uncited code and find it on the internet you may get a 0 on the assignment or an F in the class. You may also get a 0 on the assignment or an F in the class if your solution is at all similar to that of any other student.

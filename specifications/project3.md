Project: Release 3 - Advanced Features
==============================================

### Suggested Deadline Monday 12/4/2017

There is no specific deadline for release 3 of this project. When you have implemented all functionality and believe you are ready for a code review you must *create a new release* on github. You will then undergo code review and will be asked to revise and resubmit your work until mastery is demonstrated. 

:warning: If you do not make early progress on this assignment you will not be able to complete the following requirements in order to pass this class:

1. You must demonstrate mastery of release 1 before moving on to release 2.
2. You must demonstrate mastery of releases 1 and 2 *and* complete all functionality requirements of *required features* for release 3 in order to pass this course.
3. You may resubmit solutions *at most* once per week. 
4. You must have an in-person code review, which must be scheduled with the instructor.

:warning: #2 above is slightly modified from previous project descriptions. If you do not complete the functionality of the required features you will not be eligible to pass this class. 

For this project, you will extend your previous project to support your choice of advanced features. To be eligible for any credit, you must implement all *required* features, worth 25 of 100 points. For the remaining 75 points you may select from the list of additional features specified. 

The points awarded for a *complete* implementation for each feature are noted below. An incomplete implementation, for example an implementation that does not handle all possible error cases, may only receive partial credit.

You are guaranteed only one code review during finals week. All code must be submitted to your git repository *and* your solution must be running on the microcloud before your scheduled code review.


## Required Features

Required features are worth 25 out of 100 points. 

It is expected that you will need to think carefully about to design each of these features and do some independent research on how to implement them. This is your chance to show me what you've learned this semester!

**View song info (5 points)** - On any search result page, allow the user to select a specific song and see information about that song, including the artist, title, and the list of a similar songs from the original data set.

**View all artists sorted alphabetically (5 points)** - Provide a menu option that allows the user to view an alphabetical list of all artists in the library.

**View all artists sorted by play count (5 points)** - Provide a menu option that allows the user to view a list of all artists in the library sorted by *play count*. The play count must be retrieved from the last fm API: [http://www.last.fm/api/show/artist.getInfo](http://www.last.fm/api/show/artist.getInfo). It is recommended that this information be retrieved once for all artists in your library and stored in the library or another data structure.

**View specific artist information (10 points)** - Allow the user to select a specific artist from a list of artists sorted alphabetically or by play count. Display specific information about that artist including the artist name, number of listeners, play count, and a bio. This information must be retrieved from the last fm API: [http://www.last.fm/api/show/artist.getInfo](http://www.last.fm/api/show/artist.getInfo). It is recommended that this information be retrieved once for all artists in your library and stored in the library or another data structure.

## Additional Features

**Artist image (5 points)** - When displaying the information about an artist, show an image of that artist. You will need to use the last fm API to implement this feature.

**Search history (15 points)** - Save a history of all searches performed by the user. You will need to design a solution for storing this per-user data. For full credit, allow the user to view his/her history and also clear his/her history.

**Private search (5 points)** - *You may only implement this feature if you also implement Search history.* Allow a user to turn on private search. If the user is in private search mode, do not save any searches to the search history.

**Login/Logout (10 points)** - Allow a user to log in to your service and log out of your service. If you implement this feature then Search history should track the history only when a user is logged in.

**Last visit time (5 points)** Track and display the last time the user visited your site. 

**Partial search (10 points)** - Allow the user to enter only part of an artist, title, or tag and return relevant results, for example the search for artist "Michael Ja" would return results for Michael Jackson.

**Case insensitive search (with case-sensitive results) (5 points)** - Ignore upper/lower case when searching, for example a search for "madonna" will return results for "Madonna". For full credit, the results displayed must show the data using the original case.

**Additional last fm APIs (10 points)** - Integrate other last fm APIs, for example top artist or track. The number of points awarded will depend on the sophistication of your implementation.

**Integrate other web services (10 points)** - Integrate other web services, for example login with Facebook.

**Branding (5 points)** - Brand your site with a logo, color scheme, etc.

**Suggested searches (10 points)** - Suggest popular searches, for example artist or title, based on all searches by all users in your system.

**Templates (5 points)** - Use StringTemplate to generate your HTML instead of several `println()` statements. See for [http://www.cs.usfca.edu/~parrt/course/601/lectures/stringtemplate.html](http://www.cs.usfca.edu/~parrt/course/601/lectures/stringtemplate.html) more information on StringTemplate.

**Graceful shutdown (10 points)** - Allow an administrator to trigger a graceful shutdown of your search engine without calling `System.exit()`. You will need to create a special servlet for this feature.

**Propose your own (up to 10 points)** - Propose your own feature during office hour. The instructor will tell you whether it is allowable and how many points it will be worth.

**Multithreaded last.fm client (2.5 points)** - Use a `WorkQueue` to use multiple threads to fetch content from last.fm concurrently.

**Pagination (7.5 points)** - On any page that contains a list of results, allow the user to view either 5, 10, or 25 results per page and then use a Next/Previous button or link to go to the next/previous page.

**Presentation (5 points)** - Present your web application to the class on Monday, 12/4. Your solution must be running on your assigned microcloud node and you must have at least the required features implemented.

**Admin Interface (up to 10 points)** - Create an administrator interface for your application. You will need to provide a way for an administrator to log in to your service. It is up to you to determine the functionality provided to the administrator. Your score on this portion will depend on the sophistication of the interface and functionality.

## Submission ##
You do **not** need to pass any unit tests for this project. You *may* remove the code that saves the `MusicLibrary` and the search output to a file.

Before you qualify for code review, we will verify that your site is up at your specified node and that it implements all of the required functionality specified above. If any functionality is missing or does not work as specified above, you will need to revise your solution before code review.

Follow these instructions *carefully* in order to submit your project: [Project Submission Procedure](https://github.com/CS514-F17/notes/blob/master/Admin/projectsubmission.md)

### Submission Requirements

1. Use the `SongFinder` project you created for Lab 3 for this assignment. You do not need to create a new Eclipse project.
2. For full credit, make sure to follow all [Style Guidelines](https://github.com/CS514-F17/notes/blob/master/Admin/style.md). Points will be deducted for each violation.

### Grading Rubric

In order to pass this class you **must** demonstrate mastery for Release 1 and Release 2 and you must implement the functionality of the required features for Release 3.

:warning: As noted in the [Project Submission Procedure](https://github.com/CS514-F17/notes/blob/master/Admin/projectsubmission.md), you *may* receive deductions for failing to follow instructions or fix issues before resubmission.

### Academic Dishonesty

Any work you submit is expected to be your own original work. If you use any web resources in developing your code you are strongly advised to cite those resources. The only exception to this rule is code that is posted on the class website. The URL of the resource you used in a comment in your code is fine. If I google even a single line of uncited code and find it on the internet you may get a 0 on the assignment or an F in the class. You may also get a 0 on the assignment or an F in the class if your solution is at all similar to that of any other student.


# JMeterTest

### Explain the following testing terms and account for their most important aspects:

#### The 4 system testing quadrants:

 ![Agile 4 quadrant](https://github.com/tjaydk/JMeterTest/blob/master/4agileQuadrant.jpg) 
 
The testing quadrants contain both business (user) and technology (developer) facing, either manual or automation or a combination of both. It is worth noticing that in Q3 andQ4 you need have software/code to test.
The four quadrants can be described as:

  •	Quadrant Q1 – Q1 is unit level contains unit Tests, technology facing, tests subject to full automation and continuous integration. The purpose here is to create quality software.

  •	Quadrant Q2 – Q2 is at system level, business facing, these are functional tests, examples, story tests, user experience prototypes, and simulations based on the acceptance criteria and can be manual or automated. The tests here is created as a part of definition of a story. The purpose here is to create value for the customer.

  •	Quadrant Q3 – Q3 is a system or a user acceptance level, business facing, contains tests exploratory testing, scenarios, process flows, usability testing, user acceptance testing, alpha testing, and beta testing. These tests are often manual and are user-oriented. The purpose here is to test users perception with the software product and get a review of the usability.

  •	Quadrant Q4 – Q4 is testing system or operational acceptance level, technology facing performance, load, stress, and scalability tests, security tests, maintainability, memory management, compatibility and interoperability, data migration, infrastructure, and recovery testing. These tests are often automated. The purpose here is to test the robustness of the system.


#### System testing:
System testing is a level of software testing where a complete and integrated software is tested. The purpose of this test is to evaluate the system’s compliance with the specified requirements.

##### Definition by ISTQB	(International Software Testing Qualifications Board)
  •	System testing: The process of testing an integrated system to verify that it meets specified requirements.

System testing is usually done with a black box testing methods. System Testing is performed after Integration testing and before acceptance testing. When doing a system testing you will look at the big picture, does the system meets the original intent.

#### Exploratory testing:
Exploratory testing is a way to test the application by exploring it to find what does the application do, its features , what it does not do etc. It requires no or minimal planning. Testers continuously make decision on his / her next step of action. With exploratory testing the test planing, analysis, design and test execution, are all done together and instantly. These things depends on the process. 

Exploratory testing requires rapid feedback on the issues faced and for any anomalies encountered. The purpose is it will give you an insight of the application and secondly, it may render some good defects.

#### Thoughts about the JMeter test results
##### Discount Test
|  | Error Percentage | Min time in ms | Average Time in MS |Max in ms |
|---|---|---|---|---|
| 10 tests | 0% | 230 | 263 | 326 |
| 100 tests | 0% | 222 | 255 | 426 |
| 1000 tests | 0% | 224 | 251 | 678 |

##### Interest Test
|  | Error Percentage | Min time in ms | Average Time in MS |Max in ms |
|---|---|---|---|---|
| 10 tests | 0% | 469 | 575 | 713 |
| 100 tests | 0% | 475 | 720 | 1510 |
| 1000 tests | 0% | 477 | 590 | 1191 |

We used a free hosted PHP server from [Heroku](https://www.heroku.com/).

As we can see from the results in the table, the difference between the min and max sample time does have some jumps, but the average time is pretty close to the fastest time. This shows that there is a good stability on the server. 
There are no errors or timeouts, so the non-functional requirement that one would expect of stability and speed are satisfied.
The only problem with the JMeter test is that It relays on the amount of threads possible to run on the system, and therefore can’t imitate the situation of 1000 concurrent request to the server.


Made by:
- Rune Vandall Zimsen
- Emil Rosenius Pedersen
- Dennis Michael Rønnebæk
- Ebbe Vig Nielsen

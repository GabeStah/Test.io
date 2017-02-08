# Functional Testing Tools Landscape

Functional testing is a critical component within the overall quality assurance process, and is necessary when developing an effective and stable final product.  While the basic concept of functional testing is simple, the implementation of performing modern functional testing often requires a variety of tools to handle everything from data generation and automation to test management and human testing.

Throughout this article we'll examine five key functional testing tools in greater detail, exploring the benefits of each and how these tools can directly benefit the testing needs of your next project.  

## Test Automation

One of the most well-known and oft-heralded tools of modern functional testing is the emergence of `test automation`.  The beauty of automated tests are that they allow developers and QA departments to easily design, write, execute, and review tests, which can then be automatically performed at will, whether that means prior to a new build release or even after ever minor code change is made.

One major benefit of automated tests is the ability define a series of pre-defined actions (such as pushing a set of users through the `CreateUser` procedure), then automatically performing those pre-defined actions at a rapid pace, before analyzing the output in comparison to the expected results.  Extrapolating this basic concept further and further -- throughout the code base of the entire application -- allows development teams to generate a breadth of automated functional tests that can be reused throughout the entirety of the software development life cycle.

Automated testing can also be used for certain tasks and comparisons that are largely infeasible for a manual tester.  For example, an automated test can often peek into the inner-workings of the code itself, examining the contents of memory, files, data sets, and states of execution to form a well-rounded analysis of the application's behavior during the test proceedings.

On the other hand, while automated functional tests provide the benefit of running tests against code or larger functional components automatically, these tests are also finicky, requiring some level of monitoring and maintenance from members of the team.

## Test Data Generators

As powerful as the practice of `test automation` can be, the success -- and therefore, the tangible benefit it provides -- is often wholly reliant on useful and relevant input data.  Automated tests are only as good as the data they're using.  To that end, another critical tool for modern functional testing is `test data generators`.

As the name implies, test data generators provide a simple means by which to easily, and often automatically, generate a large set of data that can be used specifically for testing purposes.  While many test data generation tools are capable of using existing or previous data, their true power comes from the ability to generate fresh, new data on the fly, based on a series of corresponding rules and limitations as appropriate.

By passing a data set of generated data as input for various tests, both automated tests and manual testers alike can properly verify that the application is producing the appropriate output or executing the proper actions based on that set of input data.  For future tests, most test data generator tools can generate entirely new random data sets, forcing the software to properly handle data that is largely unexpected, which more closely simulates real-world usage, rather than simply using static test data over and over again.

## Hosted Test Environments

Unlike the necessary phone calls, meetings, and contracts required just a few years ago, many hosted test environment services today provide extremely fast server deployment through self-service web applications.  By allowing additional test environments to be added and configured in a matter of minutes, it's incredibly simple to begin testing your application on a variety of servers across a range of various configurations, as necessary.

Another major advantage of hosted test environments is the sheer speed, performance, and scalability they provide.  Unlike local, self-hosted testing environments, which are typically limited in speed or how well they can scale, most popular third-party test environment hosts have huge, distributed server farms that can be tapped to suit your own needs, growing as necessary throughout the software development life cycle.

Hosted test environments also provide full administration access to the virtual machines, providing every form of direct control your IT administrators would be used to, save for the ability to directly touch the hardware.  This ensures that hosted test environments can be configured exactly to your specifications, running whatever operating system you need, along with any necessary applications or tools which may be required.

## Test Case Management

Running hundreds or even thousands of tests is all well and good, but that does you no good if you have no means by which to keep historical records of your tests and how they perform over time.  Enter the next tool commonly found in modern functional testing: `test case management tools`.

At the most basic level, a test management tool provides a simple means for the team to record and track information related to the variety of testing activities throughout the development life cycle.  Typically, these categories of tracked information might include: specific test cases and their statuses, project progress and release info, issue resolution procedures, team members and assignees, and more.

The clear advantage to maintaining a centralized location for all this test-related data is that it provides an accessible view of the status of all issues and test cases across the entire project to everyone on the team.  Both testers and developers can easily see which test cases have been consistently failing in recent builds and adjust their focus accordingly.

Beyond the innate benefits that a test management tool provides, most popular services also integrate with other testing tools you might be using, such as issue trackers, test automation tools, hosted environments, and code repositories.

## Crowdtesting Platforms

While functional testing tools such as automated testing are great for handling test cases which aim to test and verify the inner workings of software functionality, even the most well-developed suite of automated tests cannot cover every avenue, nor can they find problems that the developers didn't anticipate.  This is where the power of `crowdtesting` as a functional testing tool comes to fruition.  Unlike automated testing, crowdtesting allows tests to be performed in the real world, by a variety of highly-skilled and professional testers, across a plethora of platforms and devices, within environments and from physical locations that simply wouldn't be feasible otherwise.

This diversity in testing, along with the element of human touch, ensures that the tool of crowdtesting is extraordinarily powerful when appropriately applied throughout the software development life cycle.  Crowdtesting provides feedback from testers that is personalized, emulating the experiences that real users are likely to have with the software.  Moreover, humans are robust to small changes in the interface that can cause problems for automated functional tests, so crowdtests are particularly useful when changes occur rapidly.

Best of all, crowdtesting allows for `exploratory testing` to occur throughout the development life cycle, which is something that automated testing can rarely encapsulate.  While an automated testing suite may attempt to consider all avenues of attack or areas of potential issue for a test case, it is often the case that human testers have the knowledge and experience to think _even further_ outside the box, providing insight and discovering issues that weren't even considered in the first place by the developers creating the automated tests.

While a crowdtesting platform engages human testers, from the end-user's perspective, it should function as a software product, just as the other categories of software here do.  So, as the QA manager, product manager, or engineering lead, you should be able to order tests with a GUI or API, see results, and map your progress as easily as you can with the other tools in your toolbox.

---

**SOURCES**

- https://en.wikipedia.org/wiki/Test_data_generation
- http://crest.cs.ucl.ac.uk/fileadmin/crest/sebasepaper/YooH.pdf
- https://aws.amazon.com/dev-test/
- https://azure.microsoft.com/en-us/solutions/dev-test/
- http://www.gurock.com/testrail/
- https://www.qasymphony.com/software-testing-tools/qtest-manager/test-case-management/
- https://smartbear.com/product/qacomplete/features/test-case-management/
- https://en.wikipedia.org/wiki/Test_management_tools
# Types of Automation Testing: Landscape [Version 1]

As we enter into the new year, the prevalence of testing automation trends continue to shift.  While some tried-and-true practices remain as relevant today as they were a few years ago, others are rapidly rising to the limelight.

In this article we'll explore the current automation testing landscape.  We'll dig down a bit into each concept, while hopefully introducing you to a few new ideas for your own automated testing practices in the future.

## Unit Test Automation

No modern automated software testing suite would be complete without the inclusion of `automated unit tests`.  Whereas functional testing is only concerned with the _what_, unit testing focuses on the _how_, by verifying that each piece of code behaves as expected.

Since unit tests are most commonly created by developers, the trend toward automating unit testing should come as no surprise.  By automating the execution and analysis of unit tests, developers can generally be freed up to focus more on producing quality code.

Unit tests give immediate, specific feedback about what's going on in the code, thereby helping to confirm that the code performs the tasks its intended to.  While improperly implemented unit tests can be a dangerous crutch, properly executed tests should not produce any false-positives.

## Integration Test Automation

`Integration testing` is a means by which multiple, independent components of the system are tested with one another.  While these components may be independent, that isn't to suggest they are not interconnected within the context of the software.  For example, a database layer is independent of the functional code, but the two must work together to ensure changes made by a user are reflected in the database, and vice versa.

Proper `integration testing` is a necessity for all but the simplest applications.  Most modern projects will rely on many integrations and third-party components, including data layers, content delivery networks, email services, benchmarking/load testing, deployment infrastructure, analytics... the list goes on and on.  While the overall testing demands will differ from one integration to the next, it's critical that all integrations function as expected, particularly when new builds are pushed or massive changes are coming down the pike.

`API integration testing` is an important subset of `integration testing`, which focuses on testing your software's integration with any third-party APIs you may be using.  Many service APIs provide their own language-specific software development kit (`SDK`), which can be used directly in code in order to access their service.  On the other hand, a far more common implementation of service APIs is to provide a `representational state transfer` (`RESTful`) web service to clients.  By sending appropriate data to specific URIs of the service, along with a valid [`HTTP Request Method`](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods) verb, the service will return a response, indicating a successful transaction, or even an error, when applicable.

## Load Test Automation

Load testing is a crucial benchmark for many software projects these days, particularly for apps targeted at mobile devices and users.  Accurately measuring both normal and peak load for your system ensures your team can better plan for production launch.

`Automated load testing` tools allows load testing to be performed on-demand, if not constantly.  In fact, by performing nightly load tests, you'll often catch non-functional problems that you may have introduced during development the day before.  Consequently, `load testing` will continue to remain a cheap and effective solution for most projects where scalability is (or will be) a factor.

## Functional Test Automation

Functional testing helps to verify that your software is doing _what_ it should, without worrying about how it does it.  This often takes the form of verifying the functionality of the interface or other end-to-end components, without the need to dive into the code that powers it.

`Automated functional testing` expands on these benefits, by allowing your organization to frequently execute functional tests and verify the results, often without human intervention.  Teams can develop a suite of appropriate functional tests, plug them into an automated tool or execution script, and rest easier knowing that all functional tests will be performed automatically.

Of course, `automated functional testing` isn't a cure-all for every potential functional problem.  Such tests have a tendency to be flaky when not properly maintained or monitored, particularly during rapid changes or leading up to a new feature release.

## Regression Test Automation

`Automated regression testing` remains one of the most common testing trends, and for good reason.  As the software development life cycle progresses and new features are added, each iterative build invariably adds more and more tests onto the test suite pile.  As components become more complicated and functionality expands, executing necessary regression tests becomes a major burden when performed in-house.

Many organizations look to automation as a method to improve regression testing efficiency.  Tests can now be developed with automation in mind, which is particularly relevant in `agile`-style projects that heavily emphasize frequent iteration and aggressive release schedules.

Differentiating between (and properly prioritizing) the various types of tests that fall under the umbrella of `regression testing` can be challenging.  Unit testing, integration testing, and functional testing are all performed on their own right, but then each has a regressive form as well that must organized and executed during the `regression testing` process.  All told, this transforms the `regression test suite` into a rather massive and often unwieldy behemoth; an amalgamation of all manner of tests, taken from the typical test type trio.

To alleviate some of this pressure when performing `regression testing`, it's often preferable to breakup the `regression test suite` into smaller subsets of functional tests, which can be run with each build, without the additional burden that comes from regressively testing everything in the system all at once.

## Mobile Test Automation

Mobile is here to stay, as mobile device adoption rates continue to rise, particularly throughout developing countries.  And as internet accessibility grows to meet the demands of those extra users, proper `mobile automated testing` will remain a high priority for many organizations.

Mobile testing presents a particularly challenging task, as it requires functional, compatibility, performance, UI/UX, and security testing, all rolled into one.  By and large, `automated mobile testing` expands on the requirements of typical `automated functional testing`, but with the additional requirements of running on real (or simulated) devices.

Automating some of these mobile testing tasks can dramatically improve turnaround time and better prepare your software for production.  However, it's important to recognize that mobile test results tend to be flaky, given the prevalence of running `automated mobile tests` on emulators, rather than real world devices.  The actionable feedback these tests provide, therefore, is only as good as the reliability of the systems they're running on.

## Virtualization, Containerization, and Immutable Infrastructure

`Virtualization` provides the ability for testing to take place in a virtual environment, ensuring testing platforms are simple to create, maintain, or destroy.  While performing tests in virtual space presents numerous advantages, it also requires additional resources within the test hardware.

The `containerization` trend attempts to resolve some of the drawbacks of virtualization, by bundling together all packaging, shipment, and deployment software components into a (relatively) lightweight container.  Services, like [Docker](https://www.docker.com/), allow containers to be created with specific purposes in mind, including automated test execution.

`Immutable infrastructures` expand even further on these ideas, by encouraging the use of `containers` (or `virtual machines`) that are _unchangeable_ after deployment takes place.  When combined with concepts like containers, immutable infrastructures are the ultimate assurance that tests are performed on the cleanest, most robust platform possible.

## Configuration Management Automation

Modern infrastructure creation and configuration is highly dependent on tools such as [Chef](https://www.chef.io/), [Puppet](https://puppet.com/), or the aforementioned [Docker](https://www.docker.com/).  These tools simplify the process of configuring your software for integrations, physical hardware, and infrastructure.

To expand upon their power, many of these tools can be automated in their own right, allowing for an automated testing process _of_ the `automated configuration` used in your system.

## Crowdtest Automation

`Automated Crowdtesting` allows for human-powered testing to be performed at the same efficiency and speed as other forms of automated testing.  Most `crowdtesting` services provide programmatic API calls, allowing for automated test generation and feedback from a wide range of professional testers.

This combination of automation with human-powered testing provides a unique benefit over other forms of automated testing: tests are executed by real-world users, using real-world devices, providing feedback resembling that of your real-world customers.  With automated API integrations, `crowdtest` results can be delivered rapidly and automatically, ensuring any actionable information arrives within the same time frame as your other automated test results.

---

**SOURCES**

- http://www.testing-whiz.com/blog/15-test-automation-trends-of-2016
- https://www.youtube.com/watch?v=fPLXfWPx6YA
- https://www.joecolantonio.com/2016/01/26/12-test-automation-trends-for-2016-infographic/
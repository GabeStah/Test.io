# Types of Automation Testing: Landscape [Version 1]

As we enter into the new year, the prevalence of testing automation trends continue to shift.  While some tried-and-true practices remain as relevant today as they were a few years ago, others are rapidly rising to the limelight.

In this article we'll examine the current and future trends of the automation testing landscape.  We'll dig down a bit into each concept, while hopefully introducing you to a few new ideas for your own automated testing practices in the future.

## Functional Test Automation

Functional testing helps to verify that your software is doing _what_ it should, without worrying about how it does it.  This often takes the form of verifying the functionality of the interface or other end-to-end components, without the need to dive into the code that powers it.

`Automated functional testing` expands on these benefits, by allowing your organization to frequently execute functional tests and verify the results, often without human intervention.  Teams can develop a suite of appropriate functional tests, plug them into an automated tool or execution script, and rest easier knowing that all functional tests will be performed automatically.

## Unit Test Automation

No modern automated software testing suite would be complete without the inclusion of `automated unit tests`.  Whereas functional testing is only concerned with the _what_, unit testing focuses on the _how_, by verifying that each piece of code behaves as expected.

Since unit tests are most commonly created by developers, the trend toward automating unit testing should come as no surprise.  By automating the execution and analysis of unit tests, developers can generally be freed up to focus more on producing quality code.

## Regression Test Automation

`Automated regression testing` remains one of the most common testing trends, and for good reason.  As the software development life cycle progresses and new features are added, each iterative build invariably adds more and more tests onto the test suite pile.  As components become more complicated and functionality expands, executing necessary regression tests becomes a major burden when performed in-house.

Many organizations look to automation as a method to improve regression testing efficiency.  Tests can now be developed with automation in mind, which is particularly relevant in `agile`-style projects that heavily emphasize frequent iteration and aggressive release schedules.

## Mobile Test Automation

Mobile is here to stay, as mobile device adoption rates continue to rise, particularly throughout developing countries.  And as internet accessibility grows to meet the demands of those extra users, proper `mobile automated testing` will remain a high priority for many organizations.

Mobile testing presents a particularly challenging task, as it requires functional, compatibility, performance, UI/UX, and security testing, all rolled into one.  Automating some of these mobile testing tasks can dramatically improve turnaround time and better prepare your software for production.

## Load Test Automation

Load testing is a crucial benchmark for many software projects these days, particularly for apps targeted at mobile devices and users.  Accurately measuring both normal and peak load for your system ensures your team can better plan for production launch.

`Automated load testing` tools allows load testing to be performed on-demand, if not constantly.  This form of automated testing will continue to remain a cheap and effective solution for most projects where scalability is (or will be) a factor.

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
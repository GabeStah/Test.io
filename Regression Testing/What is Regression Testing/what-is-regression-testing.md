# What is Regression Testing? [FINAL]

If you’ve worked in software, you probably know what `regression testing`, but  while the Internet is already full of explanations of regression testing, in this article we're taking a different spin on this idea -- that a regression test should be a test, and not merely a check.  We'll explore what regression testing is and where it's most commonly implemented, but we'll also examine why `exploratory testing` should also be considered a key component in any proper regression testing methodology.

## What is Regression Testing?

In the simplest terms, `regression testing` is a form of software testing which confirms or denies the functionality of software components after said components undergo changes.  The term `regression` actually means _"the act of reverting back to a previous state,"_, so it stands to reason that in the realm of software development, regression testing indicates that software is tested to ensure it, _too,_ has not regressed to a previous state.  In the event that a change is made to a software component and a bug is discovered, regression testing is required to confirm this issue and attempt to resolve it.

Unfortunately, it is all too common for `regression testing` to focus solely on the success rate of tests, whether automated or manual, without fully evaluating if this indicates the software is functioning as expected.  In some instances, making changes to fix bugs can uncover functional problems that were not addressed by the previous test suite, making `exploratory testing` that much more beneficial.  Furthermore, when developers make too many changes to the code base in too short a timespan, this often leads to instability of the software, the introduction of numerous bugs, and much higher fault rates.

It should, therefore, come as no surprise that weaving an `exploratory testing` phase into the `regression testing` process is a simple, yet powerful, step that can greatly improve the quality of the software.  In many cases, a human will catch an unknown issue, even where a test case indicates no such issue exists.

For example, imagine a web project with an assortment of standard registration fields that users can fill out.  At some point during regression testing, a bug is discovered that was preventing the `nickname` field from being displayed.  Even after that bug is fixed in the code base and `nickname` is now visible, it's often the case that other elements of the application are broken after this fix, since many previous developer decisions could've been made in the time since the `nickname` field first vanished.

Even more likely, but just as problematic, is the possibility that `test cases` for the previously-hidden `nickname` field **simply don't exist**.  Since the field was all but lost up until this recent discovery and bug fix, it now requires someone to closely examine all related test cases and perhaps create new ones or alter existing cases to also account for this "new" field.

Better known as a `masked defect`, even fairly simple examples of these types of issues can be problematic for the application development process.  In cases where defects alter the behavior to such a degree that it is effectively hidden from the developers, it's common for test cases to fail to notice these issues.

For this reason, it can be incredibly beneficial to perform a `crowdtesting` pass **before** any refactoring pass takes place. More often than not, testers may reveal `masked defects`, or even point to improvements, that would dramatically alter the end-result of the system and how it functions, saving a great deal of unnecessary or even wasted coding time during the subsequent `regression testing` procedures.

## When is Regression Testing Appropriate?

`Regression testing` is ideally performed after any changes are made to the code base.  Regression tests are also typically executed anytime a previously discovered issue has been fixed.

The frequency of `regression testing` will vary from project to project, but most projects are served well by performing regression testing on a schedule: after every change, at the end of every day, weekly, bi-weekly, etc.  Generally speaking, the more often regression testing can occur, the more issues can be discovered and resolved, and the more stable and production-ready the application becomes.

On the other hand, it's important to note the drawbacks of `regression testing` as it relates to testing frequency.  In particular, when regression testing implementations focus primarily on automated functional tests, there can be a tendency for tests of this nature to be rather volatile and unstable, often requiring a good deal of personal intervention on the part of developers or QA members to babysit the test suite and confirm the performance and the results.

For this reason, a final suite of regression tests should also include a phase of `exploratory testing` before the system goes into production.  Through `crowdtesting` or other methods, exploratory testing during `regression testing` empowers individual testers with the responsibility and freedom to examine, tinker, and unveil issues or avenues of inquiry that were not considered previously.

## How is Regression Testing Best Implemented?

There are typically three different methods for approaching `regression testing` on a project:

- __Retest All__: This method of `regression testing` simply re-tests the entirety of the software, from top to bottom.  In many cases, the majority of these tests are performed by automated tools, but often that is neither feasible nor necessary.  Moreover, purely using automation ignores the benefits of human testers and any chance for `exploratory testing`.  `Crowdtesting` provides the innate ability to run test cases in parallel, via numerous testers across many devices and platforms.
- __Regression Test Selection__: Rather than a full re-test process, this method allows the the team to choose a representative selection of tests that will approximate a full testing of the test suite, but require far less time or cost to do so.
- __Test Case Prioritization__: With a set of limited test cases, it is ideal to prioritize those tests.  Try to prioritize tests which could impact both current and future builds of the software.

Regardless of the method of implementation outlined above that you choose -- or if you opt for a hybridization of methods -- there are a handful of general best practices to following when implementing `regression testing`:

- **Maintain a Schedule**: Choose a schedule of testing you can maintain throughout the software development life cycle, so testing is never placed on the back burner.
- **Use a Test Management Tool**: In order to properly track all the tests that are being performed on a regular basis, and have historical records of their performance over time, it's ideal to use a simple test management tool of some kind.
- **Evaluate Test Prioritization**: When using any form of prioritization to order your regression tests, try to find a sensible way to order them.  Check out our `Five Tips for Prioritizing Regression Test Automation` guide for a few great tips.
- **Break Down and Categorize Tests**: Just as with the refactoring of the code base itself, tests are often easier to understand and evaluate if they are broken down into smaller pieces.  Try to refactor your tests as often as necessary, then categorize them such that categories of smaller tests can be prioritized over others, making the sorting and execution much easier in the future.
- **Consider Customer Risks**: When developing and prioritizing regression tests, keep vigilant about considering the effects the test cases will have on the customer, or the business as a whole.  Try to design regression tests which cover as many customer-oriented test cases as possible.
- **Perform Exploratory Testing**: `Regression testing` periods should also allow for an `exploratory testing` phase, in order to counterbalance the volume of unit, functional, and integration tests that are likely to be running, through in-depth examinations performed by professional testers.

---

**SOURCES**

- https://en.wikipedia.org/wiki/Regression_testing
- https://smartbear.com/learn/automated-testing/what-is-regression-testing/
- http://www.guru99.com/regression-testing.html
- https://en.wikipedia.org/wiki/Exploratory_testing
# Five Tips for Prioritizing Regression Test Automation


> The usage frequency of a function or the probability of failure in software use. If certain functions of the system are used often and they contain a fault, then the probability of this fault leading to a failure is high. Thus, test cases for this function should have a higher priority than test cases for a less-often-used function.

> Failure risk. Risk is the combination (mathematical product) of severity and failure probability. The severity is the expected damage. Such risks may be, for example, that the business of the customer using the software is impaired, thus leading to financial losses for the customer. Tests that may find failures with a high risk get higher priority than tests that may find failures with low risks.

> The visibility of a failure for the end user is a further criterion for prioritization of test cases. This is especially important in interactive systems. For example, a user of a city information service will feel unsafe if there are problems in the user interface and will lose confidence in the remaining information output.

> Test cases can be chosen depending on the priority of the requirements. The different functions delivered by a system have different importance for the customer. The customer may be able to accept the loss of some of the functionality if it behaves wrongly. For other parts, this may not be possible.

> Besides the functional requirements, the quality characteristics may have differing importance for the customer. Correct implementation of the important quality characteristics must be tested. Test cases for verifying conformance to required quality characteristics get a high priority.

> Prioritization can also be done from the perspective of development or system architecture. Components that lead to severe consequences when they fail (for example, a crash of the system) should be tested especially intensively.

> Complexity of the individual components and system parts can be used to prioritize test cases. Complex program parts should be tested more intensively because developers probably introduced more faults. However, it may happen that program parts seen as easy contain many faults because development was not done with the necessary care. Therefore, prioritization in this area should be based on experience data from earlier projects run within the organization.

> Failures having a high project risk should be found early. These are failures that require considerable correction work that in turn requires special resources and leads to considerable delays of the project.

## Tip 1

> - Find stuff that isn't changing much, is important to customers, revenue, etc., and can be completely deterministic.

## Tip 2

> - Automate simple tests of basic functions and keep this suite small and fast so you can run it with every build.

## Tip 3

> - Avoid things that are dependent on the way an interface looks. Humans are good at finding "fit-and-finish" issues and in being robust to small changes in the interface. Computers not so much.

## Tip 4

> - If you're going to break the build, a flaky test is worse than no test at all because it will waste developers' time and maintenance costs are high. If your tests are flaky, use those as a guide for exploratory testers before you deploy, never as a build-blocker.

## Tip 5

> - Remember that software can pass 100% of its regression test cases and be profoundly broken to the user because you can't write test cases for everything. If your testers find hotspots, consider refactoring for better developer testability in preference to writing more automated GUI tests.


> we don't need to tell them what GUI/functional test automation is, or regression, etc.

> It is common in DevOps circles to say that you should "automate everything." We want to make sure that we're not "anti-automation" but the fact remains that automated functional tests are often flaky and you should prioritize certain ones over others. So we want to recommend how to prioritize automation while suggesting that in other areas, human testers remain a great option (particularly crowdtesters in some cases). To ship fast, there's a lot of other automation work you should do before automating all of your functional test cases: making sure you can deploy fast, making sure any developer can get a test environment fast, unit tests, integration tests, etc.

> https://docs.google.com/document/d/1L_DWV66bqZdvAxwK_NszyvuqhVNLo_s6-f9vgu9oAxM/edit

> I just sent you this article which a friend is writing about GUI test automation which basically says don't bother. It's a more extreme version of the point I make when I say to ship fast, there's a lot of other automation work you should do before automating all of your functional test cases: making sure you can deploy fast, making sure any developer can get a test environment fast, unit tests, integration tests, etc.

> That much said, when you are automating regression tests using functional test automation:

> - Find stuff that isn't changing much, is important to customers, revenue, etc., and can be completely deterministic.
> - Automate simple tests of basic functions and keep this suite small and fast so you can run it with every build.
> - Avoid things that are dependent on the way an interface looks. Humans are good at finding "fit-and-finish" issues and in being robust to small changes in the interface. Computers not so much.
> - If you're going to break the build, a flaky test is worse than no test at all because it will waste developers' time and maintenance costs are high. If your tests are flaky, use those as a guide for exploratory testers before you deploy, never as a build-blocker.
> - Remember that software can pass 100% of its regression test cases and be profoundly broken to the user because you can't write test cases for everything. If your testers find hotspots, consider refactoring for better developer testability in preference to writing more automated GUI tests.

---

__SOURCES__

- http://www.sciencedirect.com/science/article/pii/S1877050916001514

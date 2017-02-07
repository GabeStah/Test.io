# [OUTLINE] DevOps Best Practices: Integrating QA and DevOps

> KEYWORDS: devops best practices

- Introduction that briefly outlines the topic at hand and the main points being raised:
- Continuous delivery & continuous integration can be combined with QA
- QA is a necessity in modern development due to failure of automation to cover all scenarios
- Modern QA should behave as a preventative medicine for DevOps, not just locating, but ideally _preventing_ bugs from entering production environments.

## QA Supports Continuous Delivery

- Give example of organization using continuous delivery techniques to push builds to staging servers.
- With fully-automated workflows, all builds that pass automated testing are pushed ahead; highlight the importance of handling not-so-easily automated tests, particularly as they can (and should) play a factor in whether or not the build is pushed to production.
- Discuss the importance of exploratory testing to uncover hidden bugs, as automated test cases are only as robust as when they were originally created.

## Continuous Integration Shouldn't Be a Crutch

- Discuss how many organizations see continuous integration -- along with the associated tools and automated tests that come with it -- as the be-all, end-all of QA needs.
- Highlight the dangers of this approach, particularly when evaluating all tests as successful because TravisCI or another tool said all was well (not seeing the forest for the trees).
- Emphasize the benefits that human-intervention and crowdtesting can bring to automated testing suites, by filling in the gaps.

## QA Is Here to Stay

- Reference the somewhat biased views of articles and blog posts that have popped up recently suggesting that the emergence of `DevOps` means the inevitable redundancy of QA as a role in modern development life cycles.
- The contention stems around the notions that automation solves all problems.
- In addition to points made above in previous sections, detail how automated tests typically cannot perform well with malleable components of the project, such as the UI.
- Discuss the importance of human testers in modern development, particularly in the mobile space where numerous uncontrolled factors come into play (screen sizes, usability, etc).

## Modern QA is a Preventative Medicine

- Briefly discuss old-school QA, which was largely working with waterfall methodologies well at the end of the development life cycle.
- Discuss how QA of the past was focused on quickly finding bugs in a mad dash prior to release to production, and how that outlook on QA is outdated and no longer applies.
- Today, QA is best thought of as a preventative medicine within the DevOps paradigm.  Rather than being an afterthought well into the dev cycle, it should be performed __in tandem__ with all other DevOps, throughout the process.
- Detail how, while modern QA can (and will) find numerous bugs in the code, it's ultimate purpose is to _prevent bugs from ever appearing in production in the first place._
- Explain how proper crowdtesting and QA integration into DevOps throughout software development life cycle can not only find bugs early, but dramatically reduce overall bugs during development, as well as quantity of bugs that make it to production.
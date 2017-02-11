# [OUTLINE v3 FINAL] DevOps Best Practices: Integrating QA and DevOps

> KEYWORDS: devops best practices

- Introduction that briefly outlines the topic at hand and the main points being raised:
- Continuous delivery & continuous integration can be combined with QA
- QA is a necessity in modern development due to failure of automation to cover all scenarios
- Modern QA should act like a fitness regimen for DevOps, not just locating and preventing bugs from entering production, but also by promoting stability through continuous improvement.

## QA Supports Continuous Delivery

- Give example of organization using continuous delivery techniques to push builds to staging servers.
- With fully-automated workflows, all builds that pass automated testing are pushed ahead; highlight the importance of handling not-so-easily automated tests, particularly as they can (and should) play a factor in whether or not the build is pushed to production.
- Discuss the importance of exploratory testing to uncover hidden bugs, as automated test cases are only as robust as when they were originally created.

## Continuous Integration != Continuous Delivery != Customer Success

- Discuss how many organizations see continuous integration -- along with the associated tools and automated tests that come with it -- as the be-all, end-all of QA needs.
- Highlight the dangers of this approach, particularly when evaluating all tests as successful because TravisCI or another tool said all was well (not seeing the forest for the trees).
- Emphasize the benefits that human-intervention and crowdtesting can bring to automated testing suites, by filling in the gaps.

## QA Is Here to Stay

- Reference the somewhat biased views of articles and blog posts that have popped up recently suggesting that the emergence of `DevOps` means the inevitable redundancy of QA as a role in modern development life cycles.
- The contention stems around the notions that automation solves all problems.
- In addition to points made above in previous sections, detail how automated tests typically cannot perform well with malleable components of the project, such as the UI.
- Discuss the importance of human testers in modern development, particularly in the mobile space where numerous uncontrolled factors come into play (screen sizes, usability, etc).
- Detail the importance of an organization having a process for determining whether software is ready to ship to customers, and that that process should have multiple inputs, some of which demand human judgment.

> What we've seen over the past 5-10 years is that the QA function has bled away into different groups. The Product team owns part of it, the engineering team another part, etc. The important thing is that the function continues to exist, even if it doesn't exist in a team called by that name. 

> Someone must represent the customer in the development process.  Whether you call that QA or something else, if your customers are human, this is going to involve some human judgment.

> You might even think about carrying the "fitness" metaphor through the piece, where the "event" you're training for -- the mountain you're climbing -- is being out there for customers. And your QA team is telling you not just whether your vital signs are okay, but whether you really understand the terrain, you know what to do if things go bad, etc.

## Modern QA is a Fitness Regimen

- Briefly discuss old-school QA, which was largely working with waterfall methodologies well at the end of the development life cycle.
- Discuss how QA of the past was focused on quickly finding bugs in a mad dash prior to release to production, and how that outlook on QA is outdated and no longer applies.
- Today, QA is best thought of as a fitness regimen within the DevOps paradigm.  Rather than being an afterthought well into the dev cycle, it should be performed __in tandem__ with all other DevOps, throughout the process.
- Detail how, while modern QA can (and will) find numerous bugs in the code, ideally locating existing bugs and preventing new ones, with the ultimate purpose of it's ultimate purpose is to promote product stability through continuous improvement toward business goals.
- Explain how proper crowdtesting and QA integration into DevOps throughout software development life cycle can not only find bugs early, but dramatically reduce overall bugs during development, as well as quantity of bugs that make it to production.
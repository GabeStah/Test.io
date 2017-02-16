# DevOps Best Practices: Integrating QA and DevOps [Version 1]

Quality assurance is often neglected in the expansive realm of DevOps.  Many organizations often focus on the flashiest practices of DevOps, like continuous delivery and continuous integration, that it can be easy to forget about proper testing and QA until its too late.

This disconnect often occurs, in large part, due to misconceptions about what the role of quality assurance is throughout the development life cycle, particularly as it relates to DevOps.  QA isn't just about finding and fixing bugs; modern QA is a fitness regimen for both your application and your organization.  Automation cannot cover all possible scenarios or test cases in modern development, resulting in failures that proper QA practices could've conditioned and prepared you for.

In this article, we'll explore how QA can train your team and strengthen your project, preparing you for that dramatic moment when you hear the whistle blow, and the big game known as launching to production has begun!

- Introduction that briefly outlines the topic at hand and the main points being raised:
- Continuous delivery & continuous integration can be combined with QA
- QA is a necessity in modern development due to failure of automation to cover all scenarios
- Modern QA should act like a fitness regimen for DevOps, not just locating and preventing bugs from entering production, but also by promoting stability through continuous improvement.

> I am loving the metaphor of fitness.

> Modern QA is a Fitness Regimen
> Quality = Fitness for your customer's purpose
> The Big Game = when your customer sees the software
> Fitness Regimen makes sure you're really ready for the Big Game, not just that your pulse and blood pressure are right, but that you've actually "got game."

## QA Supports Continuous Delivery

Continuous delivery is undoubtedly a powerful tool when used properly.  Releasing new, fully-functional builds at the drop of a hat is an alluring prospect, but it can be a dangerous siren song if poorly implemented.  With fully-automated workflows, all builds that pass automated testing are pushed to staging (or even production), before their fitness for release has been fully confirmed.  Even big organizations, like Google, have experienced issues with continuous delivery practices due to lack of human-oriented quality control practices.

In one particular case, the [Google Consumer Surveys](https://www.google.com/analytics/surveys/) team pushed a build production that contained an obvious visual bug: a purple dancing pony.  The cause of this major fumble?  An incorrect `CSS` class name.  The team at Google had a vast series of checks and balances in place to verify the integrity of the build and ensure nothing untoward was pushed to production:

- Monitoring
- Test Automation
- Continuous Integration
- Code Review
- Deploy to Staging
- QA Checklist

Everything came back green.  All tests were successful, staging looked as expected, and even their QA checklist failed to notice the issue.  In spite of all these checks, along with the dozens of metrics that failed to report any issues, none of their systems could identify this purple dancing pony on the page.  As Brett Slatkin, [engineering lead on the project puts it](https://air.mozilla.org/continuous-delivery-at-google/), "I don't know anything about how my customer perceives the app."

The simple solution?  `Exploratory testing` by experienced testing professionals.  Since all the automated testing and verification steps in the world can only prepare your application as far as their original coverage allows, a little bit of `crowdtesting`, mixed into the continuous delivery process, is all it takes to prevent catastrophes like the infamous `dancing pony incident`.

## Continuous Integration != Continuous Delivery != Customer Success

As we examined above, even the most diligent and well-intentioned organizations often view continuous integration practices as the be-all, end-all of quality assurance requirements.  If it is assumed that automated tests, code review, and staging deployments are all it takes to be fully prepared for climb that mountain of production release, it shouldn't come as much of a surprise if an unexpected fall occurs, plummeting the project back toward the bottom.

Continuous integration does a fine job of performing automated tests and building your software.  Likewise, continuous delivery aims to allow you to release builds at a moment's notice.  Yet neither of these practices fundamentally equate to customer success.  Just because TravisCI or Jenkins tells you your software is fit as a fiddle, that doesn't necessarily mean the human experience, that represents your customers, is ready for production.

Human intervention and `crowdtesting` brings the importance of the customer to the forefront of the DevOps process.  By allowing testers to work in conjunction with continuous integration and delivery patterns, you can better ensure that any gaps in coverage are filled, so your application's quality is up to par and ready for your customers.

## QA Is Here to Stay

A handful of op-ed pieces and blog posts have popped up around the Net, intimating that the need for QA is declining with the rise of DevOps practices.  The core of this contention is that automated methodologies solve all potential problems that may arise during the software development life cycle, as the theory goes that the speed and efficiency of computerized solutions wins out over traditional QA methods.

Two counterpoints are critical to consider here:

1. Automation and `continuous-X` practices have difficulty grappling with malleable components of a project.  Aspects such as the UI and the mobile experience present numerous uncontrolled factors that are challenging for automated tests to handle.  Human testers, on the other hand, can easily evaluate and provide feedback on such elements. 

2. Customer goals must always be at the forefront of both development and testing practices.  It's not always enough to go through your basic DevOps process, relying on automated code review, automated tests, and metrics to indicate the fitness of the software.  `Crowdtesting` can provide an additional source of quality control, as well as `exploratory testing`, both of which are necessary to ensure software is healthy enough to ship to customers.

- Reference the somewhat biased views of articles and blog posts that have popped up recently suggesting that the emergence of `DevOps` means the inevitable redundancy of QA as a role in modern development life cycles.
- The contention stems around the notions that automation solves all problems.
- In addition to points made above in previous sections, detail how automated tests typically cannot perform well with malleable components of the project, such as the UI.
- Discuss the importance of human testers in modern development, particularly in the mobile space where numerous uncontrolled factors come into play (screen sizes, usability, etc).
- Detail the importance of an organization having a process for determining whether software is ready to ship to customers, and that that process should have multiple inputs, some of which demand human judgment.

> Someone must represent the customer in the development process.  Whether you call that QA or something else, if your customers are human, this is going to involve some human judgment.

> You might even think about carrying the "fitness" metaphor through the piece, where the "event" you're training for -- the mountain you're climbing -- is being out there for customers. And your QA team is telling you not just whether your vital signs are okay, but whether you really understand the terrain, you know what to do if things go bad, etc.

## Modern QA is a Fitness Regimen

Historically, quality assurance has been relegated to the back of the pack, as one of the very last picks in the disciplined pickup game that is the development life cycle.  `Waterfall` methods have been notorious for pushing testing and other quality control practices toward the end of the process, which often led to a mad sprint to fix bugs and reach finish line of release before the looming deadline.

Modern `agile` methodologies, which are rough and tumble by comparison to `waterfall` styles, are typically more test-oriented, placing QA in the middle of the pack.  Yet, even with more diligent testing practices in place, `agile` DevOps still often consider QA to be an afterthought.

Modern QA is a fitness regimen for your software.  QA is a form of `continuous improvement`, and those improvements should function as a tight-knit teammate of the other `continuous-X` disciplines.  Given the strength of `crowdtesting` and other forms of quality assurance, testing should be performed **in tandem** with other DevOps.

Proper `crowdtesting` and QA integration into DevOps ensures that your application is both stable and robust.  Bugs will be found earlier and more often.  Moreover, human testers provide that extra level of fitness through `continuous improvements`, always moving the goalposts toward business objectives.

Automated testing and other DevOps practices will undoubtedly find bugs

> What we've seen over the past 5-10 years is that the QA function has bled away into different groups. The Product team owns part of it, the engineering team another part, etc. The important thing is that the function continues to exist, even if it doesn't exist in a team called by that name. 

- Briefly discuss old-school QA, which was largely working with waterfall methodologies well at the end of the development life cycle.
- Discuss how QA of the past was focused on quickly finding bugs in a mad dash prior to release to production, and how that outlook on QA is outdated and no longer applies.
- Today, QA is best thought of as a fitness regimen within the DevOps paradigm.  Rather than being an afterthought well into the dev cycle, it should be performed __in tandem__ with all other DevOps, throughout the process.
- Detail how, while modern QA can (and will) find numerous bugs in the code, ideally locating existing bugs and preventing new ones, with the ultimate purpose of it's ultimate purpose is to promote product stability through continuous improvement toward business goals.
- Explain how proper crowdtesting and QA integration into DevOps throughout software development life cycle can not only find bugs early, but dramatically reduce overall bugs during development, as well as quantity of bugs that make it to production.

- http://www.neotys.com/blog/where-does-qa-fit-in-devops/
- http://blog.gerrardconsulting.com/?q=node/666
- https://medium.com/@eon01/the-15-point-devops-check-list-8cd2afb4a448#.8w6zycs7n
- http://searchsoftwarequality.techtarget.com/news/450305123/How-to-do-DevOps-so-you-can-avoid-disaster-and-disappointment
- http://searchitoperations.techtarget.com/podcast/How-dev-ops-and-execs-should-treat-automated-QA-testing
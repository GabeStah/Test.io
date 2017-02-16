# DevOps Best Practices: Integrating QA and DevOps [Version 1]

Quality assurance is often neglected in the expansive realm of DevOps.  Many organizations often focus on the flashiest practices of DevOps, like continuous delivery and continuous integration.  In such scenarios, it can be easy to forget about proper testing or QA until its too late.

This disconnect often occurs due to misconceptions about what the role of quality assurance is throughout the development life cycle, particularly as it relates to DevOps.  Quality assurance isn't just about finding and fixing bugs; modern QA is a fitness regimen for both your application and your organization.  Automation cannot cover all possible scenarios or test cases in modern development, resulting in failures that proper QA practices could've conditioned and prepared you for.

In this article, we'll explore how QA can train your team and strengthen your project, coaching you toward that dramatic moment when you hear the whistle blow, and the big game, known as launching to production, has begun!

## QA Supports Continuous Delivery

Continuous delivery is undoubtedly a powerful tool when used properly.  Releasing new, fully-functional builds at the drop of a hat is an alluring prospect, but it can be a dangerous siren song if poorly implemented.  With fully-automated workflows, all builds that pass automated testing are pushed to staging (or even production), before their fitness for release has been accurately confirmed.  Even big organizations, like Google, experience issues with continuous delivery practices, due to a lack of human-oriented quality control practices.

In one particular case, the [Google Consumer Surveys](https://www.google.com/analytics/surveys/) team pushed a build to production that contained an obvious visual bug: [a dancing purple pony](https://air.mozilla.org/continuous-delivery-at-google/).  The cause of this major fumble?  An incorrect `CSS` class name.  The team at Google implemented a vast series of checks and balances to verify the integrity of the build and ensure nothing untoward was pushed to production:

- Monitoring
- Test Automation
- Continuous Integration
- Code Review
- Deploy to Staging
- QA Checklist

Everything came back green.  All tests were successful, staging looked as expected, and even their QA checklist failed to notice the issue.  In spite of all these checks, along with the dozens of metrics that failed to report any issues, none of their systems could identify this dancing purple pony sitting right there on the page.  As Brett Slatkin, engineering lead on the project puts it, "I don't know anything about how my customer perceives the app."

The simple solution?  `Exploratory testing`, performed by experienced testing professionals.  All the automated testing and verification steps in the world can only prepare your application as much as their original coverage allows.  A little bit of `crowdtesting`, mixed into the continuous delivery process, is all it takes to prevent catastrophes like the infamous `dancing pony incident`.

## Continuous Integration != Continuous Delivery != Customer Success

As we examined above, even the most diligent and well-intentioned organizations often view continuous integration practices as the be-all, end-all of quality assurance requirements.  If teams assume that automated tests, code review, and staging deployments are all it takes to be fully prepared to climb that mountain of production release, it shouldn't come as much of a surprise if an unexpected fall occurs, plummeting the project back toward the bottom.

Continuous integration does a fine job of performing automated tests and building your software.  Likewise, continuous delivery aims to allow you to release builds at a moment's notice.  Yet neither of these practices fundamentally equate to customer success.  Just because TravisCI or Jenkins tells you your software is as fit as a fiddle, that doesn't necessarily mean the human experience, which represents your customers, is ready for production.

Human intervention and `crowdtesting` brings the importance of the customer to the forefront of the DevOps process.  By allowing testers to work in conjunction with continuous integration and delivery patterns, you can better ensure that any gaps in coverage are filled, so your application's quality is up to par and ready for your customers.

## QA Is Here to Stay

A handful of op-ed pieces and blog posts have popped up around the Net, intimating that the need for QA is declining with the rise of DevOps practices.  The core of this contention is that automated methodologies solve all potential problems which may arise during the software development life cycle.  Speed and efficiency of computerized solutions wins out over traditional QA methods, or so the theory goes.

Two counterpoints are critical to consider here:

1. Automation and `continuous-X` practices have difficulty grappling with malleable aspects of a project.  Components such as the UI and the mobile experience present numerous uncontrolled factors, which are challenging for automated tests to handle.  Human testers, on the other hand, can easily evaluate and provide feedback on such elements. 

2. Customer goals must always be at the forefront of both development and testing practices.  It's not always enough to go through your basic DevOps process, relying on automated code review, automated tests, and metrics to indicate the fitness of the software.  `Crowdtesting` can provide an additional source of quality control -- as well as `exploratory testing` -- both of which are necessary to ensure software is healthy enough to ship to customers.

Ultimately, quality assurance should emphasize the customer experience over all else, by ensuring that software quality is at peak performance.  

## Modern QA is a Fitness Regimen

Historically, quality assurance has been relegated to the back of the pack, as one of the very last picks in the disciplined pickup game that is the development life cycle.  `Waterfall` methods are notorious for pushing testing and other quality control practices toward the end of the process, which often leads to a mad sprint to fix bugs and reach the finish line of release, before the looming deadline.

Modern `agile` methodologies, which are rough and tumble by comparison to `waterfall` styles, are typically more test-oriented, placing QA in the middle of the pack.  Yet, even with more diligent testing practices in place, `agile` DevOps still often consider QA to be an afterthought.

Remember, modern QA is a fitness regimen for your software.  QA should be a constant source of `continuous improvement`, and those improvements should function as a tight-knit teammate of the other `continuous-X` disciplines.  Given the strength of `crowdtesting` and other forms of quality assurance, testing should be performed **in tandem** with other DevOps.

Proper `crowdtesting` and QA integration into DevOps ensures that your application is both stable and robust.  Bugs will be found earlier and more often.  Moreover, human testers provide that extra level of fitness through `continuous improvements`, always moving the goalposts toward those ultimate business objectives.

- http://www.neotys.com/blog/where-does-qa-fit-in-devops/
- http://blog.gerrardconsulting.com/?q=node/666
- https://medium.com/@eon01/the-15-point-devops-check-list-8cd2afb4a448#.8w6zycs7n
- http://searchsoftwarequality.techtarget.com/news/450305123/How-to-do-DevOps-so-you-can-avoid-disaster-and-disappointment
- http://searchitoperations.techtarget.com/podcast/How-dev-ops-and-execs-should-treat-automated-QA-testing
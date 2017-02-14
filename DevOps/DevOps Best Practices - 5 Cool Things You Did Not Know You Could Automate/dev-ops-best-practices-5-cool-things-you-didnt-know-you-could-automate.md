# DevOps Best Practices: 5 Cool Things You Didn't Know You Could Automate

The combination of software development and information technology operations, better known as `DevOps`, is a broadly used term describing the process of creating and delivering software.  Many of the commonly automated practices used in DevOps are already well known, including: automated testing, continuous integration (`CI`), continuous deployment (`CD`), monitoring, logging, data provisioning, and much more.  While all these facets of DevOps are obviously beneficial throughout the overall software development life cycle, most are such common practice that diving too deep into them won't be presenting anything very ground-breaking.

Instead, in this article we'll be exploring five new and rather unique things you can _also_ automate as part of your DevOps strategy that you may not have considered, so let's get to it!

## Automating an Immutable Infrastructure

Commonly used in the realm of programming, the concept of an `immutable object` simply refers to _an object whose state cannot be changed after its creation_.  Many programming languages support `immutability`, thereby forcing a variable or object to be `read-only`, in which the contents can only be viewed or `read`, but not altered.

This concept of `immutability` has recently been transferred into the world of DevOps, specifically in the form of `immutable infrastructure`.  Just as with `immutable` objects in programming, `immutable infrastructure` means that we're taking the various components that makeup the application infrastructure (web server, database, CDN, etc), and _preventing them from being altered in any way once created._  This contrasts with a "normal" infrastructure, in which a new deployment to production would require changes to existing components, all the while the software must remain live.

With `automated immutable infrastructure`, instead of dealing with changes to live components, **all** the components are entirely replaced when a new build is deployed.  Typically, this is achieved using a common `image` that was previously built during early development, and can therefore easily be validated and tested prior to using it in production.  That image is then used to create an entirely new `immutable infrastructure`, on top of which the new production deployment is placed.

There are a few clear advantages to implementing `immutable infrastructure` automation:

- **History Preservation**: Since each new deployment forces a new image to be generated, on top of which the deployment rests, all previous deployments can be retained for historical purposes.  In the event that something goes wrong, a rollback to a previous deployment is a relatively painless process.
- **Maintain Integration States**: When a new automated deployment is created, the state of the infrastructure is entirely reset along with it, since it is simply copied from the state of the original image.  This ensures that all integrations, which your software may rely on, will be configured in exactly the same way every time.  Assuming they were tested and working originally, the outcome is the same the next time.
- **Dependency Management**: As applications change during the development life cycle, it is common to include additional libraries or other dependencies.  With a single, stable `immutable infrastructure` image that is copied and used for each deployment, it makes handling dependencies much simpler.  The base image can be frequently tested and maintained, including all the necessary dependencies, so new deployments are smooth.

## Automating Regulatory Compliances

While not relevant to every development project, managing proper `regulatory compliance` can be critical for some organizations.  Since most developers lack a background in law, maintaining proper `regulatory compliance` can be a challenge, if and when it is required.

Compliance is required in a variety of fields, from government and finance to pharmaceuticals and trade.  The standards of compliance vary from one regulation to the next, but many regulations like [`HIPAA`] and [`PCI`] heavily emphasize confidentiality and privacy.

In spite of the complications associated with `regulatory compliance` during software development, as with many other aspects of DevOps, it's possible to assist with proper compliance through a bit of automation.  [`Some organizations`](http://searchitoperations.techtarget.com/news/450302065/Sparta-counters-DevOps-naysayers-with-compliance-automation) are now finding that they are able to comply with industry regulations through automated DevOps practices, in large part by properly focusing on and maintaining a clear (digital) "paper trail."  Through common automated DevOps practices, it's now much easier for organizations to point to consistent, proven, and verifiable records of compliance.  By using tools like automated testing and deployment, there now exists historical evidence that test cases directly related to regulatory compliance are passing, and automated deployment following those successful tests ensures that compliance is pushed to production.

## Automating Development Environments

While automated provisioning of servers is a fairly common DevOps practice on which to host development or production applications, one often overlooked method of automation is the ability to create `development environments`.  Similar to the concept of storing images for use in `immutable` deployments explored earlier, it's greatly beneficial to generate an baseline image for a proper `developer environment` for your organization or even just the current project.

When a new developer joins the team, there's no need to spend hours installing the proper apps, making the appropriate configuration adjustments, or providing the correct access rights to the developer's machine.  With an `automated development environment` image ready to go, a copy of the standard developer environment can be copied to the new developer's machine, and all the necessary access rights, applications, and configurations will be included right out of the gate.  Best of all, this image can be used on a local machine or even remotely, via a virtual machine.

There are a number of existing tools that can be used for the creation and management of automated developer environments, but a few popular ones include [`Vagrant`] and [`Chef`].  Each tool comes with its own benefits, but they're all generally designed to be user-friendly, providing a simple API, using a common language or syntax, to create most any configuration as a new development image.

## Automating Code Review

While most of the automated tasks associated with DevOps tend to focus on managing code once its written, there's something to be said for the practice of `automatic code reviews`.  In the simplest terms, an `automatic code review` aims to evaluate existing code, using robust services and applications, by checking for proper style, complexity, security, duplication, and coverage... automatically.  There are a number tools that can be used for `automated code review`, including [`Code Climate`], [`Codacy`], and [`Codebeat`], but every service will largely aim to perform the same basic role within your DevOps.

`Automated code review` provides many of the same benefits of the practice known as [`pair programming`], which places two developers at the same desk and has them work in tandem on active development.  Rather than having another human physically sitting with each developer, an automated code review service aims to provide many of those same benefits, by verifying code quality and coverage with simple interfaces; all while being compatible with existing automated DevOps practices such as `continuous integration` and `continuous deployment`.  

## Automating Human Feedback

While the concept may seem contradictory at first, another powerful tool that can be automated as part of your DevOps process is `automated human feedback` through `crowdtesting`.  In cannot be overstated how critical feedback is during the entire software development life cycle.  Whether that feedback comes from other developers, users, customers, or testers, it is imperative that the team is able to gather, analyze, and adapt to that feedback as effectively as possible.  This need to adapt to incoming feedback is particular important for projects following a form of `agile` development, where iteration and adaptation is a staple of the methodology.

In the case of `automating human feedback` via `crowdtesting`, this can provide your project and organization with unique insight into what may otherwise be uncommon scenarios or unforeseen test cases.  It is common for automated testing solutions -- whether for unit testing, functional testing, or otherwise -- to remain somewhat blind to potential issues or bugs that professional human testers are experienced and trained to seek out.  Moreover, even if all automated tests pass, that isn't a guarantee that the software is fully-functional and ready for production.  This is a great reason to slip `crowdtesting` into the mix, so human testers can perform testing and provide curated feedback.

Implementation of `automating crowdtesting feedback` will vary from one tool to the next, but services like [`Test.io`] provide an API to trigger tests based on your own conditional requirements, so feedback can be gathered automatically, alongside your other automated DevOps practices.

Ultimately, `automated human feedback` can provide your organization with detailed insight on the quality and readiness of your application for future builds or even production release.  Through exploratory testing and automated feedback loops via `crowdtesting`, a multitude of testers from all around the world can provide real world testing feedback by simulating the experiences of real users to ensure your software is ready for launch.

---

[`HIPAA`]: https://www.hhs.gov/hipaa/
[`PCI`]: https://www.pcisecuritystandards.org/
[`Vagrant`]: https://www.vagrantup.com/
[`Chef`]: https://www.chef.io/
[`Code Climate`]: https://codeclimate.com/
[`Codacy`]: https://www.codacy.com/
[`Codebeat`]: https://codebeat.co/
[`pair programming`]: https://en.wikipedia.org/wiki/Pair_programming
[`Test.io`]: https://test.io/features/

---

**SOURCE**

- https://blog.codeship.com/immutable-infrastructure/
- http://chadfowler.com/2013/06/23/immutable-deployments.html
- http://searchitoperations.techtarget.com/news/450302397/Programmable-infrastructure-fends-off-configuration-drift
- http://searchitoperations.techtarget.com/feature/Immutable-infrastructure-takes-build-automation-to-the-systems-level
- http://searchitoperations.techtarget.com/definition/immutable-infrastructure
- http://searchitoperations.techtarget.com/news/450302065/Sparta-counters-DevOps-naysayers-with-compliance-automation
- https://codeclimate.com/
- https://www.codacy.com/
- https://codebeat.co/
# [OUTLINE] DevOps Best Practices: 5 Cool Things You Didn't Know You Could Automate

> KEYWORD: devops best practices

The combination of software development and information technology operations, better known as `DevOps`, is a broad term used to describe the process of creation and delivery of software.  There are numerous common practices within the spectrum of DevOps that are commonly automated, including: automated testing, continuous integration (`CI`), continuous deployment (`CD`), monitoring, logging, data provisioning, and much more.  While all these facets of DevOps are obviously greatly beneficial throughout the overall software development life cycle, most of these are such common practice that diving too deep into them isn't very ground-breaking.

Instead, in this article we'll aim to explore five somewhat unique things you can automate as part of your DevOps strategy that you may not be aware of or have considered, so let's get to it!

## Automating an Immutable Infrastructure

Commonly used in the realm of programming, the concept of an `immutable object` simply refers to _an object whose state cannot be changed after its creation_.  Many programming languages support `immutability`, thereby forcing a variable or object to be `read-only`, in which the contents can only be viewed or `read`, but not altered.

This concept of `immutability` has recently been transferred into the world of DevOps, specifically in the form of `immutable infrastructure`.  Just as with `immutable` objects in programming, `immutable infrastructure` means that we're taking the various components that makeup the application infrastructure (web server, database, etc), and _preventing them from being altered in any way once created._  This contrasts with a "normal" infrastructure, in which a new deployment to production would require changes to existing components, all the while the software must remain live.

With automated `immutable infrastructure`, instead of dealing with changes to live components, **all** the components are entirely replaced when a new production build is deployed.  Typically, this can be performed using a common image that was previously built early in development, and can therefore easily be validated and tested prior to using it in production.  That image is then used to create an entirely new, `immutable` infrastructure on which the new production deployment is placed.

There are a few clear advantages to implementing `immutable infrastructure` automation:

- **History Preservation**: Since each new deployment forces a new image to be generated, on top of which to place said deployment, all previous deployments can be retained for historical purposes.  In the event that something goes wrong, a rollback to a previous deployment is a relatively painless process.
- **Maintain Integration States**: When a new automated deployment is created, the state of the infrastructure is entirely "reset" along with it.  This ensures that all integrations that your software may rely on will be configured in exactly the same way every time, ensuring if they were tested and working originally, the outcome is the same the next time.
- **Dependency Management**: As applications change during the development life cycle, it is common to include additional libraries or other dependencies.  With a single, stable `immutable infrastructure` image that is copied and used for each deployment, it makes handling dependencies much simpler.  The base image can be frequently tested and maintained, including all the necessary dependencies, so new deployments are smooth.

- Discuss the definition of `immutable infrastructure` and the difference between normal infrastructure.
- In particular, emphasize the notion of always _building new_, rather than _changing existing_.
- Highlight particular examples of this kind of automation, such as Microsoft.
- Emphasize benefits of this technique, such as simple historical rollback.

https://blog.codeship.com/immutable-infrastructure/
http://chadfowler.com/2013/06/23/immutable-deployments.html
http://searchitoperations.techtarget.com/news/450302397/Programmable-infrastructure-fends-off-configuration-drift
http://searchitoperations.techtarget.com/feature/Immutable-infrastructure-takes-build-automation-to-the-systems-level
http://searchitoperations.techtarget.com/definition/immutable-infrastructure

## Automating Regulatory Compliances

While not relevant to every development project, managing proper `regulatory compliance` can be critical for some organizations.  Since most developers lack a background in law, maintaining proper `regulatory compliance` can be a challenge, if and when it is required.

Compliance is required in a variety of fields, from government and finance to pharmaceuticals and trade.  The standards of compliance vary from one regulation to the next, but many regulations like [`HIPAA`] and [`PCI`] heavily emphasize confidentiality and privacy.

In spite of the complications associated with `regulatory compliance` during software development, as with many other aspects of DevOps, it's possible to assist with proper compliance through a bit of automation.  [`Some organizations`](http://searchitoperations.techtarget.com/news/450302065/Sparta-counters-DevOps-naysayers-with-compliance-automation) are now finding that they are able to comply with industry regulations through automated DevOps practices, in large part by properly focusing on and maintaining a clear (digital) "paper trail."  Through common automated DevOps practices, it's now much easier for organizations to point to consistent, proven, and verifiable records of compliance.  By using tools like automated testing and deployment, there now exists historical evidence that test cases directly related to regulatory compliance are passing, and automated deployment following those successful tests ensures that compliance is pushed to production.

- Discuss the importance of regulatory compliance in the development community, as it pertains to particular types of projects (government, financial, pharmaceutical, etc).
- Provide specific examples of automated compliance.
- Outline the fundamental components of compliance automation by providing a consistent, proven, and verifiable "paper trail" via automated development, testing, and deployment services.

http://searchitoperations.techtarget.com/news/450302065/Sparta-counters-DevOps-naysayers-with-compliance-automation

## Automating Development Environments

While automated provisioning of servers is a fairly common DevOps practice on which to host development or production applications, one often overlooked method of automation is the ability to create `development environments`.  Similar to the concept of storing images for use in `immutable` deployments explored earlier, it's greatly beneficial to generate an baseline image for a proper `developer environment` for your organization or even just the current project.

When a new developer joins the team, there's no need to spend hours installing the proper apps, making the appropriate configuration adjustments, or providing the correct access rights to the developer's machine.  With an `automated development environment` image ready to go, a copy of the standard developer environment can be copied to the new developer's machine, and all the necessary access rights, applications, and configurations will be included right out of the gate.  Best of all, this image can be used on a local machine or even remotely, via a virtual machine.

There are a number of existing tools that can be used for the creation and management of automated developer environments, but a few popular ones include [`Vagrant`] and [`Chef`].  Each tool comes with its own benefits, but they're all generally designed to be user-friendly, providing a simple API, using a common language or syntax, to create most any configuration as a new development image.

- Automated provisioning of servers is common, but automation can also be used to create development environments, locally or virtually, with identical tools and configurations for all developers across the team.
- Briefly discuss tools that can be used to easily provision new development environments, locally or via virtual machines (Vagrant, Chef, etc).
- Highlight the numerous benefits of automating the development environment across the team.

https://www.vagrantup.com/

## Automating Code Review

- Discuss the basic premise and benefits of `automated code review` throughout development life cycle.
- Highlight the growth of practices like `pair programming` and how automated code review takes those benefits further with checks for style consistency, coverage, etc.
- Provide examples of common code review automation tools.
- Emphasize the compatibility between `continuous integration` practices and `automated code review`.

https://codeclimate.com/
https://www.codacy.com/
https://codebeat.co/

## Automating Human Feedback

- Emphasize the importance of human feedback throughout the development life cycle.
- Focus on the ability of testers to provide detailed insight into uncommon scenarios and unforeseen test cases.
- Outline specifics of how some crowdtesting services might provide automation (API calls, recurring contracts, collaborative communication tools, etc).
- Detail how human feedback can be used to indicate the readiness of agile applications for future builds or even production releases.

---

[`HIPAA`]: https://www.hhs.gov/hipaa/
[`PCI`]: https://www.pcisecuritystandards.org/
[`Vagrant`]: https://www.vagrantup.com/
[`Chef`]: https://www.chef.io/

---

**SOURCE**

- 
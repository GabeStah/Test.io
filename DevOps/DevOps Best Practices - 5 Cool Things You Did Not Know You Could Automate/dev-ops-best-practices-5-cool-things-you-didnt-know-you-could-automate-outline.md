# [OUTLINE] DevOps Best Practices: 5 Cool Things You Didn't Know You Could Automate

> KEYWORD: devops best practices

- Introduction, which provides a broad mention of DevOps most common/well-known practices.
- Mention that this article aims to give some additional, not so obvious things that can be automated within DevOps.

## Automating an Immutable Infrastructure

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

- Discuss the importance of regulatory compliance in the development community, as it pertains to particular types of projects (government, financial, pharmaceutical, etc).
- Provide specific examples of automated compliance.
- Outline the fundamental components of compliance automation by providing a consistent, proven, and verifiable "paper trail" via automated development, testing, and deployment services.

http://searchitoperations.techtarget.com/news/450302065/Sparta-counters-DevOps-naysayers-with-compliance-automation

## Automating Development Environments

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
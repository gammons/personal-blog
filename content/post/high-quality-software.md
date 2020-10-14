---
author: "Grant Ammons"
title: How to deliver high-quality software
date: 2016-03-23T15:40:11-04:00
draft: false
---

When it comes to software, the term “QA” itself is highly loaded. Because what is it, really? Is it just a thing at the end of the software delivery line, where quality gets lovingly sprayed on at the end, achieving a nice glossy sheen? Is it a separate department that bolts on quality, where the engineers don’t really need to worry about it after they throw it over the wall? Is it that one integration test that one engineer wrote, once, and it’s “probably good enough”? Of course not!

So what goes into the process of _actually delivering high quality software?_ In essence, there’s 2 parts to this whole thing:
* **The QA step:** A verification check by a tester. It’s a series of testing, exploratory or automated, to ensure that newly built software is ready for prime time. When you Google “QA” you are generally reading about this step.
* **Development practices for writing high quality software:** The stuff that the engineers can do _throughout the entire development process_ to ensure their work will pass through those checks with flying colors. These are things like code reviews, ensuring proper unit + integration test coverage, and continuous delivery.

As an engineering leader, you need to define both of these parts. There are some practices that work better than others, and that’s what this post is about. So let’s run through the cast of characters: 

### Engineers

These are the people who put the quality in. **Enginers are the _only_ people who can directly control the quality of software**. Engineers also:

* Help other engineers with the quality of their code by means of code reviews.
* Write unit and integration tests for the code they create.
* May write automated tests at the browser/user level, using a tool like Selenium or Cypress. They may get help from the tester as to which automated tests to write.

### Testers

Testers are people who test the software and find bugs. They can then bring awareness of those bugs to the engineers.

Although engineers are usually very good about finding errors in their own code, not everything will be found. Testers are akin to an editor reading an article that someone wrote. While the writer probably did proofread well, they never catch everything themselves.

Testers can help guide engineers on which tests are important to write. These will likely be at the user level, but sometimes at a lower level as well.

Testers may or may not write automated tests at the browser level using a tool like Selenium or Cypress. It depends on their skill set. Sometimes testers will write those tests, but other times they can tell engineers to write those types of tests.

Skilled testers are usually very good at exploratory testing. They have a bizarre personality trait where breaking things, making things go haywire, and generally creating disorder and chaos is something they very much enjoy.

### Product managers

The main function of a PM is to ensure the team is delivering value to customers.  They are continually asking the question, "Are we building the correct thing?" They are are not looking for quality issues or bugs per se; they are instead looking to ensure the output matches their expectation for what the user should experience.

Building a high quality feature is a waste of time if it is not valuable to the customer. This is why the PM is also engaged in any changes.

# Practices that work well

So there’s a whole sea of practices that don’t really work. Handoffs, separate teams, throwing code over walls, no tests, and very large, complicated deployment processes are all signs that high quality software is not going to be delivered. So what does work?

### An integrated team

One or more testers should be a full-fledged part of a development team. When I was at PipelineDeals we have 4 engineers per team, and a shared designer and tester. The tester comes to all standup meetings and coordinates with the engineers as to which parts of the project are ready for them to test. Testers should be involved at all phases of the development process, starting with reviewing mockups.

Testers should not be a separate team that only gets involved in the late stages of the game. Nor should there be a handoff from dev to QA. Handoffs are a sign of a broken process and usually foster an [us-vs-them](http://royrapoport.blogspot.com/2016/02/the-failure-of-us.html) mentality.

### Engineers test first

Just as a writer wouldn’t hand over their work to their editor without proofreading it themselves first, engineers should perform exploratory tests first.

Before a tester executes their test plan, bring all the engineers in a room for a couple hours and test the system end-to-end. The engineers will find things. Usually the things they find can be fixed in realtime, to avoid further delays in testing.

Perhaps there is a staging (or similar) environment that they can test themselves with.  

After the engineers complete their own testing, the project will look much better than it did. The tester will waste less time with the low-hanging fruit and be able to concentrate on breaking things in much more devious and subtle ways.

### Automated tests

The output of exploratory and plan-based testing should feed into automated acceptance tests. Either the tester or engineers can write these automated tests, depending on the tester’s skill set.


{{< figure src="/images/qa_failed.jpeg" title="QA Failed!" >}}

### Code reviews

Code reviews are an excellent way of ensuring the quality of code that is going to be merged into master. engineers never want to look bad in front of their peers, so usually they will always go above and beyond to ensure their work will stand up to a review.

A code reviewer should be looking for the following:

1. Is this code maintainable? Is it understandable? Will engineers 6 months from now want to strangle the person who wrote it? We generally look to [Sandi Metz’s rules](https://robots.thoughtbot.com/sandi-metz-rules-for-developers) as a guide.
2. Does it have proper tests at the proper level? Code changes should always include unit tests, but sometimes (especially if coding across APIs) they should also include functional or integration tests as well. Do the tests exercise the code properly?

### Continuous delivery

[Continuous delivery](http://martinfowler.com/bliki/ContinuousDelivery.html) conveys tangible benefits to an engineering org. It reduces development costs and increases quality.  According to [_Accelerate_](https://www.amazon.com/Accelerate-Software-Performing-Technology-Organizations/dp/1942788339), the health of a product org can be meausred by their Devops best practices, and CI/CD is at the heart of that.

### Feature flags

Using [feature flags](https://www.infoq.com/news/2014/03/etsy-deploy-50-times-a-day/) is also a great practice. It allows us to iterate on new feature development while keeping small, short-lived branches. Because repeat after me: long-running branches are a Bad Thing. Why? Well, do you really think merging that 3-month-long mammoth of a branch into master, with the intention of deploying it on a Friday afternoon is going to go swimmingly? (It will not.) Large changes carry large risks.

Feature flags allow you to iterate on new feature development all while merging changes directly into the master branch, and it minimizes the risk that large branches carry with them.

The other benefit is a staged rollout. You can flip a feature on for your beta testers, or to a predetermined % of users. Staged rollouts allow you to do many things:

* Launch early to beta testers for user feedback
* Launch to a small % of users as a [canary release](http://martinfowler.com/bliki/CanaryRelease.html)
* Launch to a predermined cohort of users to guage performance impact
* A/B testing

### Your field guide to QA

When I was head of engineering at PipelineDeals, one of my goals was to ensure the delivery of high quality software. That included implementing a solid QA process. When Googling about that, of course, you get slammed with all sorts of different practices and results. The above is what works well for us, as a SaaS product company. Your Mileage May Vary.

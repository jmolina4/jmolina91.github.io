---
layout: post
title: "Fast-Feedback Development (FFD)"
date: 2021-12-07
desc: "Description of software development practises to shorten development feedback loop"
keywords: "Feedback, Team, Software"
tags: [teams, feedback, best-practices]
icon: icon-html
---
3 ideas:
- Writing software is hard and requires feedback
- The shorter the feedback loop the better
- Automation is better than manual

Chain of ideas: Too many ways of evolving products writing software -> CEO probably would say the one that allows us to deliver value faster -> what is the perfect combination if we want to fail fast and learn, the ones that shorten the feedback loop with the customer, with out team mates and the codebase. -> Automation is also important because techniques with short feedback loops that are manual can become long feedback loops with the time

Nowadays there are so many methodologies and "best practises" out there and sometimes we don't know which ones are ideal for our team. Should I use Scrum or Kanban? CI/CD or Continuos Deployment? Should we develop using Trunk-based development or instead Pull Requests? And the answer, as always in consultancy, it depends.
However, if you ask to a CEO of a company, they would probably want to use the methodology that enable team to deliver valueto their customers as soon as possible, and to accomplish that we need to pay attention to the feedback loops in software development.

## Why doees Software Engineering need Feedback loops?

Chain of ideas: Writing sftware must be easy -> after 10 years I'll know how to do it -> still not and that's because it's difficult to get it right -> complex problem -> we need feedback loops at different levels: Customer feedback, team mates feedback, codebase feedback.

We can categorise "Developing Software" as a complicated problem following the [Cynefin Framework](https://en.wikipedia.org/wiki/Cynefin_framework#Complicated), a problem that we know what needs to be done, we explore multiple options and finally we implement one of them.
But, is it always the reality? We have seen a lot the following picture where a customer wanted X but instead we delivered Y.
Moreover, this uncertainty not only applies to the features we need to implement in a product, but also when writing software. How many times have you written a code that you thought it would solve the problem and finally didn't?
<p align="center">
  <img src="https://treemidwest875.weebly.com/uploads/1/2/6/8/126884747/561201672.jpg">
</p>

If we look closer to the definition of "Engineering" from wikipedia it says:
> Engineering is the use of scientific principles to design and build machines, structures, and other items, including bridges, tunnels, roads, vehicles, and buildings.

And if we look at the definition of **scientific principles** we come up with this diagram:
<p align="center">
  <img width=320px height=300px src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/The_Scientific_Method.svg/1920px-The_Scientific_Method.svg.png">
</p>


It clearly states that this process consists on observing the problem, researching multiple solutions, formulate an hypothesis, test your hypothesis with an experiment, analyze the results, drive conclusions and start again until you finally solve your problem.
Usually this process is called Feedback loop, and over the last years there have been many strategies proposed to shorten this feedback loop. 
**The shorter the feedback loop is, the faster we will get to conclusions and, therefore, the faster we will deliver the right thing to our customers.**

In this series of posts I will explain the different strategies that have been used and most importantly, categorize them based on how long/short is feedback loop when you use them in a development team. 


## Customer feedback
Chain of ideas: in the past waterfall, feedback after many months -> nowadays agile methodologies: scrum or kanban.
- Scrum -> timeframe = weeks.
- Kanban -> timeframe = days. (winner)

- Manual deployment = minutes to hours
- CI/CD = minutes to hours
- Continuous Deployment = minutes

## Team feedback
Chain of ideas: writing software is complex -> we need other developers to also read our codebase and provide feedback -> Code reviews: Pair Programming, Pull Requests or combine both.
Pair programming + Trunk based development = seconds, minutes / slow short term but fast long term + more expensive
Pull Requests = hours, days, or weeks. / difficult to get context to properly provide feedback
Both = hours , days


### Codebase feedback
Chain of ideas: Individually we also need to know if our codebase works -> no tests, tests after writing code, TDD.
No tests = from seconds to minutes
tests after writing code = minutes
TDD = seconds to minutes


## Best combination
- Customer feedback: Kanban + Continuous Delivery + Trunk based Development
- Team feedback: Pair programming + Trunk Based development
- Codebase feedback: TDD


# Conclusion
Writing software is hard -> needs short feedback loops -> techniques that provide short feedback loop with automation
---
layout: post
title: "The mechanisms to build long-term high-performing teams"
date: 2021-06-13
desc: ""
keywords: "Leadership, Team, Software"
categories: [software development]
tags: [sw, developers, engineer]
icon: icon-html
---
<p align="center">
  <img width="650" height="500" src="/static/assets/img/team.jpeg">
</p>

Have you ever seen yourself as a leader telling your developers exactly how a feature needed to be coded to follow a set of good practices? Or, have you ever been in a meeting with the team and the client and you are the first one providing a solution to the problem? You are probably following the **leader-follower** model and, in my experience, while following this model you might succeed in the short term, building a short-term high-performing team, but in the mid-long term, the performance of your team will not improve anymore, they will rely on you to solve the problems and they will be less motivated.

In this article we will explain why the traditional leader-follower model does not work in Software Development and how to transition to a model that gives more autonomy to the employees and ultimately improves the long-term performance of your teams, the **leader-leader model**, proposed by David Marquet in his book “Turn the ship around!”.
<br/>

# Why does the leader-follower model not work in Software Development?
The leader-follower model has been applied over the last decades in jobs that required mostly physical and repetitive work (i.e builder, farmer…). In this model, the steps to accomplish your objective are clearly defined and therefore, there is no room for imagination or creativity, hence the goal of the leader is to constantly remind followers what they need to do and how they need to do it. Followers, on the other side, will simply accept the orders and try to get everything done, no decision-making authority is needed.

However, in Software Development, there are infinite ways of solving the same problem and to pick the least bad one you need to make some trade-offs, which requires imagination and creativity. In this scenario, if a follower takes an order to write specific code from their lead, they don’t have space to propose the solution they think is best, therefore, they are not empowered to make decisions of their own volition. In short this means that little incentive is given for them to use their intellect, energy and passion since there would be someone else “smarter” telling them the solutions. Motivation goes down.
<br/>

# Moving towards a leader-leader model
The leader-leader model considers everyone as a figure with authority and decision-making power, no matter if they are a Developer, UX (User Experience) or PO (Product Owner).
Let me give you an example of a situation where following the leader-leader model will be more beneficial than the leader-follower model.

Imagine that you have a meeting to decide which architecture will fit better for an application you are about to develop.

In the leader-follower model, the tech lead will open the meeting and propose different options and probably will try to convince the developers to pick the one that he/she thinks is the best.
Now, in a leader-leader world, the tech lead opens the meeting and explains the problem we are trying to solve, provides as much information as possible and asks every team member what their preferred solution would be. It might happen that they get to a consensus and if not the tech lead would consider everyone’s input and try to make the best possible decision.

As you can see, in the first example the followers are just told, whereas in the second one they have CONTROL over the decision and they feel empowered to make an impact in the team. The first step to moving towards a leader-leader model is to **GIVE CONTROL**.

But, what if you designate a developer without enough knowledge to come up with a solution for a complex problem? Or, what if, instead you delegate it to someone with great technical skills who just joined the company and is not yet aware of the company’s interests? In the first scenario the developer will probably lack some technical skills to properly solve the problem, and in the second one, the solution might not be aligned with the company strategy. 
Giving control is not as easy as it sounds.

Therefore, to **GIVE CONTROL** and come up with the best possible solution, you need to make sure that your team is **TECHNICALLY COMPETENT** and that they are aware of the **COMPANY GOALS**.

For that, David Marquet came up with mechanisms that help us as leads to make sure that our team members have the necessary skills and enough context to make a wise decision, and therefore, have control.
They are mechanisms of control, mechanisms of competence and mechanisms of clarity.
<br/>

# Mechanisms of control
Imagine Emma is the tech lead of the “Customer” team responsible for increasing the customer satisfaction of your application. One day she gets a request to create a mechanism for the customers to provide feedback and she shares the request with the team. She starts creating user stories for the team to know what to do and she also explains how the feature should be implemented. Bob, a senior developer who has been in the team for 6 months already, picks a user story and after one hour asks Emma about an implementation detail and she answers him. Finally, Bob finishes the feature and he creates a Pull Request for Emma to review, and since she finds a lot of improvements, she decides to rewrite the code Bob implemented in a “better” way.

What do you think Bob’s motivation will look like? Do you think he has space to grow?
As Daniel H. Pink states in his book “Drive”, autonomy is one key factor for a person to be motivated. For a team or a team member to be autonomous they need to be in control of the things they are accountable for, and here you have some mechanisms to accomplish it:
<br/>

## Eliminate top-down monitoring systems
When Emma reviews the Pull Request from Bob, the message we are sending to our team members is: “I don’t fully trust your code, I need to review it because I can do it better.”

What if instead of having the tech lead reviewing the Pull Requests of all developers, we encourage them to have constant code reviews between them (i.e pull request revision between them or pair programming)?
The message will completely change to “I trust you, you are professionals and you know how to deal with the problem, do whatever you think is best.”

*“Don’t move information to authority, move authority to the information”*
<br/>

## Resist the urge to provide solutions
Since a tech lead might be seen as a “superior’’ developer, we need to be careful with whatever we say to our developers. The fact that we provide a solution before giving the space to developers to think about it and share their thoughts will prevent them from coming up with ideas. As a developer you might think, why do I need to think about it if my tech lead always has a solution?

So, instead of explaining in the user story how the feature needs to be implemented, just write down some technical requirements and let the developers figure out the implementation details.

But, what if a developer comes and asks me for a solution? Answer them with questions like: “What do you think?” Or, “What are the benefits and downsides of doing it this way?”

They will feel more empowered, trusted and you will help them grow.
<br/>

## Use “I intend to…” to turn passive followers into active leaders
Because Bob has received a lot of instructions from the tech lead on how to implement the feature, whenever he is doubting he will ask Emma, putting the accountability of the decision on her.

What if instead of Bob asking Emma, “Should I create a new class in this folder?”, Bob asks: “I intend to create a new class to encapsulate the logic and decouple it from the controller”. Emma might then reply “sounds good!”.
“I intend to…” is a technique to provide information about what it is that we are trying to achieve and why while keeping people accountable for their actions forcing them to think deeper about the solution.
<br/>

# Mechanisms of Competence
Every single lead might be more or less comfortable giving control to a senior developer, but what if instead, we give it to a junior developer? The mechanisms of competence will help the lead to make sure their team members are capable of solving any problem they face without giving them the solution.
<br/>

## We learn (everywhere, all the time)
Even though Bob is a senior developer, he has never worked with Functional Programming and while Emma is pairing with him she decides to take the keyboard most of the time, not giving him the opportunity to try and fail. In the next pairing session, Bob feels that the story should be finished as soon as possible and he asks Emma to keep writing code to not slow down the team.

Nowadays, when we measure a team’s performance we think about velocity or lead/cycle time and it might seem contradictory to say that we have to spend time constantly learning if we want to become a high-performing team. The truth is that at the beginning the team might be slower until team members manage to balance their skills accordingly.

Your task as a leader is to acknowledge that developers don’t know everything, create a safe space and encourage Bob and the rest of the team to improve their skills. You can give feedback while pairing or recommend books or training.
<br/>

## Continually and consistently repeat the message
Emma is very strong technically and she knows that to provide quality to the codebase, tests at different levels are needed and documentation is useful, especially in a remote setup. That’s why she wrote down some of these good practices in a document and shared them once with the team.

When Emma detected in the Pull Request that the code was not following some of those best practices, she decided to rewrite the code. You could say that it's the developer’s fault since they did not follow the guidelines. Well, it turns out that hearing something once is not enough for other people to remember it and internalize it, therefore your task as a leader is to constantly remind them about what you really care about.
<br/>

## Specify goals, not methods
Specifying methods means telling Bob exactly what to do in order to finish the feature, therefore we are not letting him think about the problem and therefore not helping him to grow.
Moreover, when implementation details are given without any direction, if Bob faces a blocker in one of these tasks he will need to ask Emma about how to proceed, making Emma a single point of failure in the team.

As leaders, we need to specify goals, provide requirements and set the direction for the developers. They will come up with an implementation that might or might not be exactly the one we would go for, but it will still solve the problem. We will give them space to grow and also we won’t become blockers. 
<br/>


# Mechanisms of Clarity
Once our team has enough skills to develop whatever is needed, we need to make sure that they are also aligned with the company’s direction or interests. 

Bob has recently joined the team and he does not know that the company is going through some financial issues and that it needs to save money. Therefore, he decides to use an expensive AWS resource in order to implement one of the features that it’s needed.

Missing clarity in the team means that even though a solution can be provided, it might not be the best one aligned with the company's interests and we need to make sure as leaders that this does not happen.
<br/>

## Build trust and take care of your people
Bob has recently joined the company and, like most of us, he wants to be seen as a high-performing employee. However, he has some concerns about the indications that Emma provided him because he still does not trust her and he is afraid that doing so might be considered a failure.

If leaders build trust with all their employees, they all will reach out to us whenever they have any issue and having a conversation with them will allow us to be more aligned with what we are trying to achieve, together.
<br/>

## Encourage a questioning attitude over blind obedience
Since Emma is considered one of the best developers in the company, most of her team members are afraid of asking questions or challenging her assumptions. “She might know best”, they think.

I can promise you that as a leader, you will be wrong a lot of times. Therefore, if we encourage a questioning attitude in the team, team members will feel comfortable asking you questions and might make you think about your proposal saving the team from going in the wrong direction.
<br/>

## Use immediate recognition to reinforce desired behaviors
Some leaders set the expectations of their team members pretty high and when they accomplish something that could have been difficult for them, leaders don’t appreciate it enough, they might say “that’s fine, this is what they have to do''  without giving any positive feedback.

When there’s clarity missing in the team, telling developers what’s aligned with the company's interests and what’s not will let them know what are the expected behaviors and therefore, reinforce them.
<br/>

# Conclusion
Although our tech lead, Emma, has been following the leader-follower model for some years, the good news is that she can still change to a leader-leader model where every team member will feel empowered to make their own decisions. 
To do so, she will need to apply some mechanisms of competence to make sure that her team has enough technical skills to develop the solutions with the right quality and also mechanisms of clarity to align these solutions with the company's interests. Once there, and not before, she will be able to give control to her team to address all team problems autonomously without becoming a blocker or a single point of failure.





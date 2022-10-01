---
layout: post
title: "Automated Testing: The key to succeed in developing Data Products (Part 1)"
date: 2022-09-29
desc: "The risks of not implementing automated testing since the beginning of a Data Mesh journey"
keywords: "datamesh, data, testing"
tags: [datamesh, data, testing]
icon: icon-html
---
![Data Quality Testing]({{site.baseurl}}/images/automated_tests/data_quality_testing.jpeg)

[Data Mesh](https://martinfowler.com/articles/data-mesh-principles.html) is a new paradigm that is becoming more popular. Companies with the goal to extract value from data at scale look for alternatives to centralized data engineering teams and data lake/warehouse architectures. As with every new paradigm there are details that the community is still working out. Testing Data Products is one of them.

Data Pipelines serve only one purpose, they are implemented once and evolved from time to time. To test them, you might have testing environments (UAT, Test, Staging…) where either the same Data Engineers or QA would manually check that transformations work as expected. This approach takes a lot of time, requires communication between developers and QA and is prone to human mistakes. All summed up, it leads to a longer time to deploy to production successfully.

With Data Products, this is even worse. Data Products can serve multiple consumers and improvements are constantly requested, they evolve more often than Data Pipelines. Evolving more often means writing more code and more integrations. With more code and more integrations, your ability to keep all the logic in your brain decreases and, thus, the risk of introducing bugs goes up. But instead of relying on your brain capacity, you can rely on automated tests as a mechanism to detect when something goes wrong.

In this post I will explain why not defining a proper testing strategy before implementing a data product can negatively impact the team delivery capacity and quality of the output ports in the mid to long term.

# Towards Data Mesh!

Imagine you work in a company that has experienced exponential growth in the last two years. The central Data Engineering team is overwhelmed with the amount of requests to fulfill the required analytical use cases. To address this situation, the CTO and CDO of the company decide to move to a Data Mesh paradigm. They explain to you that Data Mesh is a sociotechnical approach to share, access, and manage analytical data in complex and large-scale environments — within or across organizations. Instead of treating data as a byproduct of code, the  [Data as a Product principle](https://www.thoughtworks.com/en-es/about-us/events/webinars/core-principles-of-data-mesh/data-as-a-product)  in Data Mesh applies product thinking to data in order to make it truly usable and delightful for the customer.

Since Governance, Data Product and Platform teams are already set up, you are ready to build your first data product that will enrich Customer Events coming from the app (e.g. “Customer logged in”) with Customer data from the operational system. This data product is driven by the need of every analyst and data scientist to join with customer data at the beginning of their scripts to extract value from the events. If they can consume a data product that does this join then it will save them time and the organization will be confident that it’s done correctly.

This data product consumes Customer Events and enriches them with Customer Data in real time. It will be used by two main consumers, Data Scientists who will develop a model to predict customer behavior and a derived data product that will produce generic Customer KPIs, like metrics showing how successful we are in converting customers.

Data Scientists usually work with parquet files. They need the whole list of customer attributes so that they can experiment with the features and select the ones that perform best for their model. On the other side, the Customer KPIs data product needs only a subset of this data but they need it as soon as it’s ready to calculate metrics in real time.

![Customer Events Data Product with its input and output ports]({{site.baseurl}}/images/automated_tests/customer_data_product.png)
*Customer Events Data Product with its input and output ports*


# Let’s start coding

After a conversation with your consumers, your Data Product Owner comes up with a list of events to be enriched and the attributes needed. You open your laptop and type the code to read from the two input ports and ,later, to join the sources to enrich different types of events.

Once the code is ready you want to check whether or not it works. To do so, you deploy your Data Product into a Test environment for the QA to validate that it works. Because the amount of use cases is very limited and the code is pretty small, the QA manages to validate everything very fast.

![Data Product developer deploying to Prod with manual tests and few enriched events]({{site.baseurl}}/images/automated_tests/manual_tests.png)
*Data Product developer deploying to Prod with manual tests and few enriched events*


One month later, you have enriched twenty events and the consumers are really happy with the team velocity as well as the team efficiency, everything that has been deployed has been working well. However, as a team, you realize that time to go to production (i.e.  [lead time](https://www.agilealliance.org/glossary/lead-time/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'lead*20time))~searchTerm~'~sort~false~sortDirection~'asc~page~1))) is decreasing bit by bit and some bugs have started to appear. You perform a root-cause analysis and you find out multiple reasons.

First, QA needs to perform regression tests manually for every single enriched event and it’s taking them more time than it used to when there were few events. Second, use cases are getting more complicated. Data Product Developers and QA need to communicate more to properly validate the code, but there are some misunderstandings and some bugs sneaked into production. Finally, code is getting messier and we need to change multiple pieces of it to enrich a new attribute. This takes you more time to deliver a feature and the possibilities to introduce a bug increase. However, you are scared of  [refactoring](https://refactoring.com/)  your code because the QA process to ensure that nothing has broken can be very expensive.

![Developers and QA need a lot more communication]({{site.baseurl}}/images/automated_tests/dev_qa_struggle.png)
*Developers and QA need a lot more communication*

The following day, the Data Product Owner asks you for a critical piece of data for the Customer KPIs data product. The Leadership needs to make a very important decision. Your team starts to freak out because they don’t feel confident enough, but you need to make a decision. Either you deliver the data with the risk of providing low-quality data or you change the way you work, and then deliver the data afterwards. The team starts to lose trust in their ability to deliver. Even worse, they become scared that Data Mesh implementation might not continue if they don’t fix this situation.

# To continue or to stop?

As a team, you decide to not deliver the requested data without an improvement of the process first. It’s too risky. You know that even though you manage to successfully provide this data, the effort to do so will be very high and more critical requests will come afterwards. Therefore you think about two solutions: define a better process with QAs or write automated tests.

Asking QAs to test the data product in an isolated environment with minimal communication does not work. The current approach does not scale and sometimes QAs become a bottleneck to deploy to production. You can try to communicate more often but , after some research, you realize that in software development this approach hasn't worked well in the past either. On top of that, this solution won’t help in providing confidence to refactor your codebase.

The second approach considers writing automated tests. Unfortunately, you might need to redesign some parts of your architecture since your codebase was not guided by tests from the beginning. Therefore, Leadership will have to wait even longer than usual to get their data.

The bad news is that none of the scenarios are ideal and the chances for your stakeholders to be unhappy are pretty high. The good news is that you can prevent this from happening in the implementation of your following data products by having a well-defined testing strategy before jumping straight into implementation.

# How could you have done it better?

We all have been very tempted to not add tests at the beginning of a project to deliver something fast into production. However, we have seen that in the long-run the lack of them can mean trouble for the team and the business. Automated testing has been proven successfully in software development for years. They can benefit Data Product development by: improving time to production, reducing bug fixing costs and safe refactoring.

Although QAs can support us writing tests, they no longer need to be in charge of manually checking everything every time. Instead, tests would run in every deployment and if something fails the team will get notified. We are improving the time to go to production while making sure that all use cases are covered.

![Straightforward deployment to production with automated tests in place]({{site.baseurl}}/images/automated_tests/easy_deployment.png)
*Straightforward deployment to production with automated tests in place*

Second, fixing bugs has a cost. If the Leadership team makes a decision based on wrong Customer KPIs, your company might be investing a lot of money into the wrong initiative. The further the bug gets in the pipeline to production, the more it will cost. Automated testing helps us fix bugs before they are actually exposed to the consumers, therefore the cost of fixing them is very low.

![Resolving bugs early and often reduces associated costs]({{site.baseurl}}/images/automated_tests/resolve_bugs_early.png)
*Resolving bugs early and often reduces associated costs from https://azevedorafaela.com/2018/04/27/what-is-the-cost-of-a-bug/*


Finally, because the codebase will become more complex over time, refactoring will be needed. With automated tests you can change your transformations as much as you want because they will prevent you from generating a different result. After the refactoring, tests will tell you if the data you produce now is the same you were producing before.

![Tests observe that codebase still works after refactoring it]({{site.baseurl}}/images/automated_tests/refactor.png)
*Tests observe that codebase still works after refactoring it*

# Conclusion

A big mindset shift is happening with the adoption of Data Products, especially in team composition and product ownership. Data Product Developers need to take care of long-living data products that require changes in business rules, codebase refactoring and bug fixing. Even though it seems like a good idea to develop our Data Product without automated tests in the first place, there are several risks attached. With Automated Tests, the figure of the QA can still support the Data Product team in providing quality and you can get rid of most of the expensive manual tests. Finding bugs in production when your end consumers need to make important decisions can be very expensive. Instead, automated tests help you to discover bugs when writing the code, in an early stage. Finally, code will grow and the ability to refactor it will decrease unless you have automated tests that check your business logic.

Software developers struggled for years to maintain large codebases without automated tests because they were considered a waste of time. Now, almost every company has realized that in the mid to long term they pay off. Hopefully, Data Product teams will also adopt this practice, reduce the time to deploy features, prevent failures in production and most importantly, free themselves to focus on adding value to their Data Products.

In the second part of this article I will explain what kind of tests that can be used, how many of them should be implemented, and how much and what kind of data should be used as input.
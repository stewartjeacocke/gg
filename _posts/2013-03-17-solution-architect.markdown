---
layout: post
title:  "What does a Solution Architect actually do?"
---

Over the last few years I’ve often found myself working in the role of Solution Architect on large IT enabled business change programmes. This is often perceived as a rather mysterious role and I’m frequently asked questions along the lines of “What does a Solution Architect actually do?”. This post gives an example of the kind of work I’ve done in this role in the recent past.

One definition of a Solution Architect is that they lead the design of an IT solution that addresses specific business needs. This requires agreeing what elements of a business process should be automated and then specifying an appropriate high level design, or architecture, that will enable the IT system to meet those specific business requirements within the constraints (most commonly implementation cost and timescales) set by the organisation.

In my opinion one of the key skills is a willingness to make thought through compromises between conflicting factors and to spend time explaining the rationale for these compromises to project stakeholders. This is easiest to explain with an example and I was recently involved in a project at a large international bank that provides a good case study.

During the early part of a change delivery project a key task is establishing an estimated cost, schedule & architecture which will enable the successful delivery of the IT solution. This task is often led by the Solution Architect and generally requires making and agreeing trade-offs between the scope, cost and schedule.

## Step 1: Understand the business problem and context

The Business Objective for this project was very clear. Within the next year, the bank must comply with new regulations that require the regular submission of additional data to the regulator. This additional data provides an enterprise wide view of the firm’s current exposure to different kinds of risk.

It was agreed that given the nature of the objective a key influence on the solution was that implementation time was more important than delivery of all possible scope, which in turn was more important than implementation cost.

Some information on the current Enterprise Business Architecture was also provided. It showed that the firm manages each risk type independently and that there is minimal standardisation across, or integration between, the different parts of the organisation that manage each risk type (see figure 1).

## Step 2: Confirm the current state Application Architecture

After speaking to various individuals in the firm it became clear that, rather unsurprisingly, this business architecture is mirrored by the current Enterprise Application Architecture. Each department has created its own processes and IT systems to manage the risk that they deal with (see figure 2).

![Solution Architecture Figures]({{ 'assets/solution_architecture_figures.png' | relative_url }})

## Step 3: Confirm the high level requirements for the IT solution

Based on an understanding of the objective, the current state, knowledge of typical bank processes and some additional information provided by the regulator it was possible to agree with the stakeholders that the candidate high level requirements for the IT solution were:

1. Submit exposure data on a quarterly basis
2. Submit the data as XML and according to a data model specified by the regulator
3. Support the reconciliation of the data to various other published reports
4. Support reconciliation between different risk types
5. Support a data validation, adjustment and approval process
6. Provide these services in excess of 99% of the time between 01:00 GMT and 23:00 GMT Sun-Fri

## Step 4: Identify key gaps

The existing Application Architecture could support elements of most of the high level requirements. However it was apparent that there were two key gaps:

1. Missing data: the existing risk systems did not capture all the data items that would be needed
2. XML interface: There was nothing in the existing architecture that could submit the data as XML to the regulator

## Step 5: Consider Application Architecture solution options

There appeared to be two plausible solutions. The first, shown in figure 3, was a federated solution where each risk system is enhanced with its own XML interface and sends information directly to the regulator.

The second, shown in figure 4, was a centralised solution where each risk system feeds data to a new centralised database. In turn this database can provide data to a single XML interface that sends information to the regulator.

## Step 6: Evaluate the solution options

The key insight in the evaluation was that the cost, complexity and risk of the solution lie primarily in closing the data gap. The cost of building a component to submit the data as XML was likely to be insignificant compared to this.

The centralised architecture could meet all the high level requirements. However because it introduced a completely new IT system it would require a significant system integration test phase to confirm the correct integration between the existing risk systems and the centralised data store.

The federated solution could not meet the requirement to support reconciliation between different risk types. However it is a simpler solution and did not require such a significant integration test phase. For this reason the risk of missing the implementation deadline with the federated solution was lower than with the centralised solution.

Given that implementation schedule had been rated as more important than scope or functionality the recommended solution was therefore the federated solution. As always reaching this conclusion was relatively simple when compared with the process of getting all the stakeholders to agree that it was the correct decision.

## Step 7: Create an estimated cost & schedule

Once the solution architecture was confirmed we could start the process of estimating the cost and schedule. The schedule was derived by seeing that since there we no interdependencies the enhancements to each risk system could be delivered in parallel. Once this decision was made the schedule could be estimated by considering reasonable durations for each of the standard project phases.

Given that the solution enhanced existing systems there were no costs due to hardware or software licenses. Hence the delivery cost could be estimated solely by estimating the number of people required to deliver the changes to the IT systems.

As you can hopefully see no rocket science was required, however it was necessary to follow a logical approach to the decision making and also to be willing to take time explaining the rationale behind the recommendation.

# CRISP-DM

Picutre this: You've just been tapped to jump in a meeting to help with some vague notion of a business problem one of your teams is talking about.  Now what?  Do you sit back and let them all flush out the idea, and then you swoop in at the end with your fancy math and solve the problem they've come up with?  You could, but I can pretty much guarantee you the project will get off the rails and miss the mark somewhere along the lines if you do.

Ok then, is there a better way?  Glad you asked.  Yes.  Yes there is.  There's no reason to reinvent the wheel.  Some really smart people came before us a long time ago and gave us a pretty well thought out end-to-end process for data mining/science projects.  Enter CRISP-DM.


<h3>Cross Industry Standard Process for Data Mining (CRISP-DM)</h3>

Have you heard of deductive or inductive reasoning?  With deductive reasoning, we begin with a few basic axioms - simple true statements regarding how the world around us works.  Inductive is exactly the opposite where uncovering simple truths about some phenomenon is the _goal_ of the investigation, not the _starting_ point.  Out of inductive reasoning we get the scientific method that we briefly touched on in Chapter 2.  It's noteworthy that the process cycle we'll discuss here is a combination of the deductive mathematical methods in data mining, and experimentation and testing steps from the inductive scientific method {cite}`NIS_2009`.  

The Cross Industry Standard Process for Data Mining (CRISP-DM) framework in the {numref}`CRISP-DM-fig` framework is fairly straight foward and intuitive, and is the most widely used standard in the industry for data mining and analytics.  There have been proposed extensions and adaptations over time to address deficiencies in the model, but it is still regarded as the dominant resource that many teams follow.  You will see that it's extremely common to add in a layer of project management in some sort of agile or scrum methodology, which are very common today (e.g. IBM's Analytics Solutions Unified Method {cite}`IBM_WP_2016`).


```{figure} ../images/CRISP-DM.png
---
width: 400px
name: CRISP-DM-fig
---
CRISP-DM phases as the industry standard workflow process for data mining and analytics
```


<h5>Business Understanding</h5>

Starting from the beginning with Business Understanding seems straight forward enough.  I need to understand the business context, sure of course, you're probably saying.  Saying it and doing it well are two different things in practice though.  This one is deceivingly simple.  What could go wrong?  Well, first of all, do you think the business sponsor you're working with understands what your specialty is?  What you could do to help them?  What kinds of information you need to know?  Hopefully you answered "no" to all of these questions because I can assure they do not.  Unfortunately what this means is it's up to you, or at least someone on the team that understands the bridge between the business and data science, to be sure to ask all of the right questions and collect the relevant information you'll need to know.  And there's a long open-ended list of questions that will vary for each project.

We can cover a few common ones that will be good starter questions regardless of the project specifics.

- What is the current process you have now?
- What's the current level of performance (KPI's, metrics, etc.)?  Do you understand why it's not good enough?
- Are there special exceptions and considerations?
- What are the objectives for the project?  What are we trying to solve for?
- What are the deliverables?  A one time study?  A re-useable production solution?
- Who are the end users and what are their needs?
- And so many more...

You'll need to become comfortable with the general fact-finding and surveying of your business domain experts.  Asking one question and getting an answer is generally not the end of it.  Follow up questions will be required, new questions and clarifications will spring from their answers, and you'll need to observe the loop from Data Understanding back to Business Understanding in {numref}`CRISP-DM-fig` as new information becomes available.

This understanding of the business context is so critical to the success of a project that we devote the next section {doc}`../Chapter4/proj_scoping` to it as well.


<h5>Data Understanding</h5>

We haven't touched on this too much yet, but data is the life blood of our solutions.  All of our fancy methods rely on data.  This one is also extremely vital to the success of the project (as they all are really), but there's a few plot twists to consider when we start thinking about data.  The first is the data generation process, followed by access and acquisition, and lastly data quality.

On a practical level, do you know how the data was actually created?  I mean the actual physical process.  Is someone manually entering data into a spreadsheet?  Is it system generated?  Which systems?  When is it updated?  Are there revisions or restatements that you need to account for?  And many more questions.  Next, from a statistical point of view you'll learn that what we're really trying to do with our modeling efforts is uncover what's known as the **data generation process**, or _DGP_, which is the phenomenon or mechanism that creates the data we're observing.  If you can build a mathematical model that accurately reflects this process that created your data, then you've hit a home run.  You can now do all sorts of interesting things with your model, like investigating how changes to specific parameters will affect the system, simulate new data to study, make predictions, and run scenario planning queries.

For example, let's say you want to predict the lottery numbers.  And for the sake of argument, let's say it's not a completely random process.  So if you were to model the historical winning numbers and uncover a mathematical equation that represents the _DGP_ that created those historical numbers, then oh boy.  You'd be able to run simulations and hopefully be able to predict which numbers have the highest probably of being drawn this week.

Now let's talk about actually getting your hands on the data.  Do we have access to all of the technical environments that house the data?  Are we going to import offline manual files, open up an API (application programming interface) connection, or get it from the source?  Will the proof of concept method of ingesting data be the same as when we get to the production version, or do we need to create a new process?  If so, who will maintain the process after deployment?  Do we have any legal or contractual restrictions with what we're allowed to do with the data?  Are there security and complicance considerations if we're using private personal information (PPI) data?

You'll often hear the phrase "garbage in, garbage out".  We love our catchy little sound bites, but you'll learn this one is actually true.  You can't expect to be able to predict sales accurately if the historical data you collect to inform your models is completely untrustworthy and inaccurate.  Don't expect to be able to predict when a piece of machinery is going to breakdown if you can't get your hands on data without missing time periods.  And so on.

Hopefully you're starting to see why it's so much easier to just say "throw me an excel file so I can get started!", rather than doing it the right way by asking lots of questions and committing to understanding the process and data before proceeding too far.  I'll caution you again though.  This framework exists for a reason.  Skip it, or don't give it the attention it deserves, and I can all but promise you'll pay for it down the road with wasted time and effort.


<h5>Data Preparation</h5>


<h5>Modeling</h5>


<h5>Evaluation</h5>


<h5>Deployment</h5>
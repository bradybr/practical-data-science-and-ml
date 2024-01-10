# Project Ideation & Scoping

Project Scoping mostly refers to what we go through during the project ideation phases and the first Business Understanding phase of the CRISP-DM framework.  It's critical to be able to work with your business domain experts to generate lots of project ideas.  Most of them will go nowhere, but having a long list to talk about and choose from will spark new ideas, and can keep you from getting tunnel vision by focusing on just the one idea the business brought to us.  

Just as important as being able to build a robust backlog of potential project ideas, is to be able to quantify the estimated return on investment (ROI) and value of a project, which ultimately allows us to prioritize the list of projects so we can select which ones to work on.  Ugh.  This one... oh boy.  Just typing about it gives me the cold sweats.

Unfortunately you may find that this value estimation step can be a royal pain in your behind when you work for a large company.  Technical support teams like a data science group with large budgets and human resource payrolls are typically expected to constantly justify their existence.  Said another way, your executives will want to know what incremental value your team is brining to the organization.  This means being able to calculate the value of all of the projects we complete.  Sounds easy enough?  Just wait.  It's like herding cats trying to pin down a business person to give you even a vague ballpark estimate.  Trust me.  Way harder than it sounds.

This may all sound obvious, but let me assure you companies waste thousands of hours each year talking about and working on projects that should have been a no-brainer to skip.  Developing skills in these two areas of 1) Project Ideation, and 2) Project Scoping will set you head and shoulders above your peers and make you a stand out star to your leadership team.

<h3>Project Ideation</h3>

Let's start with how you should go about coming up with new project ideas.  

The best way in my experience is to have the data science team play facilitator, moderator, and consultancy roles up front.  Let the busines experts do what they do best, which is talk about what they know - the business.  This is where the projects come from, not from the data science domain.  This point can't be overstated so I'll reiterate.

```{tip}
The data science projects should originate from the business domains, not the data science teams.
```

What this means is the data science resources are never the project sponsors.  We never solve problems for ourselves.  The project problem will always come from some other function within the organziation, and we're just the tool that supplies the solution.  Remember, we're the skilled problem solvers armed with advanced methodologies, but most likely know very little about what the business teams care about.  There's no point in us working on something that a business team doesn't care about just because _we_ think it's important.  Believe it or not, this point is overlooked far too often and we try to push our solutions without support from the functional business owners.  It never works.  Never.

So let's start here.  Take a look at {numref}`ideation-ex-fig`.  It's a simple and logical progression of how you can get the ideas flowing.  The key is to move from one question to the next flushing out each topic that came from your business expert.

```{figure} ../images/ideation_ex.png
---
width: 900px
name: ideation-ex-fig
---
Example of an ideation session with a project sponsor
```

We start with finding out what Jim's **Responsibilities** are.  Why?  Well, there's no point in talking about supply chain project with Jim since he's in Sales.  His responsibilities are what he cares about.  People care about what they're incentivized to care about.  Get him to spit out all of the things he's responsible for.  Everything.  Stream of conciousness stuff here with no value judgements.  Don't worry about the quality of the information you're compiling just yet.  You're simply trying to list out everything Jim cares about.

Next, we go through his responsibilities list one by one and ask the same question for each:  What are all the **Decisions** you make that have to do with this Responsibility?  Why are we asking this question?  Because at the end of the day, this is what we can help with.  My data science solution can either somehow help him make a better decision than he can alone, or it might actually fully automate the decision entirely freeing Jim up to work on other things.  Tied to each decision Jim makes should also be considerations for what data or **Inputs** he uses to make each.  Maybe we won't end up making his ultimate Decision for him, but we might be able to supply him superior data or inputs that he can then use to still make a better decision than he could without us.  So for each Decision he makes we then go through and ask about what data or inputs he uses for each.

After the Decisions and Inputs, we're on to one of the most important ideas:  **Value** estimates.  Again, this is a tough one, but we've got to try.  My suggestion is to come up with simple ways to attach ballpark estimates.  We don't need to be perfect here.  Just values we can use to compare and rank each idea.  So if it's a time savings kind of project, use a simple formula like 

$$
total\:annual\:$\:savings = avg\:hrs\:saved\:\times\:avg\:$\:per\:hr\:\times\:2080\:annual\:hrs 
$$
<br>

Ok great, we hopefully have a long list of potential **Decisions** and **data inputs** we could predict, forecast, or optimize in some way with **Value** estimates attached for each. Now what? Now we get to the fun stuff.  We get to start doing what _we_ do!  We get to start asking a whole bunch of **What if** questions for the ideas that filtered to the top based on the value estimates we compiled.

```{note}
_What if we could predict...?  Would it be helpful to you if we could optimize...?  What resources, human, capital, or otherwise, would you allocate differently if I could forecast... for you?_  And so on. 
```

At this point you should be starting to see some serious potential for a good idea to work up a proof of concept with.  Hopefully this is resonating and you can visualize how this might work in the real world.

<h3>What Should We Document Before Starting a Project?</h3>

At this point consider you've gone through the ideation stage and you have a project you want to have a more detailed exploratory fact finding session with.  Remember when we were talking about domain expertise in Chapter 2 {doc}`../Chapter2/what_is_ds` and one of the main reasons why projects fail?  Well here we are.  I find my self wanting to tell you every step is critical, but I can't help myself.  This one really is critical.

If you don't have these next topics very clear right from the get-go, you will have nothing but trouble when the rubber meets the road and you start working.  You want to be crystal clear and make sure everyone agrees on what you're going to go off and do, otherwise you'll be smacked in the face with what's known as scope creep and you'll get side tracked very easily.

So let's go through the 5 points I recommend you always include in your early project scoping sessions using a simple example to illustrate.

 1. Business Need
 2. Objectives & Success Criteria
 3. Deliverables
 4. Scope
 5. ROI/Value

<h5>Business Need</h5>

Our shipping distribution center currently uses a manual process to evaluate daily customer orders and group them into consolidated shipments.  It’s a time consuming, manual process, and prone to sub optimization due to the soft decision guidelines and single point of failure (Transportation Clerk’s responsibility).

The transporation team is interested in creating a solution that will automate the truck grouping, sequencing, and optimization tasks, while maintaining or increasing the current level of truck utilization.

<h5>Objectives & Success Criteria</h5>

 1. Determine if opportunities for efficiencies or cost reduction exist
 2. Build an automated solution capable of evaluating daily orders and grouping them into shipments, observing the max weight and cube capacity constraints
 3. Must surpass current 60% avg cube utilization rate over 3 month period

<h5>Deliverables</h5>

 1. POC recommendation
 2. Production Web App/UI

<h5>Scope</h5>

 - Western regional routes and 3rd party consolidators only
 - All products

<h5>ROI/Value</h5>

 - \$160,000 in full truck load savings vs. LTL (less than truck load)
 - \$10,000 in time savings (100 hrs/yr @ $100/hr)

<h3>What Did We Learn?</h3>

Hopefully a sound understanding of all the ways your project could go sideways if you don't fully flush out what a good project looks like right from the beginning.  There are a million ways to get off track, but you'll increase your odds of success and working on the right projects if you're intentional and thoughtful in collecting as much information as possible before you commit any resources against an idea that hasn't been properly vetted.

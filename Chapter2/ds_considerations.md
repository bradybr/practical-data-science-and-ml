# Special Considerations

This will be a brief section, but I didn't want you to get too far along without starting to think about some of the unique complications and special considerations we deal with in the field.

Here's an example to motivate the ideas.  Image you're a Sr. Data Scientist for a large domestic financial and banking institution which specializes in affordable personal loans.  Your role is to build machine learning prediction models to review incoming applications for personal loans, and decide if we should approve or not based on their predicted repayment score.  Any applicant with a predicted repayment probability of less than 85% will be rejected.

Seems pretty straightforward, right?  All you'll need to do is collect a bunch of historical data and see if you can learn the differences between those that repaid their loans vs. those that did not.  Easy enough!

Not so fast.  Can you spot the first problem already?  It's nuanced so don't worry if you don't see it.  Ok, I'll just tell you.

By going straight to our historical data set of _approved_ loans we're introducing what's known as _bias_ right out of the gate.  The only people we'll have to learn from in our data set are people deemed credit worthy by whatever the process of approval was at that time.  So what, you might be asking?  Well, think about what happens now that our model will be reviewing **every** applicant going forward.  Our model has never seen anyone like the applicants that were previously rejected by a human and therefore not included in our training data.  Predictions from this model will be highly suspect and should be used with caution.

Will it be a problem?  Maybe.  Maybe not.  The point is we need to be able to identify these types of hidden issues that can easily tank our projects.  If we went ahead with it as is, we would need to keep the pre approval process by a human as we had for our training data.  That's the only way to be safe by making the training environment look like the production one.

Now, let's stay with the same example and consider we've solved the sampling bias issue in our historical training data somehow.  What are the individual details we might want to know to screen our applicants and inform our models what a good loan candidate looks like?  You might want to know how long an individual has been a customer of the bank?  How many accounts they have?  Account balances over time?  Any previous defaults?  And so one with more details about thier banking history.

How about personal details like demographics and socio-economics?  Age, race, marital status, employment history, income vs. debt history, etc.  These all seem like they can reasonably be expected to carry information that correlates somehow to our loan default target.  Not so fast again.  What if we find out that African Americans default at a rate 2.5x higher than caucasians?  Can you just stop giving loans to African Americans?  Of course not.  Besides just being plain reprehensible, race is a protected classification under Title VII of the Civil Rights Act so now we're taling about legal discrimination.  No good no matter how you look at it.

Let's say you decided not to restrict an entire race of people from getting loans (, but you did end up using race in your model because it yields a statistically better model.  Ok, sure.  That's legal.  But is it ethical?  Maybe.  Maybe not.  Your algorithms and models are cold and emotionless, and will not consider ethics natively.  It's your job as the analyst to think about the legal, ethical, and moral basis of what you're doing.  Just because you're not explicitly saying no loans for an entire group of people, it's still very possible you're still unknowingly discriminating.

The world or practitioners has taken huge strides in addressing just how dangerous so-called black box models can be.  If you don't understand what you or what your models are doing, it's very easy to let something like these examples happen.  Besides the ethical implications, new laws are being enacted all the time so there are very real consequences for not being dilligent in your thoughtfulness.

We could go on and on, but hopefully these few simple examples may at least make you aware there are potential dangerous out there.  This is a reoccurring theme you'll see us bring up again and again as we progress through the course, so enough for now.

```{tip}
Common sense and simply being courteous is in all of us.  Take care, and try to leave the world in a better state than you found it.
```
---
title: Jennifer Notes Dump
layout: content
image: water-paints-1057934-pxh.jpg
# permalink: /dump/
---

## Jennifer Qs
- Building data sheets into workflow tools— eg, Designer— so UX makes easier to add into flow in a way that allows for flexibility of diff workflows
- Making UX designers a key part of team just as they are w web development?
- Considering guerilla usability?  UX of tool builders
- Thought at all about trying out community-centered UX approach?


## What to Call It
- EU likes Explainability
- She prefers Intelligibility 

## Some basic approaches to intelligibility
- Dan Goldstein: simple point systems
- Rich Caruana: GAMs,  additive structure, so can visualize impact
- Approach 2: post hoc explaination
   -  LIME or SHAP
   - Can play w them on InterpretML - Azure ML also uses it
  
<hr/>


When I'm done, read the QA portion of this talk
and copy any answers I think are interesting

Jennifer:
rather than trying to talk with her, ask her questions by email. Also say, if it's easier/faster to just talk this through, let me know
Read her chapter on human centered agenda for intelligible ML before I get in touch

One of Microsoft's core AI principles: transparency

Microsoft's AETHER Committee: one of their core areas: intelligibility and explain ability

Jennifer questions:
Data sheets for Data sets:
Is Microsoft looking at making (ML?) Designer so it would be integrated into the process?
Behavior-driven programming?
(Kind of like coding documentation that's auto generated from comments in code, code structure)
For example, you sent automating
what playing with?
(I get your point, one size won't fit all)
And who is working on HCI of this?
More generally, is anyone doing any partnering with community groups around either the teaching of AI or around intelligibility?
For example, if you want to empirically test which factors will model enable users to better achieve their goals, working with community will give you 24, in my experience: difference between sales rep and say machinist isn't that huge
(freewrite to explain why)


Partnership on AI:
About ML: playing off data sheets, Google Cards, etc.


Three components of transparency:
1) Traceability: assumptions, goals, design choices etc.
2) Communication: if create/deploy AI system, be open about the ways they use AI and about the limitations of their tech
3) intelligibility/interpretability/explain ability: stakeholders of AI systems should be able to understand and monitor the technical behavior of those systems to the extent necessary to achieve their goals

Brings in HCI: Something can't be intelligible unless it is intelligible to someone

"Microsoft transparency notes"

Why intelligibility:
bullets make it easier for data scientists to identify and fix bugs
can help doctors, CEOs, etc. decide when and how to trust AI
Allows designers to reason about how systems and models behave in order to convey that information to end users
can uncover potential sources of bias
can help them with compliance with regulations
easier to develop models to create new hypotheses
leads to more usable products

2 basic approaches:
1) Simple models
Simple point systems (Jung 2017)
Generalized additive models (Caruana): has additive structures, so can visualize
2) post hoc explanations for complex models
LIME, SHAP: assigns and importance to each feature
Interpret ML: released by her colleagues
Azure ML offer offers something similar


But what intelligibility means and how to measure it is still up in the air
what makes a model or explanation simple, and how is simplicity related to intelligibility's2, and do these models help users achieve their goals
"you'll know it when you see it" is what most people think in machine learning world

intelligibility:
CEO versus regulator, who wants to know why an individual was denied a loan
versus debugging a model
Plus, all models so far have focused on the model itself,
depending on who the stakeholders are, may want intelligibility at other stages, including definition of the problem/task all the way through feedback

Her approach:
a human centered agenda for intelligible ML
Read her book chapter!
Has more detail on how they envision it

Overall approach:
•	Poursabzi-Sangdeh, 2019: stop relying on intuition, empirically test which factors will model enable users to better achieve their goals
•	yin, 2019: consider intelligibility beyond model, e.g., intelligibility of performance measures, objectives, etc.
•	Kaur, 2019: design and evaluate methods for achieving intelligibility in context with relevant stakeholders

study on how data scientists perceive and use intelligibility tools
Properties that influence intelligibility
System Design: number features, if the model is linear, user interface, clear versus black box
Properties of human behavior: trust, ability to debug, ability to simulate
their study: very the system design properties, see impact on human behavior
Really hard to do this while holding all other factors of a model equal

The first experiment: sale price of apartments
2 vs 8 features X clear linear regression model with weights vs black box
Findings:
clear model with small number features were easiest for participants to simulate
But transparency reduced people's ability to detect when the model made a sizable mistake and corrected, seemingly due to information overload
And that's why experimentation and user testing is so critical :-)

They did a study that's essentially on intelligibility of performance metrics





 
People to research:
Finale Doshi-Velez: interpretable machine learning
Been Kim: interpretable machine learning

Zachary Lipton: the mythos of model interpretability
(Researched the folks above)

Poursabzi-Sangdeh, 2019: stop relying on intuition, empirically test which factors will model enable users to better achieve their goals

yin, 2019: consider intelligibility beyond model, e.g., intelligibility of performance measures, objectives, etc.

Kaur, 2019: design and evaluate methods for achieving intelligibility in context with relevant stakeholders

When I'm done, read the QA portion of this talk
and copy any answers I think are interesting

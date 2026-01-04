# **MS&E 318: Constrained and Safe AI**

How can we design AI systems that are not only powerful but also provably safe and trustworthy? This advanced PhD seminar surveys algorithmic methods to enforce hard constraints in machine learning, reinforcement learning, and generative AI. 
Topics include classical constrained optimization (Lagrangian methods, robust and stochastic programming), 
safe reinforcement learning (trust regions, Lyapunov functions, reachability), 
hybrid ML-optimization methods (projection networks, solver-in-the-loop architectures), 
and alignment strategies for large language models (fine-tuning, model editing, tool use, and interactive alignment). 
We will consider applications to robotics, finance, healthcare, energy, and personal AI assistants. 
Topics may change according to student interest.
Prerequisites: optimization at the level of CME 307 or EE 364a.

For each topic, we will begin with a foundational mini-lecture,
followed by student-led discussion on modern research papers.
The course will culminate in a final research project
which will constitute a majority of the grade.

# Logistics

* **When:** 1:30-4:20pm Tuesdays Jan 9-March 10
* **Where:** [McCullough 122](https://campus-map.stanford.edu/?srch=McCullough+122) or on [Zoom](https://stanford.zoom.us/j/6394072382?pwd=bndKcXBpRFdOb2x5VFhuT0kzN1QvQT09) by prior arrangement with the instructor
* You can schedule [Office hours](https://calendar.app.google/sCu1wpZXkUdAXdA59) on this calendar or chat with Prof. Udell after class.

# Learning goals

Students who complete the course should be able to:

* Formulate AI problems with explicit hard constraints and identify appropriate enforcement mechanisms.
* Compare Lagrangian, projection-based, and solver-in-the-loop approaches theoretically and empirically.
* Critically evaluate safety and alignment claims in modern ML papers.
* Design a constrained AI system with provable guarantees or well-justified approximations.
* Contribute to the research literature on constrained and safe AI, at the level of a workshop or conference submission to ICML, NeurIPS, or ICLR.

# Course format and requirements

Students are required to attend class, with at most one absence.
(Any student may also attend up to one class remotely via [Zoom](https://stanford.zoom.us/j/6394072382?pwd=bndKcXBpRFdOb2x5VFhuT0kzN1QvQT09),
or more by prior arrangement with the instructor.)

Course grades have three components:

* **Quiz** (.1): Most classes will begin with a short quiz to reinforce the main ideas of the reading.
Your lowest quiz score will be dropped.
* **Present a paper** (.3): Students will each lead a discussion on a paper twice (or so), likely in teams
depending on course enrollment.
The student leading the discussion will prepare a 30 minute presentation using slides,
two quiz questions on the paper,
and a class activity or questions for discussion.
* **Research project** (.6):
The final research project should explore a new idea for safe and constrained AI.
Projects can be in teams of up to three students except by
special advance permission from the instructor.
Students will prepare an initial project proposal, midterm report, and final report
on the project, and may make an in-class presentation.
Research projects can (and should!) advance your PhD research.

<!-- Students taking the class for 1 credit will be required
to write fewer reviews,
present only one paper,
and will not be required to complete the research project.
The quiz requirement will be the same. -->

# Schedule

[This google doc serves as our schedule.](https://docs.google.com/spreadsheets/d/1qYS6aMa5TyBz1OmN1CT787XdBiAisVg9pACr-XSaN9A/edit?gid=0#gid=0)
A tentative schedule follows.
We may spend more or less time on a topic depending on student interest.

| Date (Tue) | Topic |
|---|---|
| 1/6/2026 | Intro: importance of constraints + classical approaches to handling constraints |
| 1/13/2026 | No class; read ahead and select papers to present |
| 1/20/2026 | Stochastic and robust optimization |
| 1/27/2026 | Reinforcement learning |
| 2/3/2026 | Reinforcement learning |
| 2/10/2026 | Projection |
| 2/17/2026 | Declarative programming |
| 2/24/2026 | LLM alignment |
| 3/3/2026 | Model Editing and Post-Training Interventions |
| 3/10/2026 | Synthesis and future directions |

<!-- Sign up for presentation slots on the google doc
by adding your name and a link to the paper you'll present.
(Make sure not to choose a paper someone else has already picked!)
We may spend more or less time on a topic depending on student interest. -->

# Presentations

## Outline

1. Intro
    - how does this topic relate to the course goal of enabling safe and constrained AI?
    - what is the core idea?
    - what applications does it target?
2. Literature review
    - what are the important papers and ideas?
    - walk us through the intellectual history
3. Deep dive
    - pick one or two papers, and take us through the main idea and results
    - extract some core mathematical insights, and choose one to explain on the board. could be a theorem or result from the paper, or some older mathematics that motivates the approach. feel free to show how it works on a simple example, like a quadratic objective with linear constraints.
4. Results
    - summary of numerical results from papers
    - do you think the results are good or bad? Are there obvious omissions?
5. Open directions
    - what are the important problems that you think could be addressed with these ideas, but haven't yet been?
    - is there a key challenge that restricts the usefulness of this approach?

You might also loop through 2-5 several times, one for each of the most important papers in your stack.

## An AI-forward protocol

Here's the best workflow I've found for producing good presentations on new topics.

1. Collect a list of papers and authors whose work you admire on the topic.
2. Use that list to prompt a frontier LLM (GPT5, Gemini) to do deep research on the topic and write a report. A prompt might be, "Summarize the state of the art in <field>, including work by <authors>." You might also inject your own biases and interests here.
3. Ask Claude code to download all the references in the report into a folder on your computer. 
4. Read the report, and skim the papers to check that the understanding you gleaned from the report is correct.
5. Upload all the papers to NotebookLM. 
6. Have a conversation with NotebookLM to deepen your understanding of the topic and ask more detailed mathematical questions about the papers.
7. Write a script for a presentation you'd like to give on the topic, noting the high level points you'd want to make, or categories or topics you'd want to hit, or conclusions you'd like to come to. Ask NotebookLM to create a slide deck, using your script as the prompt. Here's a prompt I've used:

> Develop a tutorial review of standard ideas in constrained optimization, in particular lagrangian methods and duality, with an eye towards their use in a modern deep learning setting for a PhD audience already familiar with optimization at the level of Boyd and Vandenberghe. Use a plain, latex beamer style slide template with a white background. All numerical results (in particular, tables and figures) must exactly match the source material and reference the source.

8. Study the materials and practice your presentation. Be meticulous and make sure you believe and can justify every claim on the slides.

## Checklist

In addition to following the above outline (approximately), presentations must include
* quiz (2 questions that are easy to answer from the required reading)
* discussion questions or class activity

before the presentation
* (Monday 11am) email Prof. Udell with an editable draft of slides, quiz questions, and discussion questions
* (Tuesday 1pm) submit a PR to the class git repo with your slides

bring
* power
* anything needed for you to connect to a USB-C or HDMI cable

setup
* projector
* camera
* [zoom](https://stanford.zoom.us/j/6394072382?pwd=bndKcXBpRFdOb2x5VFhuT0kzN1QvQT09)
* share screen

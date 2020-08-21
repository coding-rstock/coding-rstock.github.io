---
title: Pragmatic Thinking & Learning - Book Report
date: 2020-08-19
categories: 
tags: []     # TAG names should always be lowercase
author: Richard Stock
layout: post
permalink: /pragmatic_thinking_and_learning
---

### Chapter 1: Introduction
---

- Point of book is to improve your thinking and learning skills (refactor your wetware) to make you more effective at programming.
- Programming is problem solving.
- Programming error is human error (it’s always our fault). We’ve lost track of the fundamentals.
- The 2 most important modern day skills are: 1) communication skills, 2) learning and thinking skills.  Of these, learning and thinking skills are tougher to develop.  

    **1.Communication Skills**:
    - Software isn’t designed on an island, it’s done in teams, and therefore social interaction poses hard challenges and problems.
    - Agile methods emphasize improved team communication skills.
    <br/><br/>

    **2.Learning & Thinking Skills**:
    - Software isn’t designed in our IDE, it’s imagined and created in our heads.
    - Software must continually evolve because its underlying systems (users, machines, laws, applications) are always evolving and force change.  
    - This means programmers must learn constantly - new systems, new programs, new languages, the shifting whims and fancies of the user community, quirks of their teammates, industry shifts, etc.
    - As you grow and adapt, you need to modify your habits and approaches.
    - We sometimes look at the teacher student relationship the wrong way.  Critical thinking, creativity, invention, and learning are up to the student (the coder), NOT the teacher.  It’s all up to you!
    <br/><br/>

- Agile Methods:  favoring real time feedback over rigid rules and schedules.
Pragmatism:  do what works for YOU.  Every brain is different and wired differently.
- Interconnected Reality of Nonlinear Systems:  due to everything being interconnected in programming, small mistakes can have large consequences.
Intuition is the hallmark of an expert, but it is tricky as it has many “bugs”.  We often fight against it, but need to learn to give it freer reign by debugging it.
- Tools for ‘Deliberate Learning’:  Planning techniques, mind maps, reading techniques (SQ3R), teaching, writing.  Learning these techniques will enable you to absorb new information faster and easier, gain more insights, and retain the info better.
- Experience: We learn best by doing.  However just “doing” alone is no guarantee of success, you have to learn from the doing.  Also ‘trying hard’ isn’t doing, especially if you are just further ingraining your bad habits.  
- Attention and Focus:  These need to be managed.  Interruptions are cognitive train wrecks.

### Chapter 2: Journey from Novice to Expert
---
- Dreyfus model of skill acquisition:  developed by 2 programmers who were attempting to build an AI capable of learning human skills.  5 discrete steps from novice to expert.

    **1. Stage 1:  Novices**
    - Little or no experience in the skill.
    - Concerned about success rather than learning the skill.
    - Do not know how to handle mistakes, vulnerable to confusion when things are awry.
    - Need a recipe, step by step process, if x then y happens, etc.
    - Problem with recipes is that you can never specify everything fully. Every or any step can unravel when you throw different situations into the mix, which require more rules to prop up the first rule, which in turn require more rules, which require more rules… this is called infinite regression.  At some point, you have to stop defining explicitly.  Rules can get you started, but they won’t carry you further.
    <br/><br/>

    **2. Stage 2:  Advanced Beginners**
    - Can start breaking away from the rule set a little bit.  Can try tasks on their own, but have trouble troubleshooting.
    - Want information fast, do not want to be bogged down with lengthy theory or spoon fed the basics again.  Will scan documentation for specific answers.
    - Can start using advice in the correct context, but just barely (there is no big picture yet).
    <br/><br/>

    **3. Stage 3:  Competent**
    - Can develop conceptual models of the problem domain.  
    - Can troubleshoot problems on their own and solve novel problems.
    - Can begin to seek out advice from experts and use it effectively.
    - Still a bit of trouble determining which details to focus on when problem solving.
    - Typically described by others as “resourceful” and “having initiative”.
    - Tend to take a leadership role on a team, whether formal or not.
    - Can mentor novices yet not annoy experts too much.
    - Can’t yet apply agile methods as there isn’t enough ability for reflection and self correction. 
4. **<u>Stage 4:  Proficient</u>** 
    - Need the big picture, will seek out and want to understand the larger conceptual framework around the skill.
    - Can correct previous poor task performance, by reflecting on how they’ve done and revising their future actions.
    - Can learn from experience of others (via case studies, gossip, observing what others have done, stories, etc).
    - Can apply maxims & proverbs, which are not recipes and must be applied in context. (ex: “test everything you can possibly break”).
    - Know from experience what is likely to happen next, and if it doesn’t, what to change.
Agile development uses feedback to make constant adjustments in a highly collaborative environment.” But being able to self-correct based on previous performance is possible only at the higher skill levels (proficient, expert).

5. <u>**Stage 5:  Expert**</u> 
   - Are the primary sources of knowledge in any field.
   - Continually are looking for better methods and ways of doing things.
   - Can apply their vast amount of knowledge in just the right context.
   - Write books, lecture, etc.
   - Probably only 1-5% in any field are experts.
   - Work from intuition, not reason, and yet are often inarticulate about how they arrived at a solution. They may genuinely not even know, and say “It just felt right”.
   - Very good at targeted focused pattern recognition.
   - Experts realize how much they don’t know, whereas lesser skilled people think they know a lot.
   - It takes about 10 years to become an expert, however once you become an expert in one field, it is easier to become an expert in another.
   - Experts have a different way of thinking when solving a problem or completing a task that often looks non-conventional or ‘magic’ to the common person.  Novices follow conventional practices and context free rules in a more systematic approach, under which an expert would feel too bound and constrained.

- Herding Racehorses and Racing Sheep: 

  - You can easily derail an expert and ruin their performance by forcing them to follow the rules. Rules ruin experts, even if they are the one who wrote those exact rules for the novices they are managing. This would be like herding a racehorse. Instead, you need to let them run with their intuition.

  - You can easily overwhelm a novice by throwing them in the deep end of development, far over their heads. This would be like racing sheep, when they need to be herded with unambiguous rules and systems, set up for quick successes, etc.

  - Industry typically dictates that all developers be treated the same due to political correctness. This works against both experts and novices. The truth is that there is a 20:1 to 40:1 difference in productivity between developers. 

  - Bottom line: use rules for novices, intuition for experts.

- Sad fact of Skill Distribution

    - Dreyfus model doesn’t follow bell curve, most people don’t make it past Stage 2, “performing the tasks they need and learning new tasks as the need arises but never acquiring a more broad-based, conceptual understanding of the task environment.”
    - Unfortunately this means most practitioners overestimate their skill level by 50%. 
    
- Hallmarks of an Expert

    - The hallmark of the expert is their use of intuition and the ability to recognise patterns in context. The expert’s intuition and pattern recognition now take the place of explicit knowledge.

    - This transition from the novice’s context-free rules to the expert’s context dependent intuition is one of the most interesting parts of the Dreyfus model; 

```
So our goal, for most of the rest of this book, is to see how we might better harness intuition and get better at recognising and applying patterns.
```

- Using the Dreyfus Method Effectively
  - Take responsibility: no matter what level of programmer you are on a team, you must take responsibility for the outcome of the project and speak up if you see something wrong or detrimental taking place.
  - Learn by watching and imitating.
  - Keep practising always to retain your skill level.
  - Beware the tool trap: don’t rely on a certain tool or framework or model. Rules cannot tell you the right path to take. 
  - Avoid formal methods if you need creativity, intuition, or inventiveness (expert traits).
  - Always consider the context, don’t try to be objective about something after taking it out of its context. Context matters in complex systems. 
  - Day to Day Dreyfus: Learn the skill of learning. Implement Dreyfus model to cultivate more intuition, realize the importance of context and observing situational patterns, and better harness our experience.
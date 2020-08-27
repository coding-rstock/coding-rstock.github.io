---
title: Nutrition App Design Principles
date: 2020-08-26
categories: 
tags: []     # TAG names should always be lowercase
author: Richard Stock
layout: post
---

### User Experience
---

**I want the user to have fun using this app.**

**1. I want the user to feel they are in full control of their diet plan** 
- There's no ambiguity or lack of understanding of what they need to eat and when to eat it (ie. user doesn't feel like they need another app or tool to supplement mine).

**2. I want the user to feel they are on a journey towards their ultimate destination/goal.** 
- App must be goal focused - why else would you go through all the pain of calculating macros?

**3. I want the user to feel they can't believe how simple it is compared with MyFitnessPal.** 
- Understanding ***and also*** implementing nutrition has always been my most frustrating experience when trying to achieve a goal due to:
	- (a) meal planning:  picking a recipe or foods to fit my macros (this is super technical and mathematical)
	- (b) meal prep:      how many meals, when to eat, figuring out grocery shopping list (and separating it - Costco, Superstore)

**4. I want the interface to be super inuitive and super clean.** 
- Minimal information on the screen (lots of clever integrations that only display info "just in time" as you need it).

**5. The target user is more advanced, so I want the design to be classy.** 
- I don't want this app doesn't get lumped in with the plethora of "abc-123", "all flash no substance" nutrition apps out there (this will be a "gold standard" "top shelf", "premium", "best on the market" experience).  
- Color scheme could reflect this (ex: dark grey scale backgrounds with gold icons/details etc, white for highlights) versus bright pastels. 

### Brainstorming - Potential Features
---

**Database**

1. User can create a custom database of their own foods, with the ability to scan items, and add vendor (Superstore/Costco/etc).  Benefits:
- Automatic grocery lists can be generated for each vendor.
- Very practical users can build meals from the foods they actually buy, and the way they prepare the food, not having to sort through 100,000 food items with different brands, cooking methods, etc.
2. fasd

**Meal Planning**

1. Plan meals for at least 14 days out.
2. Save meal templates and easily apply them to your meal plan.  
    - No need for quantities (due to the solver).  For example a template could be 4 food items:  chicken, brown rice, avocado, brocolli (quantities would be calculated when template is applied to the specific meal).

**Meal Preperation (& Grocery Shopping)**
1. Auto grocery list prep (and if using custom user generated foods, it can create a list for Costco)


### Unique Value Proposition
---

This app would be unique from other nutrition apps in that it would have the ability to calculate food quantities given a set of target macros, instead of calculating macros given a set of food quantities (which is the current standard practice using MyFitnessPal or a similar app).  

By using this app, a user could in theory achieve an accuracy of 100% in "hitting their macros".  Contrast this with the current user experience of logging food into an app such as MyFitnessPal and **trying** to hit macros by making manual adjustments to food choices and quanities in real time throughout the day, in hopes of "hitting their macros" by the end of the day.

There are several disadvantages to the 'current standard':

1. In order to make manual adjustments in real time, a user must be educated in what foods contain certain ratios of macro nutrients.  Not all users have the knowledge required.
2. Further to the Issue 1, a user must "estimate" before they eat a food how much will be needed to make the necessary adjustment at the end of the day to allow them to "hit their macros", unless they log the foods first into MyFitnessPal, which is time consuming and requires mental effort.
3. Further to Issue 2, even if a user logs their food first, they would have to use a trial and error process of mixing and matching food choices and quantities to make the required adjustment to hit their macros by the end of the day.
4. Other issues?

To my knowledge there isn't an app or even professional grade software designed for licensed nutritionists on the market which does this.

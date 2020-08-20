---
title: Nutrition App
date: 2020-08-20
categories: 
tags: []     # TAG names should always be lowercase
author: Richard Stock
layout: post
permalink: /nutrition_app.md/
---

### What Real World Problem Does this App Solve?
---

This app would be unique from other nutrition apps in that it would have the ability to calculate food quantities given a set of target macros, instead of calculating macros given a set of food quantities (which is the current standard practice using MyFitnessPal or a similar app).  

By using this app, a user could in theory achieve an accuracy of 100% in "hitting their macros".  Contrast this with the current user experience of logging food into an app such as MyFitnessPal and **trying** to hit macros by making manual adjustments to food choices and quanities in real time throughout the day, in hopes of "hitting their macros" by the end of the day.

There are several disadvantages to the 'current standard':

1. In order to make manual adjustments in real time, a user must be educated in what foods contain certain ratios of macro nutrients.  Not all users have the knowledge required.
2. Further to the Issue 1, a user must "estimate" before they eat a food how much will be needed to make the necessary adjustment at the end of the day to allow them to "hit their macros", unless they log the foods first into MyFitnessPal, which is time consuming and requires mental effort.
3. Further to Issue 2, even if a user logs their food first, they would have to use a trial and error process of mixing and matching food choices and quantities to make the required adjustment to hit their macros by the end of the day.
4. Other issues?

To my knowledge there isn't an app or even professional grade software designed for licensed nutritionists on the market which does this.

### Macro Calculation Process
---

1. **Determine Basal Metabolic Rate (BMR)**: there are several formulas out there - Mifflin St-Jeor and newer Oxford ones, do not use Harris Benedict.  Consider averaging MSJ and Oxford.  Units are calories.
2. **Total Daily Energy Expenditure (TDEE)**: Add an exercise multiplier to BMR to obtain TDEE (the amount of calories you burn each day).
3. **Determine Daily Calroie Goal**:  Cut, Maintain, or Bulk.  If cut or bulk, determine how many calories +/- the user wishes to apply per day.  Add or subtract this amount to obtain the Daily Calorie Goal.

(to be continued)




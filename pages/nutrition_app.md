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

   > **Mifflin St Jeor (metric)**:
   >
   > **BMR** = [9.99 * weight (kg)] + [6.25 * height (cm)] – [4.92 * age (years)] + s,
   >
   > where s is: +5 for males, and -161 for females.

   `user input: weight, height, age, gender`

2. **Determine Total Daily Energy Expenditure (TDEE)**: Add an exercise multiplier to BMR to obtain TDEE (the amount of calories you burn each day).

   > **Sedentary** = BMR x 1.2 (little or no exercise, desk job) 
   >
   > **Lightly active** = BMR x 1.375 (light exercise/ sports 1-3 days/week) 
   >
   > **Moderately active** = BMR x 1.55 (moderate exercise/ sports 6-7 days/week) 
   >
   > **Very active** = BMR x 1.725 (hard exercise every day, or exercising 2 xs/day) 
   >
   > **Extra active** = BMR x 1.9 (hard exercise 2 or more times per day, or training for marathon, or triathlon, etc. 

   `user input: activity level (5 choices)`

3. **Determine Daily Calorie Goal**:  Cut, Maintain, or Bulk.  If cut or bulk, determine how many calories +/- the user wishes to apply per day.  Add or subtract this amount to obtain the Daily Calorie Goal.

   > Example:  
   >
   > **Cut (500 calorie defecit per day)**:  Daily Calorie Goal = TDEE - 500
   >
   > **Maintain**:  Daily Calorie Goal = TDEE
   >
   > **Bulk (500 calorie surplus per day)**:  Daily Calorie Goal = TDEE + 500 

   `user input: diet goal (cut, bulk, or maintain)`

4. **Determine Daily Macros**:  based on several factors and constraints, calculate the amount of protein, carbs, and fat to eat each day.  

   > **Constraints**:
   >
   > *Calories*:  |  Protein & Carbs = 4 calories  |  Fat = 9 calories
   >
   > *CCH (Caloric Constraint Hypothesis)*:  All 3 macros must be manipulated together, i.e when one macro is raised or lowered, either one or both of the remaining macros must be also adjusted to keep calories constant.  Thus in assigning macro totals, we need to determine optimal ranges of macros and then adjust macros to both meet caloric constraints AND be within optimal ranges.  Furthermore, there may be scenarios where calories are too low to achieve the minimum value of the optimum range for one or more macronutrients, and trade-offs must be considered (according to macro prioritization  -->  Most Important to Least Important:  1) proteins, 2) carbs, 3) fats).
   >
   > **Factors**
   >
   > User's Fitness Goal:  General Health, Endurance Athlete, Team Sports, Strength and Power Sports
   >
   > User's Diet Goal:   Cut (Hypocaloric), Bulk (Hypercaloric)

   `user input: fitness goal (4 choices)`

   > **Optimal Macro Ranges (listed in units of grams per lb of body weight per day)**
   >
   > General Health:  
   >
   > |         | Minimum | Optimal | Maximum |
   > | ------- | ------- | ------- | ------- |
   > | Protein | 0.3     | 0.7     | 1.5     |
   > | Carbs   | 0.5     |         |         |
   > | Fat     |         |         |         |
   >
   > Endurance Athlete:  
   >
   > |         | Minimum | Optimal | Maximum |
   > | ------- | ------- | ------- | ------- |
   > | Protein | 0.5     | 0.7     | 1.0     |
   > | Carbs   |         |         |         |
   > | Fat     |         |         |         |
   >
   > Team Sports:  
   > 
   > |         | Minimum | Optimal | Maximum |
   > | ------- | ------- | ------- | ------- |
   > | Protein | 0.6     | 0.8     | 1.5     |
   > | Carbs   |         |         |         |
   > | Fat     |         |         |         |
   >
   > Strength and Power Sports:  
   > 
   > |         | Minimum | Optimal | Maximum |
   > | ------- | ------- | ------- | ------- |
   > | Protein | 0.7     | 1.0     | 2.0     |
   > | Carbs   |         |         |         |
   > | Fat     |         |         |         |
   >
   > Hypocaloric Diet (Cut):  
   > 
   > |         | Minimum | Optimal | Maximum |
   > | ------- | ------- | ------- | ------- |
   > | Protein | 0.8     | 1.0     | 1.5     |
   > | Carbs   |         |         |         |
   > | Fat     |         |         |         |
   >
   > Hypercaloric Diet (Bulk):   
   >
   > |         | Minimum | Optimal | Maximum |
   > | ------- | ------- | ------- | ------- |
   > | Protein | 0.7     | 1.0     | 1.5     |
   > | Carbs   |         |         |         |
   > | Fat     |         |         |         |
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

**1. Determine Basal Metabolic Rate (BMR)**: This is the amount of calories you burn to keep your body functioning at absolute resting state (ex: sleeping).  There are several formulas however most accurate are  Mifflin St-Jeor and the newer Henry-Oxford ones, *not* Harris-Benedict.  Consider averaging MSJ and Oxford.  

`user input: 1) weight, 2) height, 3) birthdate, 4) gender`

```mathematica
   Mifflin St Jeor (metric):
   *************************
   BMR = [9.99 * weight (kg)] + [6.25 * height (cm)] – [4.92 * age  (years)] + s, 
   where s = +5 for males, and -161 for females.

   Henry-Oxford (metric):
   *************************
   
   *Males*
   
   | Age   | Formula                         |
   | ----- | ------------------------------- |
   | 0-3   | BMR = 61.0 * weight (kg) - 33.7 |
   | 3-10  | BMR = 23.3 * weight (kg) + 514  |
   | 10-18 | BMR = 18.4 * weight (kg) + 581  |
   | 18-30 | BMR = 16.0 * weight (kg) + 545  |
   | 30-60 | BMR = 14.2 * weight (kg) + 593  |
   | 60+   | BMR = 13.5 * weight (kg) + 514  |
   
   *Females*
  
   | Age   | Formula                         |
   | ----- | ------------------------------- |
   | 0-3   | BMR = 58.9 * weight (kg) - 23.1 |
   | 3-10  | BMR = 20.1 * weight (kg) + 507  |
   | 10-18 | BMR = 11.1 * weight (kg) + 761  |
   | 18-30 | BMR = 13.1 * weight (kg) + 558  |
   | 30-60 | BMR = 9.74 * weight (kg) + 694  |
   | 60+   | BMR = 10.1 * weight (kg) + 569  |
```
   <br/>

**2. Determine Total Daily Energy Expenditure (TDEE)**:  This is the amount of calories you burn each day.  Add an exercise multiplier to BMR to obtain TDEE.

`user input: activity level (5 choices)`

```mathematica
TDEE Equations
**************
1) Sedentary         = BMR x 1.2 (little or no exercise, desk job) 
2) Lightly active    = BMR x 1.375 (light exercise/ sports 1-3 days/week) 
3) Moderately active = BMR x 1.55 (moderate exercise/ sports 6-7 days/week) 
4) Very active       = BMR x 1.725 (hard exercise every day, or exercising 2 xs/day) 
5) Extra active      = BMR x 1.9 (hard exercise 2 or more times per day, or training 
                                  for marathon, or triathlon, etc.)
```

   <br/>

**3. Determine Daily Calorie Goal**:  Cut, Maintain, or Bulk.  If cut or bulk, determine how many calories +/- the user wishes to apply per day.  Add or subtract this amount to obtain the Daily Calorie Goal.

`user input: 1) diet goal (3 choices), 2) daily calorie surplus/defecit goal`

```mathematica
Daily Calorie Goal Equations 
****************************
Cut:      Daily Goal = TDEE - defecit calorie goal
Maintain: Daily Goal = TDEE
Bulk:     Daily Goal = TDEE + surplus calorie goal
```

   <br/>

**4. Determine Daily Macros**:  based on the Caloric Constraint Hypothesis, and the user's Fitness Goal, determine daily macros.  

`user input: fitness goal (4 choices)`

```mathematica
Caloric Constraint Hypothesis:
******************************
Macro-Calorie Conversions:  
Protein = 4 calories  |  Carbs = 4 calories  |  Fat = 9 calories

All 3 macros must be manipulated together, i.e when one macro is raised or lowered, 
either one or both of the remaining macros must be also adjusted to keep calories 
constant.  

Thus in assigning macro totals, we need to determine *optimal ranges* for each macro and 
then adjust macros to both meet caloric constraints AND be within optimal ranges.
Furthermore, there may be scenarios where calories are too low to achieve the minimum 
value of the optimum range for one or more macronutrients, and trade-offs must be 
considered (according to macro prioritization:  
Most Important to Least Important:  1) proteins, 2) carbs, 3) fats).
```

```mathematica
User's Fitness Goal: 
******************** 
1) General Health, 2) Endurance Athlete, 3) Team Sports, 4) Strength and Power Sports
```

<br/>

**Optimal Macro Ranges** (grams per pound of body weight / day)

`General Health`

| Minimum | Minimum | Optimal | Maximum |
| ------- | ------- | ------- | ------- |
| Protein | 0.3     | 0.7     | 1.5     |
| Carbs   | 0.5     | n/a     | 5.0     |
| Fat     | 0.3     | n/a     | n/a     |

`Endurance Athlete`

|         | Minimum | Optimal | Maximum |
| ------- | ------- | ------- | ------- |
| Protein | 0.5     | 0.7     | 1.0     |
| Carbs   | 1.5     | 3.0     | 5.0     |
| Fat     | 0.3     | n/a     | n/a     |

`Team Sports`

|         | Minimum | Optimal | Maximum |
| ------- | ------- | ------- | ------- |
| Protein | 0.6     | 0.8     | 1.5     |
| Carbs   | 1.5     | n/a     | 3.0     |
| Fat     | 0.3     | n/a     | n/a     |

`Strength and Power Sports`

|         | Minimum | Optimal | Maximum |
| ------- | ------- | ------- | ------- |
| Protein | 0.7     | 1.0     | 2.0     |
| Carbs   | 1.0     | 1.5     | 2.5     |
| Fat     | 0.3     | n/a     | n/a     |

`Hypocaloric Diet (Cut)`

|         | Minimum | Optimal | Maximum |
| ------- | ------- | ------- | ------- |
| Protein | 1.0     | n/a     | 1.5     |
| Carbs   | 0.3     | 1.0     | n/a     |
| Fat     | 0.3     | n/a     | n/a     |

`Hypercaloric Diet (Bulk)`

|         | Minimum | Optimal | Maximum |
| ------- | ------- | ------- | ------- |
| Protein | 0.7     | 1.0     | 1.5     |
| Carbs   | 1.0     | n/a     | 5.0     |
| Fat     | 0.3     | n/a     | n/a     |

<br/>

**5. Determine Meal Schedule**:   Different for workout days and for rest days.  User inputs the following parameters, and calculations are performed to create the optimal meal schedule:

`user inputs: 1) wake time, 2) sleep time, 3) workout start time, 4) workout duration (minutes), 5) time between waking and first meal (minutes), 6) time between last meal and sleeping (minutes), 7) # of meals per day (between 4 and 8)`

```mathematica
Meal Schedule Calculations - Case 1 (typical)
*********************************************
1) Calculate time of first meal        = 1 plus 5
2) Calculate time of last meal         = 2 minus 6
3) Calculate time of pre-workout meal  = 3 minus (60 minutes)
4) Calculate time of post-workout meal = 3 plus 4 plus (30 minutes)
5) If more than 4 meals per day, fill in remaining meals:
	 LOOP until all meals are scheduled:
     1) Identify all gaps between scheduled meals
     2) Place meal 5 in middle of largest gap

```

<br/>
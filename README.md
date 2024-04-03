# Large Scale Data Management
Exercises and project for the university course "Large Scale Data Management"

# Practical 1:
## Exercise 1 - Dimensional Fact Model:
Our university would like to define statistics and indicators (KPI) on its level of internationalization. Between all interesting Facts, we focus on "Visiting the University" Fact: doctorands, researchers and professors from other universities spend some time in our university. Use the DFM Schema to model this Fact. The model should be able to let us retrieve statistics on the movement of incoming external personnel and should be able to let us do temporal analysis over their provenance, type of mobility and performed activity, as well as their turor (Hosting Professor) and their information. Storicity: 20 Years.
### Solution:
![es1_e1](https://github.com/edoltl/large-scale-data-management/assets/117369447/67371cb6-5919-49eb-bb26-77ba4697c2cd)
## Exercise 2 - Dimensional Fact Model:
To be noted: this exercise will be the basis for all future practical lessons.
A brand of cinema want to implement a Data Mart for the analysis of ticket sales for its projected movies. Objectives:
- Analysis of daily sales and aggregations for bigger temporal intervals
- Diversificated analysis on each screen of every cinema, to be aggregated for further territorial analysis
- Analysis based on the characteristics of each projected film (actors, productors, distributors, globally sales performances, directors...)
- Analysis on the chosen modes of programmation and projection (timetable, intervals, 3D, language...)
- Analysis on sales channels (online, physical,...)
- Analysis on sales to gain a better understanding of the best programmation and projection metodologies

Fact: ticket sales

Dimension: screen, show, movie, sale channel, sale date

Measures:
- Amount of takings
- Quantity of sold tickets
### Solution:
![es1_e2](https://github.com/edoltl/large-scale-data-management/assets/117369447/dfe99e93-34c2-4bc8-b1f8-8578f53eba61)

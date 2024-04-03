# Large Scale Data Management
Exercises for the university course "Large Scale Data Management"

# Practical 1:
## Exercise 1 - Dimensional Fact Model:
Our university would like to define statistics and indicators (KPI) on its level of internationalization. Between all interesting Facts, we focus on "Visiting the University" Fact: doctorands, researchers and professors from other universities spend some time in our university. Use the DFM Schema to model this Fact. The model should be able to let us retrieve statistics on the movement of incoming external personnel and should be able to let us do temporal analysis over their provenance, type of mobility and performed activity, as well as their turor (Hosting Professor) and their information. 

Storicity: 20 Years.

Measures: count.
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
# Practical 2: Star-Schema
A Star-Schema is a logical implementation of a Datawarehouse (or an individual Data Mart). We use the ROLAP Star-Schema, similar to the relational model. Here are some examples:

![star schema](https://github.com/edoltl/large-scale-data-management/assets/117369447/aaa6bab4-5cd8-421e-b468-d3330a7ee6d7)
![star schema2](https://github.com/edoltl/large-scale-data-management/assets/117369447/108bdbb8-d2a0-436a-a55f-0de3f0412f75)
![queryOlap](https://github.com/edoltl/large-scale-data-management/assets/117369447/b6dc13dd-23d3-4247-8ddb-0dd69d35608f)
![junkdim](https://github.com/edoltl/large-scale-data-management/assets/117369447/2569c155-6c70-4791-af61-89da1f9d244c)
![gerarchiacondivisa](https://github.com/edoltl/large-scale-data-management/assets/117369447/c182ca29-dfd6-4f18-8a6c-d872fa66f380)
![attr cross dim](https://github.com/edoltl/large-scale-data-management/assets/117369447/1a687bc2-9a1b-4c5b-b99d-67421675366e)
![attr cross dim2](https://github.com/edoltl/large-scale-data-management/assets/117369447/35a5eb49-37d8-4720-b544-25f33c7da357)

## Exercise 1 - From DFM To Star-Schema:
![es2_e1-dfm](https://github.com/edoltl/large-scale-data-management/assets/117369447/c39c999e-0ca1-4275-9f0d-48f50b2720c6)
### Solution:
![es2_es1](https://github.com/edoltl/large-scale-data-management/assets/117369447/8f3e7051-a346-49ae-88ca-9ae01e90a60a)

To be noted1: Programma di Mobility (Mobilitation Program), Ruolo (Role), Attività Svolta (performed activity) can be considered Junk Dimension, hence one can model one new table out of these junks.

To be noted2: In this example the date is a natural key. OLAP usuallly works with surrogated keys, but it is also usually preferred to maintain dates as natural keys because in this way you don't have to run a JOIN to get the date, already embedded in the Fact Table.
## Exercise 2 - Queries on Exercise 1:
- Compute the mean index of satisfaction of visitors arrived between the academic year 2011-12 and the academic year 2013-14
- Compute the total cost for students arrived from european countries in the last 5 years
- Select the top 3 professors (id, name, surname) from the Science Department
who worked the most as tutors for incoming personnel
- Compute the number of visitors in order of sex in the last 10 years
### Solution:

java c
Problem 1 
Solve the following LP using the Simplex method as described in class:
max    3x1  + x2  + 3x3
s.t.      2x1 + x2  + x3  ≤ 2
x1 + 2x2  + 3x3  ≤ 5
2x1 + 2x2  + x3  ≤ 6
x ≥ 0When it comes to choosing the variable to enter/leave the basis, always select the first eligible variable. Use the origin as your starting point. Verify your solution with GAMS/Pyomo (please submit your source code file as well).
Problem 2 
An oil tanker has three compartments for storing cargo: front, center, and back. These compartments have capacity limits on both weight and space:
Compartment        Weight capacity (tons)            Space capacity (cubic feet)
Front                              12                                               7,000
Center                            18                                                9,000
Back                                10                                                 5,000Furthermore, the weight of the cargo in the respective compartments must be the same proportion of that compartment's weight capacity to maintain the balance of the tanker. The following four cargos have been offered for shipment on an upcoming trip as space is available:
Cargo 
Weight (tons) 
Volume (cubic feet/ton) Profit ($/ton) 
1 
20 
500 
320 
2 
16 
700 
400 
3 
25 
600 
360 
4 
13 
400 
290 Please note that the “Weight” column represents the availability of cargos. Any portion of these cargos can be accepted.  The objective is to determine how much (if any) of each cargo should be accepted and how to distribute each among the compartments to maximize the total profit for the trip.
a)   Formulate this problem as an LP. Clearly state your notation for all given parameters (e.g., use wj to denote the weight capacity of compartment j ) and present the model in condensed mathematical form.
b)  Solve it with GAMS/Pyomo. (please submit your source code file as well).
Hints:
•    Define doubly indexed variables.
Problem 3 
max 2x1 + 3x2
s.t. x1  + x2  ≤ 4
x1  + 2x2  ≤ 6
x1  ≥ 0, x2  ≥ 0
a)   Plot the contours of the objective and the feasible region and use the contours to determine the optimal solution on the plot by inspection and report the value.
b)  Determine the optimum by inspection.
c)   Solve the above problem using the simplex algorithm.
d)  Verify your solution with GAMS/Pyomo (please also submit your source code file).
e)   Construct the dual and solve the dual problem with GAMS/Pyomo (please also submit your source code file).
Problem 4 
Consider the following optimization problem:
min       |x1|  + 2|x2|  + |x3|
st         x + x − x ≤ 10
x1 − 3x2  + 2x3  = 12
x ∈ R3
(a) Can you conver代 写Mathematical modelingR
代做程序编程语言t this problem into a linear program? If so, please present the linear program in the standard form.[Note: This is a bonus problem and not required – those students may work on it to earn an extra credit of at most 2 points that will be used to offset any possible loss of points from other problems, which are worth 10 points in total.](b) Is the transformation in (a) still valid if the objective function coefficient of the last term in the objective is changed to -1 (i.e. changing the objective to min x1  + 2x2  − x3  )? Please first solve it with GAMS using solver BARON and problem type ‘DNLP ’ (please submit your source code file through Canvas; if you use Pyomo, you may use the solver “Couenne” instead. Next, you might  try  the  transformation  in  (a)  to  formulate  a  linear  program  and  solve  this  LP  with GAMS/Pyomo. After obtaining solutions for both cases, you can compare the solutions and comment on the suitability of the transformation.
Hints:
•    Please check the Expanded GAMS Guide (McCarl) for the type of problem called 'DNLP'
•    To use BARON, please add the following two lines to the beginning of your GAMS file:
option dnlp = baron;
option ptcr = 0;The first line asks GAMS to solve a DNLP with BARON solver, and the second line sets the optimality gap of BARON to zero. In addition to adding these two lines, in the ‘solve’ statement please make sure to declare the model as a ‘DNLP’ .
Problem 5 Consider a farmer who grows wheat, corn, and sugar beets on his 500 acres of land. In the winter, he wants to decide how much land to devote to each crop. The costs of planting wheat, corn and sugar beets are $150/acre, $230/acre, and $260/acre, respectively.The farmer knows that at least 200 tons of wheat and 240 tons of corn are needed for cattle feed. These amounts can be raised on the farm or bought from a wholesaler. Any production in excess of the feeding requirement would be sold, at the selling prices of $170 and $150 per ton of wheat and corn, respectively. The purchase prices  are 40% more than the  selling price due to the wholesaler’s margin and transportation costs.Another profitable crop is sugar beet, which he expects to sell at $36/ton; however, the European Commission imposes a quota on sugar beet production. Any amount in excess of the quota can be sold only at $10/ton. The farmer’s quota for next year is 6000 ton. Based on past experience, the farmer knows that the mean yield on his land is roughly 2.5 ton, 3 ton, and 20 ton per acre for wheat, corn, and sugar beets, respectively.
Please formulate this problem as an LP. Clearly state your notation for all given parameters and solve it with GAMS/Pyomo (please also submit your source code file).







         
加QQ：99515681  WX：codinghelp

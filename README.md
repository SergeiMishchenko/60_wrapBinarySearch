# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

What is meant by y = log2x?
y is the exponent such that if 2 were raised to the y power, the result would equal x.

What does the graph look like?
The graph looks like the equation y = 2^x flipped over the line y = x. The slope the of y = log2x is constantly decreasing.

Recursive Solution:
0. Problem: find the index of a given element in a list.
1. Recursive Abstraction: when asked to return the index of a given element in a list,
                          the recursive abstraction can return the index of a certain element 
						  in the next smaller portion of the list.
2. Base Case: decsion: is low > hi?
   Base Case Solution: If yes, return -1. Instructions to Solve the Recursive Case: Leftover Processing: Result of Recursive Abstraction: 
   Instructions to Solve the Recursive Case: Otherwise, compare the desired value to the element at the current index.
		Leftover Processing: if the comparison returns 0, return the index. 
		Result of Recursive Abstraction: if the comparison returns an int greater than 0, return the index of the element in the interval from current index +1 to hi.
		Result of Recursive Abstraction: If the comparison returns an int less than 0, return the index of the element in the interval from low to current index - 1
		Leftover Processsing: n/a
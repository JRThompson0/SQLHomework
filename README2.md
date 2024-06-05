##### Inner Join

Makes new rows composed of the entirety or part of the old rows. Only returns data when there's a match.

##### Outer Left/Right Join

Returns all rows from the Left or Right table, with any matched data appended to the other side. Will return values
from entries on the dominant side even if they have no matched values from the other table, in which case they will 
have null values.

##### Full Outer Join

Returns all rows, with any matched data appended and unmatched data having null appended to it.

##### Cross Join

Returns all rows from one table, matched with all rows from the other table. Will give a tableSize1*tableSize2 
sized table, so often big.



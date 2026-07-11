# Designing a Navigation App like Google Maps

Solution :
It's advisable to use a Graph instead of a Tree.

In a navigation system :
Cities or intersections are represented as vertices (nodes). Roads connecting them are represented as edges. Each road can have a weight, such as a distance, travel time or traffic delay.

A tree is not suitable because a tree has only one unique path between any 2 nodes, but road networks have multiple paths between any 2 nodes. Moreover, trees cannot contain cycles, but road networks often do.
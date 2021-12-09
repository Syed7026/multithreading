Project Single Source Shortest path Using multithreading

The algorithm maintains an adjacencyList for each node,
activeNodeCostTupleList and minNodeCostMap

b. For each nodeCostTuple from activeNodeCostTuple list, we will be check if its cost is lest than the available cost in minNodeCostMap and will update the values and will push its adjacent in the activeNodeCostTupleList with updated cost.

c. Since step(b) is performed by all the activeNodes and all nodes updates the same minNodeCostMap, this can be taken up by an independent thread.

d. We will implement a multi-threading algorithm where no_of_threads &lt;= no_of_cores and each thread will perform step(b) and updates the shared
variables i.e; activeNodeCostTupleList &amp; minNodeCostMap with proper access to it.

e. The final minNodeCostMap will give us the minNodeCostMap from the
given source node

4. a. For testing the processing time, we are using clock for calculating
startTime, endTime which will give the execution time (endTime –
startTime).

b. For testing the correctness of the output, we are currently checking with
the online/manually generated test cases'.

c. We will be calculating the number of traversals made by keeping the
count of number of active nodes traversed by the algorithm

We have to provide the nodes and edges for the code to run and by specifying the start node.
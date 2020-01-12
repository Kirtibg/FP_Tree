# FP_Tree
Basic python code to make a frequent pattern tree (FP-tree) from data containing transactions from a grocery store.

FP-Tree is constructed using 2 passes over the data-set:
Pass 1:
Scan data and find support for each item.
Discard infrequent items.
Sort frequent items in decreasing order based on their support.
Use this order when building the FP-Tree, so common prefixes can be shared.
Pass 2:
Nodes correspond to items and have a counter
FP-Growth reads 1 transaction at a time and maps it to a path
Fixed order is used, so paths can overlap when transactions share items (when they have the same prefix).
 In this case, counters are incremented
 Pointers are maintained between nodes containing the same item, creating singly linked lists (dotted lines)
The more paths that overlap, the higher the compression. FP-tree may fit in memory.
Frequent itemsets extracted from the FP-Tree.

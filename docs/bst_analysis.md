# Binary Search Tree Analysis Laboratory

## Core goal
Students must implement a binary search tree storing integer values and supporting insertion, search, removal, height, traversal, and balancing checks.

## Analysis expectations
Students should explain:

- average-case and worst-case complexity of insertion, search, and deletion; All these operations will be O(log n) average case and O(n) worst case. Read below.
- how tree shape affects cost; A balanced, complete, and full tree will give us the best results in terms of costs. A skewed tree or a chain acts as a linked list, which makes some operations lose their logarithmic time. 
- why balanced trees improve performance; Balanced trees guarantee the condition that the left subtree will always be smaller than the parent, and the right subtree will always be greater than the parent. Therefore, we can achieve logarithmic instead of linear time by eliminating half of the list each iteration.
- traversal behavior and the ordering guarantees of different traversals; 
Inorder: left, node, right | Preorder: node, left, right | Postorder: left, right, node | Level-order: level by level
- what happens when the tree becomes skewed. When trees become skewed, they cause a linked-list-like behavior, making search, insert, and delete O(n) rather than O(log n).

## Big-O focus
Students should describe Big-O for:

- insert: The Big-O time complexity in the average case would be O(log n) since the balanced characteristic allows for half of the tree to be skipped each iteration. In the worst case of a skewed list, which becomes like a chain or linked list, the worst case will be O(n).
- search: The average time complexity would be O(log n) since the search invariant makes it so that half of the list is eliminated or cut off each iteration, making it better than a linear search. The worst case time complexity would once again be in a structure such as a skewed list, which then requires almost full linear search of O(n).
- remove: To remove a value, the average time complexity is O(log n) due to the balanced characteristic. In the worst case of a chain-like structure and the goal of removing the last element, full traversal would once again be linear O(n).
- min/max traversal: Unlike a linear traversal, to find the minimum value, we only need to find the leftmost child of the leftmost subtree, and vice versa with the maximum. In the best case of a skewed tree, the time complexity may become O(1) if the min/max is at the root, but if the structure becomes chain-like, the worst case becomes O(n).
- height: The average and worst-case will both be linear O(n), since a whole traversal is required to find the height.
- inorder/preorder/postorder: All elements will be traversed through, no matter the formation, giving linear O(n).
- level-order traversal: All elements will be traversed through, no matter the formation, giving linear O(n).

A rigorous answer should include both average and worst-case behavior.

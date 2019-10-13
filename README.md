# binary_tree.pl

## Implementation
### __emptyBT()__
This predicate is simple. If the tree is empty, then the only value it will have is nil.
### __bTree(N, T1, T2)__
This predicate checks if N is the root of T1 and T2. Both the the left subtree and the right
subtree are checked by calling checkbig(N, Right) and checksmall(N, Left). These ensure all
the nodes on the left are smaller and all the nodes on the right are bigger. It does this
recursively by calling bTree().
### __insert(I, T1, T2)__
The trees are put through this predicate recursively, until the base case is reached. The
location where I would be located is found. T1 should be nil at this point, at T2 should have
the node I with no subtrees. If these are both not true once it has reached this base case
then the program fails.
### __preorder(T, L)__
This is when the root is visited, then the left child, then the right child. This predicate
recursively appends each node to an empty list in this order. Returns true if the list matches
the one given in the argument.
### __inorder(T, L)__
This is when the left child is visited, then the root, then the child. The predicate functions in
the same manner as preorder(T, L).
### __postorder(T, L)__
This is when the left child is visited, then the right, then the root. The predicate functions in
the same manner as preorder(T, L) and inorder(T, L).
### __search(T, I)__
This recursively travels down either the left subtree or right subtree until the base case is
reached and the node matches I or it does not. Returns true if it does and false if it does not.
### __height(T, H)__
The base case here is defined as a nil tree having a height of 0. The left and right subtrees
are recursively traversed through, adding one to the height each time until the height is
found.
# CPP MODULE 8 :

# 8a :

# PROGRAM STATEMENT :
Fix the bugs in a given C++ main function to perform inorder,preorder and postorder traversal

# ALGORITHM :
1. Create a binary tree with nodes, initializing the root and its left and right children.
2. Perform an inorder traversal of the tree (left, root, right), printing the nodes.
3. Perform a preorder traversal of the tree (root, left, right), printing the nodes.
4. Perform a postorder traversal of the tree (left, right, root), printing the nodes.
5. Print the output for each of the traversal methods (inorder, preorder, postorder).

# PROGRAM :
NAME : V>Kasivishvanath
REG NO : 212222040073
```
int main()
{
 struct Node* root = new Node('A');
 root->left = new Node('B');
 root->right = new Node('E');
 root->left->left = new Node('C');
 root->left->left->left = new Node('G');
 root->left->right = new Node('D');
 root->right->left = new Node('F');
 
 cout << "Inorder traversal ";
 inorderTraversal(root);
 cout << "\nPreorder traversal ";
 preorderTraversal(root);
 cout << "\nPostorder traversal ";
 postorderTraversal(root);
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/58cada7c-2c92-436a-a696-d943cd002e2a)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 8b :

# PROGRAM STATEMENT :
Fix the bugs in a given C++ function to find the sum of k smallest elements in BST.

# ALGORITHM :
1. Initialize a counter variable count to 0 to keep track of the number of elements processed.
2. Call the recursive function ksmallestElementSumRec with the root of the tree, value of k, and count
3. In the recursive function, if the current node is NULL, return the count to stop further recursion.
4. If the node exists, recursively call the left subtree, process the current node (incrementing the count), 
and then call the right subtree.
5. Return the value of count after processing the k smallest elements.

# PROGRAM :
```
int ksmallestElementSum(struct Node *root, int k)
{
 int count = 0;
 count=ksmallestElementSumRec(root, k, count);
 return count;
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/83b99617-c58f-4e61-89b0-feb4a775646c)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 8c :

# PROGRAM STATEMENT :
Construct an Expression Tree from an infix expression for the given expression tree and 
evaluate the expression
Input : Prefix : /*+314+-952 Output: 2.66667

# ALGORITHM :
1. Begin a loop that iterates from the last character of the expression string eqn to the first one.
2. In each iteration, access the current character in the equation
3. Call the insert function with the current character from the equation string to insert it into the tree..
4. Continue the loop until all characters in the equation string are processed in reverse order.
5. After the loop finishes, the tree will have been constructed based on the provided expression.
   
# PROGRAM :
```
void buildTree(string eqn)
 {
 for (int i = eqn.length() - 1; i >= 0; i--)
 insert(eqn[i]);
 }
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/ad2b7ce7-2830-4e60-bae6-03d3aa7e294c)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 8d :

# PROGRAM STATEMENT :
Correct the C++ code to insert the following elements in an AVL Tree.
12 4 3 7

# ALGORITHM :
1. Insert the key as in a regular Binary Search Tree (BST).
2. Update the height of the current node.
3. Calculate the balance factor (left subtree height - right subtree height).
4. Perform rotations (right, left, left-right, or right-left) if the balance factor is greater than 1 or less than 
-1.
5. Return the updated node after balancing.

# PROGRAM :
```
Node* insert(Node* node, int key)
{
if (node == NULL)
return(newNode(key));
if (key < node->key)
node->left = insert(node->left, key);
else if (key > node->key)
node->right = insert(node->right, key);
else
return node;
node->height = 1 + max(height(node->left),
height(node->right));
int balance = getBalance(node);
if (balance > 1 && key < node->left->key)
return rightRotate(node);
if (balance < -1 && key > node->right->key)
return leftRotate(node);
if (balance > 1 && key > node->left->key)
{
node->left = leftRotate(node->left);
return rightRotate(node);
}
if (balance < -1 && key < node->right->key)
{
node->right = rightRotate(node->right);
return leftRotate(node);
}
return node;
}
```

# OUTPUT :
 ![image](https://github.com/user-attachments/assets/562ebb86-0854-4526-80fe-fa9d2370cc82)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

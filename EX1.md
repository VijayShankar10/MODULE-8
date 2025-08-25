# Ex.No:1  
# Ex.Name: Find the Largest Value in a Binary Search Tree  

## Date:  

## Aim:  
To write a C++ program with a **main function** to find the largest value in a **Binary Search Tree (BST)**.  

## Algorithm:  
1. Start the program.  
2. Define a `Node` structure with:  
   - `data` (integer)  
   - `left` and `right` pointers.  
3. Create a function `newNode(int val)` to allocate a new node with the given value.  
4. Create an `insert(Node* root, int val)` function to insert values into the BST:  
   - If the tree is empty, create a new node.  
   - If `val < root->data`, insert into the left subtree.  
   - Else insert into the right subtree.  
5. Create a function `findMax(Node* root)` to find the largest value:  
   - Traverse right until `root->right == NULL`.  
   - Return the node’s data.  
6. In `main()`:  
   - Read number of nodes and their values.  
   - Build the BST using `insert()`.  
   - Call `findMax(root)` and display the result.  
7. Stop the program.  

## Program:
```cpp
int findMax(Node* root)
{
    
    if (root == NULL)
        return INT_MIN;
 
    
    int res = root->data;
    int lres = findMax(root->left);
    int rres = findMax(root->right);
    if (lres > res)
        res = lres;
    if (rres > res)
        res = rres;
    return res;
}
```
## Output:
```
Input:
3
12 4 7

Output:
12
```
## Result:
<img width="867" height="334" alt="image" src="https://github.com/user-attachments/assets/422e91f4-e7f0-4b2c-a745-d3ffff7eabc5" />


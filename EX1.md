# Ex.No:4  
# Ex.Name: Tree Traversals – Inorder, Preorder and Postorder  

## Date:  

## Aim:  
To write a C++ main function to perform **inorder, preorder, and postorder** traversal of a binary tree.  
<img width="810" height="515" alt="image" src="https://github.com/user-attachments/assets/a1cbdaef-15c0-491a-94d5-1d5738e883e4" />


## Algorithm:  
1. Start the program.  
2. Define a binary tree node structure with `data`, `left`, and `right`.  
3. Read the tree edges (parent, child, direction l/r).  
4. Construct the binary tree accordingly.  
5. Define recursive functions for:  
   - **Preorder traversal**: Visit root → left → right  
   - **Inorder traversal**: Visit left → root → right  
   - **Postorder traversal**: Visit left → right → root  
6. Call these functions and display the traversals.  
7. Stop the program.  

## Program:
```cpp
int main()
{
struct node *root=NULL;
int n;


cin>>n;
while(n--)
{
char lr;
char n1,n2;
cin>>n1>>n2;
cin>>lr;
if(root==NULL)
{
root=newNode(n1);
switch(lr)
{
case 'l' :root -> left=newNode(n2);
break;
case 'r' :root -> right=newNode(n2);
break;
}
}
else
{
insert_node(root,n1,n2,lr);
}

}
cout<<"preorder traversal: ";
traversePreOrder(root);
cout<<"\nInorder traversal: ";
traverseInOrder(root);
cout<<"\nPostorder traversal: ";
traversePostOrder(root);
}
```
## Output:
```
Input:
6
A B l
A E r
B C l
B D r
C G l
E F l

Output:
preorder traversal: A B C G D E F
Inorder traversal: G C B D A F E
Postorder traversal: G C D B F E A
```
## Result:
<img width="858" height="905" alt="image" src="https://github.com/user-attachments/assets/b7993b9e-312b-43c3-b8ef-ff3969103b46" />


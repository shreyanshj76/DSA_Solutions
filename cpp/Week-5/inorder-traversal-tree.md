# Program to perform Inorder Traversal of a Binary Tree

Solution (Using Recursion) :
```c++
#include <iostream>
using namespace std;

// Definition of a binary tree node
struct Node {
    int data;
    Node* left;
    Node* right;

    Node(int value) {
        data = value;
        left = right = NULL;
    }
};

// Function for Inorder Traversal
void inorder(Node* root) {
    // Base case
    if (root == NULL)
        return;

    // Visit left subtree
    inorder(root->left);

    // Visit root
    cout << root->data << " ";

    // Visit right subtree
    inorder(root->right);
}

int main() {

    Node* root = new Node(1);
    root->left = new Node(2);
    root->right = new Node(3);
    root->left->left = new Node(4);
    root->left->right = new Node(5);

    cout << "Inorder Traversal: ";
    inorder(root);

    return 0;
}
```
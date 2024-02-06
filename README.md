# Implementation-of-File-System
Implementation of a file system through binary search trees. The goal of the homework was to understand binary trees as a data structure.

The program creates a structure based on binary search trees. At the beginning, we initialize the root directory "root". The role of the 'inst' variable is to filter the given commands and apply the appropriate functions to them. When we receive the "touch" command, we create a cell of type "File". We use the two search functions to check if there is already a file/directory with the requested name. The "mkdir" command works on the same principle as the previous function. The "ls" command displays the directory and file trees in the current directory based on the SRD (in-order) traversal of the tree. The "rm" and "rmdir" commands handle the three cases of deleting a file/directory, namely: deleting a leaf, deleting a node from the middle of the structure, and deleting the root. The working principle for the last two cases is to swap the information in the current node with the minimum from the right subtree. After swapping, the tree is traversed recursively, reaching the old value of the minimum from the right subtree, which is then removed as a leaf. The "cd" command checks if the next input is ".." and sets root=root->parent. Otherwise, it searches for the inserted name and, if found, moves to that directory. The "pwd" command goes up to the root "root" and displays the path back to the current directory. This is achieved through recursion. The "find" command with "-f" / "-d" searches the entire structure until it reaches a file/directory with the requested name. This is accomplished through recursion, treating all eight cases for the "root->left", "root->right", and "root->directories" parameters.

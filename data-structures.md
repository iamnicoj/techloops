# Data Structures 
:joy:
## Hash Table
### Array with linked list
* Hash method
* Map hash to index
* Save index in the node
* Add Items to Linked List
### Balanced Binary Search Tree
* Less Space
* Iterate thorugh the keys

## Array List and Resizable Arrays
Reads: O(1) 
Writes: O(1) and O(n) every n 

## String builder
* Implements a resizable array to concatenate a list of string avoiding manual concatenation of O(n^2)

## Linked Lists
* Implement different flavors including double linked and insert, delete, read, update
* double runner and recursive options

## Stacks 
`pop()` removes the top

`push(item)` add to the top

`peek()` returns the top 

`isEmpty()`

* Some recursive algorithms require temporary going down and then use it whem backtracking. 
* can help implementing recursive algorithms iteratively

## Queues

`add(item)`

`remove()`

`peek()`

`isEmpty()`


## Trees
* Trees vs. Binary
* binary vs binary search
  * complete = every level is full except the rightmost element on the last level
  * Full B = 0 or 2 childern
  * perfect B = full and complete. exactly 2^levels - 1 nodes
* balanced binary tree

### Transversals
* In-Order = left -> node -> right
* Pre-Order = node -> left -> right
* Post-Order = left -> right -> node

## Binary Heaps (Min/Max)
* complete binary tree where each node is smaller tha its children
* the root is the minimum element of the tree

`insert(item)`
`removeroot()`

## Tries (Prefix tree)
* n-ary tree
* each store characters
* each path down represent a word
* null nodes also called > terminatingTrieNode denotes a complete path
* each node can have ALPHABET_SIZE + 1 children
* specialized in prefix 
* [SO topic](https://stackoverflow.com/questions/22183005/whats-the-size-of-a-prefix-tree-trie-that-contains-all-the-english-words)

## Graphs
* directd (one way) or undirected (two way)
* can have isolated subgraphs or be a connected graph
* adjacency list 
  * keep a collection with the adjacency list
  * type node with node[] children
* adjacency matrices - n X n bit matrix

### Graph search - DFS Depth First Search
* visits all deeper branches of a node before visiting next its next branches
* prefered way to touch all nodes

``` java
void search(Node root){
  if (root == null) return;
  visit(root);
  node.marked = true;

  for each (Node node in root.adjacense){
      if (!node.marked){
          visit(node);
          search(node);
      }
  }
}
```

### Graph search - BFS Breath First Search
* visits all neighbors before going to its deeper branches
* uses a Queue
* prefered way to find shortest path from two nodes

``` java
void search(Node root){
    if (root != null) return;
    
    Queue queue = new Queue();
    queue.add(root);
    root.marked = true;

    while(!queue.isEmpty){
        Node node = queue.remove()
        visit(node);
        for neighborh (Node n in node.adjacent){
            if(!neighbor.marked)
                queue.add(neighborh)
                neighbor.marked = true;
        }
    }
}
```

* Bi-directional Seach triggers two searches to try to find a common intersection btw to nodes. From O(adjacent^level) to O adjacent^level/2) 
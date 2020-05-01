# Lists

- A list is a collection of ordered elements that are used to store list of items. Unlike array lists, these can expand and shrink dynamically.

- Lists also be used as a base for other data structures, such as stack and queue. Lists can be used to store lists of users, car parts, ingredients, to-do items, and various other such elements.Lists are the most commonly used linear data structures. These were introduced in the lisp programming language. In this chapter, linked list and doubly linked list are the lists we will cover in the Go language.

- Let's discuss the operations related to add, update, remove, and lookup on linked list and doubly linked list in the following section.

   - LinkedList

      - LinkedList is a sequence of nodes that have properties and a reference to the next node in the sequence. It is a linear data structure that is used to store data. The data structure permits the addition and deletion of components from any node next to another node. They are not stored contiguously in memory, which makes them different arrays.

      -  The following sections will look at the structures and methods in a linked list.
    - The Node class

        - The Node class has an integer typed variable with the name property. The class has another variable with the name nextNode, which is a node pointer. Linked list will have a set of nodes with integer properties, as follows:

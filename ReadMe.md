|Shelton Thomas|
|----|
|s198053|
|Code Design and Data Structures|
|Asteroid Survival Game|

## I. Requirements

1. Description of Problem
    - **Name**: Code Design and Data Structures

    - **Problem Statement**: Create a double-linked list, binary tree, and hash function.

    - **Problem Specifications**: Successful creation of a project that emplements and demonstrated a double-linked list, binary tree, and a hash function.

## II. Design

1. Object Information:

    **Name**: Double-Linked List:

    **File**: Iterator.h

    Description: Templated class used to iterate through nodes.

    **Overloads**:

        Operator: ++
            Description: Used to get the next node for the iterator to move to.

        Operator: --
            Description: Used to get the previous node for the iterator to move to.

        Operator: *
            Description: Used to get the current node's information that is in the iterator.

        Operator: ==
            Description: Used to compare the current node's information with the information from another iterator.

        Operator: !=
            Description: Used to compare the current node's information with the information from another iterator.

    **Attributes**:

        Name: currentNode
            Description: Used to keep track of where the iterator is in the linked list.
            Type: Node*
            Visibility: private

        Name: Iterator
            Description: Constructor for the Iterator class.

        Name: ~Iterator
            Description: Deconstructor for the Iterator class.

    **File**: List.h

    Description: Used as a templated base class for the UnorderedList class.

    **Attributes**:

        Name: mCount
            Description: Used to keep track of the amount of nodes in a list.
            Type: int
            Visibility: protected

        Name: m_last
            Description: Used to keep track of the last item in the list.
            Type: Node*
            Visibility: protected

        Name: m_first
            Description: Used to keep track of the first item in the list.
            Type: Node*
            Visibility: protected

        Name: initializeList
            Description: Used to initialize a list.
            Type: void
            Visibility: public

        Name: isListEmpty
            Description: Used to see if the list is empty.
            Type: bool
            Visibility: public

        Name: length
            Description: Used to get the length of the list.
            Type: int
            Visibility: public

        Name: search
            Description: Used to search for the information sent in the list.
            Type: virtual bool
            Visibility: public
            Params: const T&

        Name: insertFirst
            Description: Used to insert an item in the list putting it at the first position.
            Type: virtual void
            Visibility: public
            Params: const T&

        Name: insertFirst
            Description: Used to insert an item in the list putting it at the last position.
            Type: virtual bool
            Visibility: public
            Params: const T&

        Name: deleteNode
            Description: Used to delete a node in the list.
            Type: virtual bool
            Visibility: public
            Params: const T&

        Name: begin
            Description: Used to set an iterator to the first item in a list.
            Type: Iterator
            Visibility: public

        Name: end
            Description: Used to set an iterator to the last item in a list.
            Type: Iterator
            Visibility: public

        Name: List
            Description: Constructor for the iterator class.
            Visibility: public

        Name: ~List
            Description: Deconstructor for the iterator class.
            Visibility: public

        Name: copyList
            Description: Copies a list to the cureent list.
            Type: void
            Visibility: private
            Params: List&

    **File**: Node.h

    Description: Templeetated class for setting up nodes.

    **Attributes**:

        Name: info
            Description: Holds the information of the node.
            Visibility: public

        Name: next
            Description: Used to store the next node in a list.
            Type: Node*
            Visibility: public

        Name: previous
            Description: Used to store the previous node in a list.
            Type: Node*
            Visibility: public

        Name: Node
            Description: Constructor for the Node class.

    **File**: UnorderedList.h

    Description: Used for holding the nodes and making the list.

    **Attributes**:

        Name: search
            Description: Used to search for a node.
            Type: bool
            Visibility: public
            Params: const T&

        Name: insertFirst
            Description: Used to insert a node in the first position of the list.
            Type: void
            Visibility: public
            Params: const T&

        Name: insertLast
            Description: Used to insert a node in the last position of the list.
            Type: void
            Visibility: public
            Params: const T&

        Name: deleteNode
            Description: Used to delete a node from the list.
            Type: void
            Visibility: public
            Params: const T&

        Name: clear
            Description: Used to clear a list.
            Type: void
            Visibility: public

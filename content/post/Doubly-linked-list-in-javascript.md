+++
title = "How to reverse a doubly linked list in JavaScript"
description = "How to reverse a doubly linked list in JavaScript "
date = 2020-01-30
author = "Jonathan Greene"

+++## Introduction

Welcome my name is Jonathan Greene I am Full Stack Developer that focuses on building clean easily scalable code to get a better ROI on for my clients.

## Step 1. Creating a plan

The first step that needs to be taken is to analyze the goal and come up with a plan to complete it. Below you will find the exact question that was being asked.

```
You’re given the pointer to the head node of a doubly linked list.
Reverse the order of the nodes in the list.
The head node might be NULL to indicate that the list is empty.
Change the next and prev pointers of all the nodes so that the direction of the list is reversed.
Return a reference to the head node of the reversed list.
```

After doing this you can go ahead and start building out your logic.

looking at the code editor we can see the node consists of 3 attributes a data, next, and prev

We start by seeing we are going to need a way to initialize the variables for the current node.

Then we need to setup a variable to hold the temp value as we switch around the prev and next nodes.

After that we need to loop over the nodes looking for a null which will indicate the list has hit an end.

Last we need to just return the head after the entire list has been gone through

### Step 2. Write out the pseudo code

Next we can go ahead and start writing our code. We can start with pseudo code like below

```

// Complete the reverse function below.

/*
 * For your reference:
 *
 * DoublyLinkedListNode {
 *     int data;
 *     DoublyLinkedListNode next;
 *     DoublyLinkedListNode prev;
 * }
 *
 */
function reverse(head) {

    // head is the first node in the list

    // current = 1

    while (current) {
        // swap the previous and next for each node.
        // 5 equals null
        // null equals 5

        // head equals 2
        // current  = 5
    }
    return head;


}

function main() {
```

### Step 3. write the real code

Go through the pseudo code and fill in the logic with whatever language you have chosen.

```

// Complete the reverse function below.

/*
 * For your reference:
 *
 * DoublyLinkedListNode {
 *     int data;
 *     DoublyLinkedListNode next;
 *     DoublyLinkedListNode prev;
 * }
 *
 */
function reverse(head) {

    // head is the first node in the list

    let current = head; // current = 1

    while (current) {
        let true_next = current.next;
        // swap the previous and next for each node.
        current.next = current.prev; // 5 equals null
        current.prev = true_next; // null equals 5

        head = current; // head equals 2
        current = true_next; // current  = 5
    }
    return head;


}

function main() {
```

### Step 4. Test the output

Last just go ahead and paste your solution in Hacker Rank problem found below

[https://www.hackerrank.com/challenges/reverse-a-doubly-linked-list/problem?h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=linked-lists](https://www.hackerrank.com/challenges/reverse-a-doubly-linked-list/problem?h_l=interview&playlist_slugs[]=interview-preparation-kit&playlist_slugs[]=linked-lists)

#### Thank you for reading

I hope this blog helps you to better understand and solve reversing a doubly linked list.

References:

[https://www.hackerrank.com/challenges/reverse-a-doubly-linked-list/problem?h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=linked-lists](https://www.hackerrank.com/challenges/reverse-a-doubly-linked-list/problem?h_l=interview&playlist_slugs[]=interview-preparation-kit&playlist_slugs[]=linked-lists)

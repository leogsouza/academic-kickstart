---
title: Learning Data Structures - Linked List
authors:
  - leogsouza
date: 2021-01-04T11:19:00Z
reading_time: true
featured: true
draft: false
summary: Learning about Linked Lists
image:
  placement: 3
  caption: 'Image credit: [**Kaley Dykstra**](https://unsplash.com/@kaleyloved)'

tags: ["Go", "Data Structure"]
---

A linked list is another linear data structure, like array, it stores elements in a linear way. However, unlike arrays, linked lists does not stores its elements at contiguous memory location. The elements are connected to each other using nodes. In another words, a linked list is a list of nodes where each node contains a data field and a reference (link) to the next node in the list.

Because of its form, this data structure allows add and remove elements eficiently from any position within the list during interation. But, the search cost more effort and often requires O(n) time to find an element.

Let's dive into some code e see how implement a Linked List in Go:

~~~go

package main

// Node represents a linked list's node
type Node struct {
	Data int
	Next *Node
}

// NewNode creates a pointer to a new Node
func NewNode(data int) *Node {
	newNode := &Node{}
	newNode.Data = data

	return newNode
}

// LinkedList is a linked list data structure
type LinkedList struct {
	Head *Node
}

// AddToHead adds a new node into linked list head
func (ll *LinkedList) AddToHead(data int) {

	newNode := NewNode(data)

	newNode.Next = ll.Head
	ll.Head = newNode

}

// AddAfter adds a new node after the given prevNode
func (ll *LinkedList) AddAfter(prevNode *Node, data int) {
	if prevNode == nil {
		fmt.Println("The given previous node cannot be null")
	}

	newNode := NewNode(data)

	newNode.Next = prevNode.Next

	prevNode.Next = newNode
}

// AddToEnd adds a new node into do end of the linked list
func (ll *LinkedList) AddToEnd(data int) {
	newNode := NewNode(data)

	if ll.Head == nil {
		ll.Head = newNode
		return
	}

	last := ll.Head
	for last.Next != nil {
		last = last.Next
	}

	last.Next = newNode
}

// DeleteNode deletes the first occurrence of a key in linked list
func (ll *LinkedList) DeleteNode(key int) {
	temp, prev := ll.Head, &Node{}

	if temp != nil && temp.Data == key {
		ll.Head = temp.Next
		return
	}

	for temp != nil && temp.Data != key {
		prev = temp
		temp = temp.Next
	}

	if temp == nil {
		return
	}

	prev.Next = temp.Next

}

// DeleteAt deletes a node at specific position
func (ll *LinkedList) DeleteAt(position int) {
	if ll.Head == nil {
		return
	}

	node := ll.Head

	if position == 0 {
		ll.Head = node.Next
	}

	for i := 0; node != nil && i < position-1; i++ {
		node = node.Next
	}

	if node == nil || node.Next == nil {
		return
	}

	next := node.Next.Next

	node.Next = next
}

// DeleteList deletes the entire Linked List
func (ll *LinkedList) DeleteList() {
	ll.Head = nil
}

~~~

For the moment, that's all.


Thanks for reading, see you in the next post.
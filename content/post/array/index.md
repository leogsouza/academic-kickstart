---
title: Learning Data Structures - Arrays
authors:
  - leogsouza
date: 2020-12-24T11:02:00Z
reading_time: true
featured: true
draft: false
summary: Getting started with Arrays
image:
  placement: 3
  caption: 'Image credit: [**AltumCode**](https://unsplash.com/photos/oZ61KFUQsus)'
---

Array is a data structure used to store a fix number of elements and these elements should be of the same type. 
In Go we create and use arrays as follows:

```go

package main

import "fmt"

func main() {
  // we are creating an array that should store 3 elements
  var a [3]int

  // In Go, by default, an array is zero-value which means 
  // that when is created an array of int type and it's not initialized, 
  // all array positions are filled with 0s.
  fmt.Println("array elements:", a)

  // Set a value at specific index
  a[1] = 5

  fmt.Println("array element set:", a)
  fmt.Println("array at index 1:", a[1])

  // length of array
  fmt.Println("array length: ", len(a))

  // traversing the array
  fmt.Println("Traversing array: ")
  for i := 0; i < len(a); i++ {
    fmt.Print(a[i], " ")
  }
}

```

This is a short explanation about arrays. Next time, I'll discuss about Linked List. 

Thanks a lot.
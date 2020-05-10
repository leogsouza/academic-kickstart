---
title: Your first program in Go (Golang)
authors:
  - leogsouza
date: 2020-05-08
draft: false
feathred: true
tags: ["Go", "Beginner"]
---

Hi Everyone, when we are learning a new programming language it's common starting with the classic "Hello, World" program. So this is what we'll do now in Go.

For this tutorial I'll consider that you have go installed in your machine. If you don't have go installed in your machine please access the [Go documentation](https://golang.org/doc/install) and follow the steps into installation section.

## Writing your code

Start creating a folder hello in your computer and inside of it create a new file called main.go.
Next, add this content to main.go file

```go
package main

import "fmt"

func main() {
  fmt.Println("Hello, World")
}
```
Let's look through the code and understand the code.

In the first line we have the package declaration
```go
package main
```
Every go program is made up of packages and the program start running in package main.

In the next line we are using a package inside our program.
```go
import "fmt"
```
In our case we are using the package **"fmt"** to use a function to print a message on the screen.

Following the code we have the function main
```go
func main() {
  fmt.Println("Hello, World")
}
```

Every Go program has one and only one function main and inside of it you put what your program have to do. In this piece of code we are just calling the function **Println** from the **fmt** package and passing "Hello World" as argument. The function Println from "fmt" package just print the message passed as argument and appends a new line.


## Executing the program
To execute a go program you have to use the Go command to compile and run the program. 
Inside the folder that you created the main.go, run the command like this:
```bash
  $ go run main.go
  "Hello, World"
```

For the moment, that's all.


Thanks for reading, see you in the next post.




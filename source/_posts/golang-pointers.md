---
title: Golang's pointers
date: 2022-06-10 18:58:00
metatags: golang
description: Golang's pointers
cover: "posts/golang.png"
---

![Golang](/posts/golang.png)

# Pointers

A pointer holds a variable's address in the computer's memory. One can say that once a pointer is created, its value is just an address that lead you to where in the computer's memory the program will store the actual data.

## Example

```go
package main

import "fmt"

func main() {

	// Creating a pointer
	var fullNamePtr *string = new(string)
	fmt.Println(fullNamePtr) // Prints the address: 0x14000110230
	
	// Storing value in the pointer's address by dereferencing it
	*fullNamePtr = "John Doe"
	fmt.Println(fullNamePtr, *fullNamePtr)
	
	// Getting the pointer of an existing variable
	country := "Brazil"
	fmt.Println(&country)
}
```
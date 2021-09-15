# lstack
This is a generalized stack package with clean and transparent API for the Go language.

## Features
- Lightweight and Fast.
- Native Go implementation.
- Support all data types.

## Requirements
- Go 1.9 or higher. We aim to support the 3 latest versions of Go.

## Installation
Simple install the package to your [$GOPATH](https://github.com/golang/go/wiki/GOPATH "GOPATH") with the [go tool](https://golang.org/cmd/go/ "go command") from shell:
```bash
$ go get -u github.com/lovesaroha/lstack
```
Make sure [Git is installed](https://git-scm.com/downloads) on your machine and in your system's `PATH`.

## Usage

### Create Stack

```Golang
  // Create a stack.
  stack = lstack.Create()

  // Add values in stack.
  stack.Push(2)
  stack.Push(4)
  stack.Push(6)
  stack.Push("love")

  // Remove value from stack and return value.
  stack.Pop()

  // Print values in stack.
  stack.Print()

```

### Add Multiple Values

```Golang
  // Create a stack.
  stack = lstack.Create()

  // Add values in stack.
  stack.PushValues([]interface{}{1,2,3,4,5,6,7,8,9})

  // Remove value from stack and return value.
  stack.Pop()

  // Print values in stack.
  stack.Print()

```

### Custom Data Type
```Golang 
  type user struct {
    name string
  }

  // Create a stack.
  stack = lstack.Create()

  // Add values in stack.
  stack.Push(user{name: "love"})
  stack.Push(user{name: "joe"})
  stack.Push(user{name: "doe"})

  // Remove value from stack and return value.
  stack.Pop()

  // Print values in stack.
  stack.Print()

```

### Pop Values With Specific Data Type
```Golang 

  // Create a stack.
  stack = lstack.Create()

  // Add values in stack.
  stack.Push(2)
  stack.Push(4)
  stack.Push(6)
  stack.Push("love")

  // Remove value from stack and return string value ("love").
  stack.PopString()
  // Remove value from stack and return int value (6).
  stack.PopInt()
  // Remove value from stack and return float64 value (4.00).
  stack.PopFloat64()

  // Print values in stack.
  stack.Print()

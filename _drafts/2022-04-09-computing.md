---
layout: post
title:  Things you must know as a software engineer
date:   2022-04-09 00:30:05 +0800
author: Fang Guojian
tags: CS
---

# Things you must know as a software engineer
---
## [Programming paradigm](https://en.wikipedia.org/wiki/Programming_paradigm)

Common programming paradigms include:

- *imperative* in which the programmer instructs the machine how to change its state,
- *declarative* in which the programmer merely declares properties of the desired result, but not how to compute it


---
### Imperative

- ***procedural*** which groups instructions into procedures,
- ***object-oriented*** which groups instructions with the part of the state they operate on,


---
### Declarative

- ***functional*** in which the desired result is declared as the value of a series of function applications,
- *logic* in which the desired result is declared as the answer to a question about a system of facts and rules,
- *mathematical* in which the desired result is declared as the solution of an optimization problem
- ***reactive*** in which the desired result is declared with data streams and the propagation of change
---
### Example: Euclidean algorithm

```go
func gcd(a, b int) int {
    for {
        if b == 0 {
            return a
        }
        t := b
        b := a % b
        a := t
    }
}
```
---
```go
func gcd(a, b int) int {
    if b == 0 {
        return a
    }
    return gcd(b, a % b)
}
```




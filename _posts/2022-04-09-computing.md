---
layout: post
title:  Things you must know as a software engineer
date:   2022-04-09 00:30:05 +0800
author: Fang Guojian
tags: CS
marp: true
---

# Things you must know as a software engineer

---

## #0 Learn Lambda Calculus

---

### DEFINITION

(i) *Lambda terms* are words over the following alphabet:
|||
|---|---|
|$v_0, v_1, ...$|variables,|
|$\lambda$|abstractor,|
|$(, )$|parentheses.|

(ii) The set of $\lambda$-terms $\Lambda$ is defined inductively* as follows:
(1) $x \in \Lambda ;$
(2) $M \in \Lambda \implies (\lambda x M) \in \Lambda ;$
(3) $M, N \in \Lambda \implies (M N) \in \Lambda;$
where $x$ in (1) or (2) is an arbitrary variable.

---

A variable $x$ occurs *free* in a $\lambda$-terms $M$ if $x$ is not in the scope of a $\lambda x$; $x$ occurs *bound* otherwise.

In $x (\lambda y.xy)$, $x$ occurs free and $y$ occurs bound.
In $y (\lambda y.y)$, $y$ occurs both free and bound.

---

## #1 Choose programming paradigm wisely

---

## [Programming paradigm](https://en.wikipedia.org/wiki/Programming_paradigm)

Common programming paradigms include:

- *imperative* in which the programmer **instructs** the machine how to change its state.

<img src="{{site.baseurl}}assets/img/imperative.svg" alt="">
<!-- 
@startuml
digraph G {
rankdir="LR";
    "State 0" -> "State 1" [label="action 0"]
    "State 1" -> "State 2" [label="action 1"]
    "State 2" -> "State ???" [label="action 2...N"]
} 
@enduml
-->

- *declarative* in which the programmer merely **declares** properties of the desired result, but not how to compute it.

<img src="{{site.baseurl}}assets/img/declarative.svg" alt="">
<!--
@startuml
digraph G {
rankdir="LR";
    "State 0" -> "State N" [label="???"]
} 
@enduml
 -->

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

### Example

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

```go
func gcd(a, b int) int {
    if b == 0 {
        return a
    }
    return gcd(b, a % b)
}
```

---

## #1.1 Write stateless code as much as possible

---

## #2 Context matters a lot

---

## References

“Conversion.” *The Lambda Calculus: Its Syntax and Semantics*, College Publications, 2012.

[Presentation](/assets/2022-04-09-computing.html)

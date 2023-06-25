---
layout: post
title: "Using assertions in production"
date: "2012-03-27"
categories: 
  - dev
tags: 
  - java
---

Code assertions provide a clear way to define the required behaviour of an application. For example, the following Java assertion states that the variable **number** should be non-negative<!--more-->:

```java
assert ( number >= 0)
```

Unlike exceptions, which can be caught and handled gracefully, an assertion failure indicates that something has gone terribly wrong within the application and causes it to exit. Thus, in the above example, if assertions are switched on and **number** is equal to **\-5** the application will crash.

## The Dilemma

There is a question about whether assertions should be switched on in production code.

**The argument for switching them off roughly follows:**

> Production applications should not suddenly and unexpectedly crash.  Assertions should be left on during testing and switched off during production code.  Adequate logging should be used to ensure any anomalous application states are identified.

**The argument for switching them on roughly follows:**

> Assertions specify conditions which should never occur. Leaving assertions off in production code may allow the application to run in an unstable state. Failing early allows the problem to be identified and corrected sooner.

## The Answer...well sort of

Like all things, the answer will depend on your domain and your needs. Early failure is definitely the way to go however, you may, for some spectacular reason, be in a situation where running an unstable application is preferable to a non-running application.

The biggest problem with assertions, however, is not that they can cause an unstable application to crash, but that they can cause a stable application to slow down. Consider an optimised sort method which gets called on a large data set - a few additional expensive assert evaluations could jeopardise the efficiency of the base code.  For this reason, Oracle switches assertions off by default on Java.

**The answer then seems to be to have assertions switched on during testing and switched off in production for optimisation reasons. And one other thing, your unit tests should be damn good.**

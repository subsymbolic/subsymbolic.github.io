---
layout: post
title: "7 Objective C tips to avoid memory mistakes"
date: "2012-11-18"
categories: 
  - dev
tags:
  - objective-c
  - ios
  - memory-management
---

![Apple Memory Management](/assets/objc-memory-management.jpg "Apple Memory Management")

There is no argument to be had about whether ARC is beneficial. The reduction of boiler-plate memory code, is alone, enough to justify its use. The elimination of issues resulting from objects being incorrectly retained or released also saves developers untold hours debugging weird memory management issues. <!--more-->

However much ARC has simplified matters, issues will still arise if memory management is not adequately understood. These issues commonly fall into two categories, **retain cycles** and **accessing released memory**.

The following tips may help developers avoid common mistakes. Tips 1, 2, 3 and 4 deal with retain cycles while 5, 6 and 7 deal with accessing released memory.

## Avoid retain cycles

**TIP ONE:** Do not retain delegates. Use a weak lifetime qualifier.

**TIP TWO:** Beware of accessing block owners within a block.

**TIP THREE**: Do not retain IBOutlets unless Tip Five applies. Use a weak lifetime qualifier.

**TIP FOUR**: Do not retain subviews. Use a weak lifetime qualifier.

## Avoid accessing released items

**TIP FIVE:**  Do retain top-level IBOutlets (but NOT the main view or subviews). Use a strong lifetime qualifier.

**TIP SIX:** Do not access IBOutlets unless the ViewController is currently at the top of the stack

**TIP SEVEN:** Copy member blocks.

**Memory management is a complex area and it is easy to make mistakes which are difficult to debug and which suck up time. If there is one area to invest time in understanding, this is it. Apple's memory guides are thorough and worth a read.**

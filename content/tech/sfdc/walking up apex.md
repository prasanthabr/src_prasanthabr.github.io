---
date: 2019-06-06T06:00:00+06:00
lastmod: 2021-10-06T17:30:00+06:00
title: Walking up Apex
authors: ["prasanthabr"]
categories:
  - Salesforce.com
tags:
slug: walking-up-in-apex
draft: false
---
updated on 20Jan22

Random thoughts on Apex development
1. Avoid deeply nexted if statements --> find a pattern that should be used in a
   cascade of checks?
2. Small functions with easily testable inputs and outputs --> what are
   functions here? Are these methods?
3. Fast Tests --> meaning short tests that execute quickly
4. Good balance between abstraction and implementation --> have no clue what
   this means?? --> apparently a good example is when code (tests) are written
   with so many helper functions (I have seen helpers in rails, but should
   understand what this means universally) that it is difficult to read and
   understand what the code does. New funcationality added will break tests -->
   this is something that was observed.

   what are chunking errors? --> need to read further

   Method Overloading --> seems to be the way of defining the same method with
   multiple signatures --> input values; ! wonder if its the same output type
   --> from memory no; have to recheck.

## Brain Dump
- YCombinator School
- Plan how to market
- Micro Sites

picking up on apex

## Data Types
All variables and expressions have a datatype. Need to understand why an
expression would have a datatype (?)

A string, Integer, boolean -> all inherit object. remind me of Ruby where
everything is an Object. Saw a creative use of object, when using object as an
attribute on a method - so that it can handle the various types that are listed
as an object. Trick is - an integer can be held on an object variable. NOTE:
Read up more on this one.

Much like there are primitive and non primitive datatypes in other languages,
there are primitive, non primitive (sObject or custom Apex type) and enums in Apex.

Read more on how the custom Apex types are used and also enums.
Did encounter custom Apex types in the external service setup a while back. when
using a flow to update the api schema, the custom apex type is used to populate
the same.

Another interesting use case is where sObject can be generic or specific - have
seen this used in Congnizant and at other places - the concept seems simple
enough to wrap your head around. Define in generic terms, so that the method can
be used on different sObject types - very similar to the Object specification I
would say.

Ref:
https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/langCon_apex_data_types.htm

### Primitive Data Types




### Notes to Self

##### Apex Triggers
a before trigger is riding the wave and can make changes on the record -- so its natural that it does not support a DML statement
context variables indicate the triggering values and the behaviour of the trigger

addError - to cause a fatal error and prevent further execution -- this is interesting!

need to read further on method operators - so the static operator implies that
the method does not need to be instatiated.

so all apex variables are initialized to null. Something that is missed in
boolean. Always initialize boolean to flase.

Dates are limited in its arithmetic functions. Integers can be added or
substracted from dates. Any further operations require date methods.

Dates and DateTimes should be created in system static methods. Need to figure
out what a system static method is. <- NOTE

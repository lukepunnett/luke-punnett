---
layout: post
title: Strings - Understanding Data Structures in Java
description: Tackling key data structures in Java pt.3 - Sets
---
    Set Interface:

    Set is an interface in Java which extends the Collection interface.
    It is an unordered collection of unique elements, i.e., it cannot contain duplicate elements.
    Commonly used Set implementations: HashSet, TreeSet, and LinkedHashSet.

java

import java.util.Set;
import java.util.HashSet;

    HashSet:

    HashSet is an implementation of the Set interface.
    It uses a hash table to store elements.
    It doesn't guarantee any specific order of elements.
    It permits null values.
    Offers constant time O(1) performance for basic operations like add, remove, contains, and size.

Creating a HashSet:

java

Set<String> hashSet = new HashSet<>();

Adding elements to a HashSet:

java

hashSet.add("apple");
hashSet.add("banana");
hashSet.add("orange");

Checking if a HashSet contains an element:

java

boolean containsApple = hashSet.contains("apple");

Removing an element from a HashSet:

java

hashSet.remove("apple");

Getting the size of a HashSet:

java

int setSize = hashSet.size();

Iterating over a HashSet:

java

for (String element : hashSet) {
    System.out.println(element);
}

Converting a HashSet to an Array:

java

String[] array = hashSet.toArray(new String[hashSet.size()]);

Clearing all elements in a HashSet:

java

hashSet.clear();

Checking if a HashSet is empty:

java

boolean isEmpty = hashSet.isEmpty();

These basic operations should give you a good start when working with Sets and HashSets in Java. The same operations can also be applied to other Set implementations like TreeSet and LinkedHashSet, with minor differences in their behavior and performance characteristics.
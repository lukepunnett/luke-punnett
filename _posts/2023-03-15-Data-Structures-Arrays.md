---
layout: post
title: Arrays - Understanding Data Structures in Java
description: Tackling key data structures in Java pt.1 - Arrays
---

Absolute need to knows for all data structures:
1. Initialisation
2. data access
3. modification
4. iteration
5. sort
6. addition
7. deletion
```
public class Main {
    public static void main(String[] args) {
        // 1. Initialize
        int[] a0 = new int[5];
        int[] a1 = {1, 2, 3};
        // 2. Get Length
        System.out.println("The size of a1 is: " + a1.length);
        // 3. Access Element
        System.out.println("The first element is: " + a1[0]);
        // 4. Iterate all Elements
        System.out.print("[Version 1] The contents of a1 are:");
        for (int i = 0; i < a1.length; ++i) {
            System.out.print(" " + a1[i]);
        }
        System.out.println();
        System.out.print("[Version 2] The contents of a1 are:");
        for (int item: a1) {
            System.out.print(" " + item);
        }
        System.out.println();
        // 5. Modify Element
        a1[0] = 4;
           for (int item: a1) {
            System.out.print(" " + item);
        }
        System.out.println("Now let's sort");
        // 6. Sort
        Arrays.sort(a1);
         for (int item: a1) {
            System.out.print(" " + item);
        }
        
    }
}
```
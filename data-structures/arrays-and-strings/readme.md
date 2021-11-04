# Hash Tables

A hash tible is a data structure that maps keys to values for highly efficient lookup.

use an array of linked lists and a hash code function to implemente simple hash table.
To insert a key(string or any other data type) and value
1. First, compute the key's hash code(usually int or long). Two different keys could have the same hash code, as there may be an infinite number of keys and a finite number of ints
2. Then, map the hash code to an index in the array. hash(key) % array_length. Two different hash code could map to the same index
3. At this index, there is a linked list of keys and values. Store the key and value in this index. We must use a linked list because of collisions: you could have two different keys with the same hash code, or two different hash codes that map to the same index

### BigO
If the number of collisions is very high, the worst case runtime is O(N), where N is the number of keys
We generally assume a good implementation that keeps collisions to a minimum, in which case the lookup time is O(1)

# ArrayList & Resizable Arrays

# StringBuilder

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

In some languages, arrays(often called lists in this case) are automatically resizable. The array or list will grow as you append items. In other languages, like Java, the array's size can't change after its creation. </br></br>
An ArrayList is an array that resizes itself as needed while still providing O(1) access. A typical implementation is that when the array is full, the array doubles in size. Each resizing takes O(n) time, but happens so rarely that its amortized insertion time is still O(1)
```Java
ArrayList<String> merge(String[] words, String[] more) {
  ArrayList<String> sentence = new ArrayList<String>();
  for (String w : words) sentence.add(w);
  for (String w : more) sentence.add(w);
  return sentence;
}
```
<i> Why is the amortized insertion runtime O(1)? </i>
N/2 + N/4 + N/8 + ... + 2 + 1

# StringBuilder

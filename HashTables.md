# Hash Tables

## What is a Hashtable?

Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

## Why do we use them?

1. Hold unique values
2. Dictionary
3. Library

- A hash table is a data structure that is used to store keys/value pairs. It uses a hash function to compute an index into an array in which an element will be inserted or searched. By using a good hash function, hashing can work well. Under reasonable assumptions, the average time required to search for an element in a hash table is O(1).

- Let us consider string S. You are required to count the frequency of all the characters in this string.

```
string S = “ababcd”
```

The simplest way to do this is to iterate over all the possible characters and count their frequency one by one. The time complexity of this approach is O(26*N) where N is the size of the string and there are 26 possible characters.

```
  void countFre(string S)
    {
        for(char c = ‘a’;c <= ‘z’;++c)
        {
            int frequency = 0;
            for(int i = 0;i < S.length();++i)
                if(S[i] == c)
                    frequency++;
            cout << c << ‘ ‘ << frequency << endl;
        }
    }
```

Output

a 2
b 2
c 1
d 1
e 0
f 0
…
z 0

## Structure

- Creating a Hash:

A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a simplistic hashing algorithm:

Add or multiply all the ASCII values together.
Multiply it by a prime number such as 599.
Use modulo to get the remainder of the result, when divided by the total size of the array.
Insert into the array at that index.
Example:

```
Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16
```

Key gets placed in index of 16.
We now know that our key Cat maps to index 16 of the array. We can view into this index and find “Josie”, our value quickly.

- Hash maps do this to store values:

1. accept a key
2. calculate the hash of the key
3. use modulus to convert the hash into an array index
4. store the key with the value by appending both to the end of a linked list

- Hash maps do this to read value:

1. accept a key
2. calculate the hash of the key
3. use modulus to convert the hash into an array index
4. use the array index to access the short LinkedList representing a bucket
5. search through the bucket looking for a node with a key/value pair that matches the key you were given

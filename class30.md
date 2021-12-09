# Hash Tables

### What is a Hashtable?

1. **Hash :** *A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array ( A data structure that is used to store keys/value pairs)*

2. **Buckets :** *A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.*

3. **Collisions :** *A collision is what happens when more than one key gets hashed to the same location of the hashtable.*

***

### Why to use Hash tables?

- Hold unique values
- Dictionary
- Library
  
- Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.
  
 - The basic idea of a hashtable is the **ability to store the key into this data structure, and quickly retrieve the value.** This is done through what we call a hash
  
- `hash` is the ability to encode the key that will eventually map to a specific location in the data structure that we can
  
- `search through the data to look up` a neighborhood and obtain it’s zip code. We could do this using a for loop that looks through each piece of data one by one until it finds the neighborhood name, then returns the zip code there. This would be an` O(N) read operation because it requires searching through each piece of data to find the one piece we want`.

- `Hash maps take advantage of an array’s O(1) read access.` Instead of adding elements to an array from beginning to end, a hash map uses a “hash function” to place each item at a precise index location, based off it’s key.

***
### Creating a Hash
- `Hashing`
Basically, a hash code turns a key into an integer. 

- `Creating a Hash`
A hashtable traditionally is created from an array
  - Add or multiply all the ASCII values together.
  - Multiply it by a prime number such as 599.
  - Use modulo to get the remainder of the result, when divided by the total size of the array.
  - Insert into the array at that index.
  
  **ASCII:**, abbreviated from American Standard Code for Information Interchange, is a character encoding standard for electronic communication. ASCII codes represent text in computers, telecommunications equipment, and other devices.

  ![](https://www.unitronicsplc.com/Download/SoftwareHelp/VisiLogic_Knowledgebase/ASCII_Table.gif)

```js
  Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16. 
  ```

**We now know that our key Cat maps to index 16 of the array. We can view into this index and find “Josie”, our value quickly.**
***️

## Collisions

- Collision occurs when more than one key hashes to the same index in an array.
- Collisions are solved by changing the initial state of the buckets.
- Instead of starting them all as null we can initialize a LinkedList in each one.
- Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list.
- Since different keys can lead to the same bucket it’s important to store the entire key/value pair in the bucket, not just the value.

## How to Store Values?

- Hash maps to this to store values:
  - accept a key.
  - calculate the hash of the key.
  - use modulus to convert the hash into an array index.
  - store the key with the value by appending both to the end of a linked list.

## How to Read Values?

- Hash maps do this to read value:
  - accept a key
  - calculate the hash of the key
  - use modulus to convert the hash into an array index
  - use the array index to access the short LinkedList representing a bucket
  - search through the bucket looking for a node with a key/value pair that matches the key you were given

****

## Intranal Methods

`Add()`

When adding a new key/value pair to a hashtable:

 - send the key to the GetHash method.
 - Once you determine the index of where it should be placed, go to that index
 - Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
 - If something does exist, add the new key/value pair to the data structure within that bucket.


`Find()`

The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

`Contains()`

The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

`GetHash()`

The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.
# Hashtables

- Hashtables are a data structure that utilize key value pairs.
- every Node or Bucket has both a key, and a value
- hash: is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.
- O(1) time complexity.

## Terminology

- Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

## Hashing

- hash code turns a key into an integer.
- very important that hash codes are deterministic
- output is determined only by their input.
- Hash codes should never have randomness
- The same key should always produce the same hash code.

## Collisions

- collision occurs when more than one key hashes to the same index in an array.

## Internal Method

- Add() sends a key to gethash method
- Find() takes a key gets the hash and goes to the index.
- Contains() takes a key and return a boolean if that key exists.
- GetHash() accepts a akey as string and conducts the hash.

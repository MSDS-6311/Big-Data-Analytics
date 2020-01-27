# Assignment 2. Hash functions (work in progress)


Due Feb 3, 2020

Hash functions find wide use in Data Science.  

Some uses include: 
1. In software, hash functions are used to organize data for fast lookup in data structures known as hash tables or associative arrays. An example of such data structure is the `dict` data type in Python.
1. Data integrity checking. A hash can be used as a checksum to verify that the contents of a file has not been changed. Unlike simple sums, hashes are difficult to manipulate. 
1. As identifiers for data items. [UUIDs](https://docs.python.org/3/library/uuid.html) (universally unique identifiers) are generated with the help of hash functions. 
1. [Cryptography and cybersecurity](https://en.wikipedia.org/wiki/Cryptographic_hash_function), including encryption, digital signatures, password authentication, [cryptocurrency](https://www.coindesk.com/bitcoin-hash-functions-explained), etc.
1. For data partitioning (e.g. [Hadoop](https://data-flair.training/blogs/hadoop-partitioner-tutorial/) and [database sharding](https://blog.yugabyte.com/how-data-sharding-works-in-a-distributed-sql-database/))

In this exercise, you will master the following two modules of the Python standard library:
* [`hashlib`](https://docs.python.org/3.7/library/hashlib.html)
* [`uuid`](https://https://docs.python.org/3.7/library/uuid.html)


In our  `main.data-science-ust`, create 

### Problem 1 (Math).
What minimum number of bits must a hash function encode so that 1 billion items would have less that 1% chance of colliding, i.e. producing the same hash value for two different items. 

### Problem 2 (Math). 
UUID uses 122 free bits, i.e. bits available for encoding unique IDs since some 6 bits are reserved to encode the UUID version.  How many items can be identified by UUIDs before there is a 1% chance of collision? 

### Problem 3. File checksums.
...

### Problem 4. Password check
Secure password do not store user passwords. Instead, they store the hashes of passwords. 
This enables the system to check passwords even if someone gets access to the hashes. 


Read about [password salting](https://auth0.com/blog/adding-salt-to-hashing-a-better-way-to-store-passwords/).


### Problem 5. Password break
You found that someone is using a password consisting of only three characters and you found that its md5 hash is `52268f215114b03e97f21b8227b487af`.
The password hash was "salted" with the prefix "s7".  This means that if the password was "a7#", then the hash would be computed on the string "s3A7#". 

Write a short python program, `password_break.py` that breaks the password. What was the password? 


### Problem 3. Assign UUIDs. 
...

### Problem 4. Partition names.
...


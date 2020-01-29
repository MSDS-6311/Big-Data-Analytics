# Assignment 2. Hash functions and UUIDs


Due Feb 3, 2020

Hash functions find wide use in Data Science.  

Some uses include: 
1. In programming, hash functions are used to organize data for fast lookup in data structures known as hash tables or associative arrays. An example of such data structure is the `dict` data type in Python.
1. Data integrity checking. A hash can be used as a checksum to verify that the contents of a file has not been altered. Unlike simple sums, hashes are difficult to manipulate. 
1. As identifiers for data items. [UUIDs](https://docs.python.org/3/library/uuid.html) (universally unique identifiers) are generated with the help of hash functions. 
1. [Cryptography and cybersecurity](https://en.wikipedia.org/wiki/Cryptographic_hash_function), including encryption, digital signatures, password authentication, [cryptocurrency](https://www.coindesk.com/bitcoin-hash-functions-explained), etc.
1. For data partitioning (e.g. [Hadoop](https://data-flair.training/blogs/hadoop-partitioner-tutorial/) and [database sharding](https://blog.yugabyte.com/how-data-sharding-works-in-a-distributed-sql-database/))

In this exercise, you will master the following two modules of the Python standard library:
* [`hashlib`](https://docs.python.org/3.7/library/hashlib.html)
* [`uuid`](https://https://docs.python.org/3.7/library/uuid.html)

The purpose of this exercise is develop understanding and skills for using hashes for identification and verification of data objects. 


In your home folder on `main.data-science-ust`, create the folder `~/homework/a02`. 
For each problem below, save the answer in a separate file with extensions `.txt` for text files and `.py` for python programs. Make the python programs executable specifying the Python interpreter and granting the `x` permission to yourself with the `chmod` command.

### Problem 1 (Math).
What minimum number of bits must a hash function encode so that 1 billion items would have less that 1% chance of colliding, i.e. producing the same hash value for two different items. 

This type of problem is described as the [birthday paradox](https://betterexplained.com/articles/understanding-the-birthday-paradox/), also [on wikipedia](https://en.wikipedia.org/wiki/Birthday_problem).

Save as your answer and reasoning in plain text in file `~/homework/a02/problem1.txt` 


### Problem 2 (Math). 
UUID uses 122 free bits, i.e. bits available for encoding unique IDs since some 6 bits are reserved to encode the UUID version.  How many items can be identified by UUIDs before there is a 1% chance of collision? 

Save as your answer and reasoning in plain text in file `~/homework/a02/problem2.txt` 

### Problem 3. File checksums.

Imagine that someone shared a collection of files with you found in folder `/home/shared/a02-share`. The folder contains `checksums.txt` with a list of data filenames and their md5 checksums. Write a python program that reads `checksums.txt` and reports any missing or corrupt files in the folder.

Save your program as `~/homework/a02/problem3.py` and make it executable.


### Problem 4. Password check
Secure systems do not store user passwords directly. Instead, they store the hashes of passwords.
This enables the system to check passwords even if someone is able to read the stored hashes. 
Stealing the hashes does not enable one to break into the system. 
As an extra precaution, passwords are prefixed by a short random string called "salt", which is stored along with the hash. 
This prevents someone from detecting if the same password is used twice. 
Read more about [password salting](https://auth0.com/blog/adding-salt-to-hashing-a-better-way-to-store-passwords/).

Write a python program to answer which of the following passwords corresponds to the `sha-1` checksum `334fd4c7a6283b9c09705f500dd97722a83398fb`  with the salt string `a0q7`. This means that if the password was `Freedom7`, the string passed to `sha1` would be `a0q7Freedom7`.

```python
salt = "a0q7"
pass_hash = "334fd4c7a6283b9c09705f500dd97722a83398fb"
passwords = ['aardvarK7', 'platypU7', 'platypus', 'sea-otter-37', 'Mirounga33', 'Dugong!']
```

Save your program as `~/homework/a02/problem4.py` and make it executable. 

### Problem 5. Password break
You found that someone is using a password consisting of only three characters and you found that its `md5` hash is `52268f215114b03e97f21b8227b487af`.
The password hash was "salted" with the prefix "s7".  This means that if the password was "a7#", then the hash would be computed on the string "s7a7#". 

Write a short python program that breaks the password. What was the password? 

Save your program as `~/homework/a02/problem5.py`

### Problem 6. Assign UUIDs. 
Imagine we are creating a database of courses offered across all universities (e.g. Coursicle style).  To identify courses in this database, we will use UUID version 5.
Start with the null context UUID `UUID('00000000-0000-0000-0000-000000000000')`, write a short Python script that generates a UUID for the string "University of St Thomas", then using the university UUID as the context, create program UUID for string "MSDS". Then for using the program UUID, create UUIDs for courses "5312", "5315", and "6311".

Save your program as `~/homework/a02/problem6.py`

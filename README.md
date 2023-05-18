# What is this

You have object A of FORMAT_A and object B of FORMAT_B

You need to convert from A to B

**A -> B**

For whatever reason:

*You want an untrusted third party to be able to define the conversion logic at runtime*

You need to perform the conversion safely, with **guaranteed** success and correctness.

The third party needs to be able to define highly complex conversion logic (but not arbitrarily complex).

## why in the worl-

**ok, imagine GraphQL but if client could**

- define a query
- define how to manipulate the result of that query
- make conditional decisions based on results
- stick transformed result right back into some other query or even queries
- do this as many times as you want before returning result

(Yes, GraphQL can **sorta** do this, but conversion logic complexity is limited)

All this logic **runs entirely on server**, avoiding network heavy ping-pong between client/server.

This can occur because server can guarantee
- maximum time complexity
- maximum space complexity
- transformation is possible and will succeed
- execution safety

There are also many other megabrain applications, including distributed secure computation, e.g. smart contracts on blockchain.

In theory, you can also determine high quality estimates of true execution time because
given actual input data, you can calculate exact T(N) (number of operations). 

## what is this

In a pure sense, this is a programming language which is **guaranteed to halt in finite time**.

Practically, this is a library for
- defining complex conversion logic between two arbitrary data formats
- verify conversion logic correctness, allowing for determination of:
    - time and space complexity upper bounds
    - conversion validity based on input/output formats
- run conversions, which are guaranteed to succeed if valid



## attempt

![attempt](https://www.cs.utexas.edu/~angg/attempt.png)

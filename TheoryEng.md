# Theory for Solving the "Happy Prime Numbers"

## Understanding the Problem

The task is to develop a program to find the number of "happy" prime numbers in a given range from L to R.

The input data for the program is provided as a string, where:
- The first part is the lower limit.
- The second part is the upper limit of the range.
- These two parts are separated by #.

### Example:

For the string:
```
"5#50"
```
- The first part 5 is the lower limit.
- The second part 50 is the upper limit.

## Prime Numbers

A prime number is a natural number greater than 1 that is divisible only by 1 and itself. Examples of prime numbers: 2, 3, 5, 7, 11, etc.

Properties of prime numbers:
- The first prime number is 2, the only even prime number.
- The number of prime numbers is infinite (proved by Euclid).
- Any natural number greater than 1 is either prime or composite (it can be factored into prime numbers).
- Any natural number greater than 1 can be uniquely represented as a product of prime numbers (Fundamental Theorem of Arithmetic).

## Sieve of Eratosthenes

The Sieve of Eratosthenes is an algorithm for finding all prime numbers from 1 to n.

The main idea corresponds to the name of the algorithm: we write a series of numbers 1, 2,..., n, and then we cross out
- first the numbers divisible by 2, except the number 2 itself,
- then the numbers divisible by 3, except the number 3 itself,
- we do not do anything with the numbers divisible by 4 because we have already crossed them out,
- then we continue to cross out the numbers divisible by 5, except the number 5 itself,

…and so on.

## Main Steps of the Algorithm

### Input Data

Obtain two numbers, L and R, which define the range for searching "happy" prime numbers.

### Finding the Largest Digit in Number L

Determine which digit in the number L is the largest. This is needed to check the "happiness" condition of a number.

### Finding All Prime Numbers up to R (Sieve of Eratosthenes)

Finding all prime numbers from 2 to R using the Sieve of Eratosthenes algorithm. This step allows for effectively determining which numbers in the given range are prime.

### Checking Each Number in the Range from L to R

Traverse each number in the range from L to R. For each number, perform the following steps:
- ensure the number is prime,
- check if this number contains the largest digit from the number L; if it does not, then it is considered "happy."

### Counting "Happy" Prime Numbers

Count the number of numbers that satisfy the "happiness" conditions (prime number and does not contain the largest digit from L).

### Output the Result

Output the final count of "happy" prime numbers.

## Time Complexity:

- Sieve of Eratosthenes: $O(nloglogn)$
- Finding the largest digit in number L: $O(logL)4
- Checking for "happiness": $O(RlogR)$
- Overall time complexity: $O(RlogR)$

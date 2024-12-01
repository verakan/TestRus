# Task Description: Happy Prime Numbers

We need to create a console application that will use the Sieve of Eratosthenes to find all prime numbers in a given range and count the number of "happy" prime numbers. 
A happy number in our task is a number that satisfies the following conditions:
- it is a prime number;
- it does not contain the largest digit from the number L in its representation.

The application should accept two integers: L and R. These numbers will define the range in which to find the number of "happy" prime numbers.

The goal of our program is to find the number of "happy" prime numbers in the given range from L to R inclusive.

## Task:

On the number line, two numbers L and R are given. It is necessary to find the number of "happy" prime numbers in the range from L to R inclusive. To solve the problem, use the "Sieve of Eratosthenes" algorithm to find prime numbers.
- The values of L and R (two integers that define the range to find "happy" prime numbers) will be entered into the console. 
L is the lower bound of the range, and R is the upper bound of the range.
- Output one integer representing the number of "happy" prime numbers in the range.

### Input Format:

- A string with two values entered via the console, where the first value is the lower limit of the range and the second value is the upper limit.

### Output Format:

- Output the number of "happy" prime numbers in the given range.

## Example 1:
- **Input**: `5#50`
- **Output**: `12`
- **Explanation**:
1. The largest digit in L = 5 is '5'.
2. Prime numbers up to 50: {2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47}.
3. Checking numbers for the presence of the digit '5':

- 5: contains the digit '5', not "happy".
- 7: does not contain the digit '5', "happy".
- 11: does not contain the digit '5', "happy".
- 13: does not contain the digit '5', "happy".
- 17: does not contain the digit '5', "happy".
- 19: does not contain the digit '5', "happy".
- 23: does not contain the digit '5', "happy".
- 29: does not contain the digit '5', "happy".
- 31: does not contain the digit '5', "happy".
- 37: contains the digit '5', not "happy".
- 41: does not contain the digit '5', "happy".
- 43: does not contain the digit '5', "happy".
- 47: contains the digit '5', not "happy".

## Example 2:
- **Input L**: `3#25`
- **Output**: `5`
- **Explanation**:
1. The largest digit in L = 3 is '3'.
2. Prime numbers up to 25: {2, 3, 5, 7, 11, 13, 17, 19, 23}.
3. Checking numbers for the presence of the digit '3':

- 3: contains the digit '3', not "happy".
- 5: contains the digit '3', "happy".
- 7: does not contain the digit '3', "happy".
- 11: does not contain the digit '3', "happy".
- 13: contains the digit '3', not "happy".
- 17: does not contain the digit '3', "happy".
- 19: does not contain the digit '3', "happy".
- 23: contains the digit '3', not "happy".

# Test Cases

1. **Test 1:**
  - Input: `15#60`
  - Output: `9`

2. **Test 2:**
  - Input: `453#460`
  - Output: `0`

3. **Test 3:**
  - Input: `28#90`
  - Output: `13`

4. **Test 4:**
  - Input: `128#200`
  - Output: `14`

5. **Test 5:**
  - Input: `13#40`
  - Output: `3`

6. **Test 6:**
  - Input: `17#57`
  - Output: `7`

7. **Test 7:**
  - Input: `21#29`
  - Output: `0`

8. **Test 8:**
  - Input: `78#120`
  - Output: `7`

9. **Test 9:**
  - Input: `67#200`
  - Output: `15`

10. **Test 10:**
  - Input: `254#670`
  - Output: `47`

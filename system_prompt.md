# LogicSmith - CustomGPT System Prompt & Specifications
### Role / Persona
* __Persona__: Expert Python mentor + logic coach.
* __Tone__: Friendly, patient, encouraging, slightly playful to keep motivation high.
* __Primary Goal__: Build the user's independant problem-solving and logical thinking skills in Python.

### Core Functionalities
1. __Daily Logic Challenges__:
   * Suggests 1-3 problems per day depending on the user's pace. (Only 1 problem per interaction).
   * Problems progress in difficulty (loops -> nested logic -> pattern recognition -> small projects)
   * Provides problem description, key concept focus, example input/output.
3. __Hint System__:
   * Offers gradual hints if the user is stuck.
     * Hint 1: Conceptual nudge
     * Hint 2: Logic step guidance
     * Hint 3: Pseudocode skeleton
   * Never gives the full solution unless explicitly requested.
5. __Code Review__:
   * User pastes their code; GPT provides feedback on:
     * Logic flow & clarity
     * Use of loops, conditionals, variables
     * Suggestions for cleaner or more efficient code
   * Encourages reflection: “What did you learn from this problem? Could you approach it differently next time?”
7. __Mini Puzzles__:
   * Occasionally throws small logical puzzles or challenges unrelated to Python syntax to train raw reasoning.
9. __Progress Tracking__:
    * Keeps track of which problem types you’ve solved (counting, pattern, recursion, string logic).
    * Gives motivational feedback like: “You’ve solved 8 counting problems and your loops are strong — ready for nested loops next!”

# System Prompt
You are LogicSmith, an expert Python mentor and logic coach. Your role is to help the user build strong independent problem-solving skills in Python, focusing on logical thinking, flow control, loops, conditionals, data structures, and algorithmic patterns.



Your personality is:

- Friendly, patient, and encouraging

- Slightly playful to keep motivation high

- Always focused on developing the user’s thinking, not just giving answers



Your core responsibilities:



1. **Daily / On-Demand Logic Challenges**

   - Suggest structured problems from beginner to intermediate difficulty, in phases:

     - Phase 1: Foundations (loops, conditionals, lists, strings)

     - Phase 2: Applied Logic (nested loops, functions, pattern recognition)

     - Phase 3: Problem-Solving Flow (easy LeetCode-style problems)

   - For each problem, provide:

     - Problem description

     - Expected input/output examples

     - Key concepts being practiced

     - Hints (stepwise, from conceptual to pseudocode)

   - Only give full solutions if the user explicitly asks.



2. **Hints System**

   - Provide hints in stages:

     - Hint 1: Conceptual nudge

     - Hint 2: Closer logic clue

     - Hint 3: Pseudocode skeleton

   - Never give full code unless asked.



3. **Code Review**

   - Evaluate user’s code for:

     - Correctness of logic

     - Clarity and structure

     - Use of proper programming patterns

   - Provide suggestions for cleaner or more efficient approaches.

   - Encourage reflection: “What did you learn here? Could you approach it differently next time?”



4. **Mini Puzzles / Stretch Tasks**

   - Occasionally offer small logic puzzles unrelated to Python syntax to strengthen raw reasoning skills.



5. **Progress Tracking & Feedback**

   - Keep track of problem types the user has solved (loops, counting, patterns, recursion, strings, etc.)

   - Provide motivational feedback and recommendations for next problem(s)

   - Celebrate milestones (e.g., completing 5 problems without hints, mastering a pattern, etc.)



6. **Teaching Philosophy**

   - Always ask the user to **explain their thought process in plain English** before coding.

   - Encourage stepwise thinking: break problems into sub-problems, use pseudocode, then code.

   - Avoid rushing; the goal is understanding and logic-building, not just finishing tasks.



**Interaction Style:**

- Ask the user their current confidence level before suggesting a problem.

- Suggest problems in increasing difficulty.

- Give incremental hints only when requested.

- Evaluate code and provide reflective questions.

- Keep explanations clear, structured, and supportive.



---



**Example Interaction Flow:**



**User:** “Give me a Phase 1 Day 2 problem.”  

**LogicSmith GPT:**  

> ✅ Sign Checker  

> Input a number, print whether it’s positive, negative, or zero.  

> Key concepts: Conditionals, flow control  

> Hint 1: Think about splitting possibilities into three groups  

> Hint 2: Use if…elif…else  

> Hint 3: Pseudocode:  

> ``` 

> Read number  

> If number > 0: print "positive"  

> Else if number < 0: print "negative"  

> Else: print "zero"

> ```  



**User:** “Here’s my code. Any improvements?”  

**LogicSmith:**  

- Reviews code for correctness and clarity  

- Suggests cleaner or more efficient logic  

- Encourages reflection and pattern recognition



---



Your job as LogicSmith GPT is to **mentor, challenge, and guide** the user to think like a programmer while keeping the experience motivating and enjoyable.



# Problem Set

## Phase 1: 

---



### Day 1 — Odd Number Printer



**Problem:**  

Print all odd numbers from 1 to 100 without using `if x % 2 != 0`.  



**Key Concept:**  

Loops + sequence logic  



**Example Output:**  

```

1 3 5 7 ... 99

```



**Hints:**  

- **Hint 1:** Odd numbers start at 1 and increase by 2 each time.  

- **Hint 2:** Use `range(start, stop, step)` or a `while` loop.  

- **Hint 3 (Pseudocode):**  

```

number = 1

while number <= 100:

    print(number, end=" ")

    number += 2

```



---



### Day 2 — Sign Checker



**Problem:**  

Input a number and print whether it is positive, negative, or zero.  



**Key Concept:**  

Conditional logic  



**Example Input/Output:**  

```

Input: -5 → Output: Negative

Input: 0 → Output: Zero

Input: 7 → Output: Positive

```



**Hints:**  

- **Hint 1:** Think of three categories: >0, <0, =0  

- **Hint 2:** Use `if…elif…else` statements  

- **Hint 3 (Pseudocode):**  

```

num = int(input("Enter a number: "))

if num > 0:

    print("Positive")

elif num < 0:

    print("Negative")

else:

    print("Zero")

```



---



### Day 3 — Vowel Counter



**Problem:**  

Count the number of vowels in a string.  



**Key Concept:**  

Strings + loops + conditions  



**Example Input/Output:**  

```

Input: "Aristo AI" → Output: 4

```



**Hints:**  

- **Hint 1:** Define a string of vowels: `"aeiouAEIOU"`  

- **Hint 2:** Loop through each character and check if it’s a vowel  

- **Hint 3:** Use a counter variable to accumulate the total  



**Pseudocode:**  

```

text = input("Enter a string: ")

vowels = "aeiouAEIOU"

count = 0

for char in text:

    if char in vowels:

        count += 1

print("Number of vowels:", count)

```



---



### Day 4 — Manual Max-Min



**Problem:**  

Find the largest and smallest numbers in a list without using `max()` or `min()`.  



**Key Concept:**  

Loop comparison + tracking values  



**Example Input/Output:**  

```

Input: [3, 7, 2, 9] → Output: Max: 9, Min: 2

```



**Hints:**  

- **Hint 1:** Start by assuming the first element is both max and min  

- **Hint 2:** Loop through the list, updating max or min when needed  

- **Hint 3:** Print results after the loop  



**Pseudocode:**  

```

nums = [3, 7, 2, 9]

max_num = nums[0]

min_num = nums[0]



for n in nums:

    if n > max_num:

        max_num = n

    if n < min_num:

        min_num = n



print("Max:", max_num)

print("Min:", min_num)

```



---



### Day 5 — Fibonacci Series



**Problem:**  

Print the first `n` terms of the Fibonacci sequence.  



**Key Concept:**  

Sequential logic + variable updates  



**Example Input/Output (n=7):**  

```

0 1 1 2 3 5 8

```



**Hints:**  

- **Hint 1:** Start with two variables `a=0`, `b=1`  

- **Hint 2:** Next term = `a + b`  

- **Hint 3:** Update `a = b`, `b = next_term` each iteration  



**Pseudocode:**  

```

n = 7

a, b = 0, 1

for _ in range(n):

    print(a, end=" ")

    a, b = b, a + b

```



---



### Day 6 — Number Pyramid



**Problem:**  

Print a numeric triangle pattern.  



**Key Concept:**  

Nested loops + pattern generation  



**Example Output (n=4):**  

```

1

1 2

1 2 3

1 2 3 4

```



**Hints:**  

- **Hint 1:** Outer loop handles rows, inner loop prints numbers in each row  

- **Hint 2:** Use `end=" "` in print for same line  

- **Hint 3:** After inner loop, print a newline  



**Pseudocode:**  

```

n = 4

for i in range(1, n+1):

    for j in range(1, i+1):

        print(j, end=" ")

    print()

```



---



### Day 7 — Digit Sum



**Problem:**  

Input a number and output the sum of its digits.  



**Key Concept:**  

Integer manipulation + loops  



**Example Input/Output:**  

```

Input: 753 → Output: 15

```



**Hints:**  

- **Hint 1:** Convert number to string and iterate OR use `% 10` and `// 10`  

- **Hint 2:** Keep a running total  

- **Hint 3:** Stop when number reaches 0  



**Pseudocode:**  

```

num = int(input("Enter a number: "))

total = 0

while num > 0:

    total += num % 10

    num //= 10

print("Sum of digits:", total)

```



---



### Day 8 — Character Frequency



**Problem:**  

Count frequency of each character in a string.  



**Key Concept:**  

Dictionaries + loops  



**Example Input/Output:**  

```

Input: "banana" → Output: {'b':1, 'a':3, 'n':2}

```



**Hints:**  

- **Hint 1:** Initialize empty dict: `freq = {}`  

- **Hint 2:** Loop through each char: add 1 if exists, else initialize  

- **Hint 3:** Print dictionary after loop  



**Pseudocode:**  

```

text = "banana"

freq = {}

for char in text:

    if char in freq:

        freq[char] += 1

    else:

        freq[char] = 1

print(freq)

```



---



### Day 9 — Manual Reverse



**Problem:**  

Reverse a list manually (no slicing `[::-1]`, no `.reverse()`)  



**Key Concept:**  

Index manipulation + loops  



**Example Input/Output:**  

```

Input: [1,2,3] → Output: [3,2,1]

```



**Hints:**  

- **Hint 1:** Create empty list `reversed_list`  

- **Hint 2:** Loop from last index to first (`range(len(list)-1, -1, -1)`)  

- **Hint 3:** Append each element to `reversed_list`  



**Pseudocode:**  

```

lst = [1, 2, 3]

reversed_list = []

for i in range(len(lst)-1, -1, -1):

    reversed_list.append(lst[i])

print(reversed_list)

```



---



### Day 10 — Number Guessing Game



**Problem:**  

Computer picks a number 1–50; user keeps guessing until correct.  



**Key Concept:**  

Loops + conditionals + random  



**Example Flow:**  

```

I'm thinking of a number between 1 and 50

Guess: 20 → Too low!

Guess: 37 → Too high!

Guess: 32 → Correct! You guessed in 3 tries

```



**Hints:**  

- **Hint 1:** Import `random` and use `random.randint(1,50)`  

- **Hint 2:** Keep a guess counter  

- **Hint 3:** Use while loop until `user_guess == target`  

- **Hint 4:** Give feedback (too high / too low) inside loop  



**Pseudocode:**  

```

import random

target = random.randint(1, 50)

guess = 0

attempts = 0

while guess != target:

    guess = int(input("Enter your guess: "))

    attempts += 1

    if guess < target:

        print("Too low!")

    elif guess > target:

        print("Too high!")

print(f"Correct! You guessed in {attempts} tries.")

```

## Phase 2:

### Day 11 — Functions: Prime Checker



**Problem:**  

Write a function to check if a number is prime.  



**Key Concept:**  

Functions + Loops + Conditionals  



**Example Input/Output:**  

```

Input: 7 → Output: True

Input: 8 → Output: False

```



**Hints:**  

- **Hint 1:** A prime number is greater than 1 and divisible only by 1 and itself.  

- **Hint 2:** Loop from 2 to sqrt(n) to check divisibility.  

- **Hint 3 (Function):**  

```

def is_prime(n):

    if n < 2:

        return False

    for i in range(2, int(n**0.5)+1):

        if n % i == 0:

            return False

    return True

```



---



### Day 12 — Lists + Conditions: Remove Duplicates



**Problem:**  

Remove duplicates from a list without using `set()`.  



**Key Concept:**  

Lists + Conditionals  



**Example Input/Output:**  

```

Input: [1,2,2,3,1] → Output: [1,2,3]

```



**Hints:**  

- **Hint 1:** Create a new list and add elements only if not already present.  

- **Hint 2:** Loop through the original list.  

- **Hint 3 (Function):**  

```

def remove_duplicates(lst):

    result = []

    for item in lst:

        if item not in result:

            result.append(item)

    return result

```



---



### Day 13 — Strings + Loops: Palindrome Checker



**Problem:**  

Check if a string is a palindrome.  



**Key Concept:**  

Strings + Loops  



**Example Input/Output:**  

```

Input: "racecar" → Output: True

Input: "hello" → Output: False

```



**Hints:**  

- **Hint 1:** Compare the string to its reverse.  

- **Hint 2:** Can use slicing `s[::-1]` or loop from ends to middle.  

- **Hint 3 (Function):**  

```

def is_palindrome(s):

    return s == s[::-1]

```



---



### Day 14 — Searching: Linear Search



**Problem:**  

Implement linear search manually.  



**Key Concept:**  

Loops + Conditionals  



**Example Input/Output:**  

```

Input: lst=[3,5,2], target=5 → Output: Index 1

Input: lst=[3,5,2], target=7 → Output: Not found

```



**Hints:**  

- **Hint 1:** Loop through each element and compare with target.  

- **Hint 2:** Return index when found; otherwise indicate not found.  

- **Hint 3 (Function):**  

```

def linear_search(lst, target):

    for i, val in enumerate(lst):

        if val == target:

            return i

    return -1  # not found

```



---



### Day 15 — Sorting: Bubble Sort



**Problem:**  

Implement bubble sort manually.  



**Key Concept:**  

Nested Loops + Swapping  



**Example Input/Output:**  

```

Input: [5,2,4,1] → Output: [1,2,4,5]

```



**Hints:**  

- **Hint 1:** Compare adjacent elements and swap if out of order.  

- **Hint 2:** Repeat for n-1 passes.  

- **Hint 3 (Function):**  

```

def bubble_sort(lst):

    n = len(lst)

    for i in range(n):

        for j in range(0, n-i-1):

            if lst[j] > lst[j+1]:

                lst[j], lst[j+1] = lst[j+1], lst[j]

    return lst

```



---



### Day 16 — Dictionaries: Word Frequency



**Problem:**  

Count word frequency in a sentence.  



**Key Concept:**  

Dictionaries + Loops  



**Example Input/Output:**  

```

Input: "hello world hello" → Output: {'hello':2, 'world':1}

```



**Hints:**  

- **Hint 1:** Split sentence into words.  

- **Hint 2:** Use a dictionary to count occurrences.  

- **Hint 3 (Function):**  

```

def word_frequency(sentence):

    freq = {}

    for word in sentence.split():

        if word in freq:

            freq[word] += 1

        else:

            freq[word] = 1

    return freq

```



---



### Day 17 — Nested Structures: Sum Even Numbers



**Problem:**  

Sum all even numbers inside a nested list.  



**Key Concept:**  

Nested Loops + Conditionals  



**Example Input/Output:**  

```

Input: [[1,2],[3,4,6]] → Output: 12

```



**Hints:**  

- **Hint 1:** Loop through outer list, then inner lists.  

- **Hint 2:** Check if element is even before adding.  

- **Hint 3 (Function):**  

```

def sum_even_nested(lst):

    total = 0

    for sublist in lst:

        for num in sublist:

            if num % 2 == 0:

                total += num

    return total

```



---



### Day 18 — Logical Patterns: nth Fibonacci Number



**Problem:**  

Build a function that returns the nth Fibonacci number.  



**Key Concept:**  

Loops + Function + Sequential Logic  



**Example Input/Output:**  

```

Input: 7 → Output: 8

```



**Hints:**  

- **Hint 1:** Start with first two numbers: 0,1  

- **Hint 2:** Use a loop to generate up to nth term  

- **Hint 3 (Function):**  

```

def fibonacci(n):

    a, b = 0, 1

    for _ in range(n-1):

        a, b = b, a+b

    return a

```



---



### Day 19 — Problem Breakdown: Anagram Checker



**Problem:**  

Write a program to check if two strings are anagrams.  



**Key Concept:**  

Strings + Sorting + Comparison  



**Example Input/Output:**  

```

Input: "listen", "silent" → Output: True

Input: "hello", "world" → Output: False

```



**Hints:**  

- **Hint 1:** Two strings are anagrams if sorted letters match.  

- **Hint 2:** Can also count letters using dictionary.  

- **Hint 3 (Function):**  

```

def are_anagrams(s1, s2):

    return sorted(s1) == sorted(s2)

```



---



### Day 20 — Mini Project: Basic Calculator



**Problem:**  

Build a basic calculator using functions.  



**Key Concept:**  

Functions + Conditionals + User Input  



**Example Input/Output:**  

```

Enter first number: 5

Enter operation (+,-,*,/): *

Enter second number: 4

Output: 20

```



**Hints:**  

- **Hint 1:** Define functions for add, subtract, multiply, divide  

- **Hint 2:** Take user input for operation and numbers  

- **Hint 3 (Function skeleton):**  

```

def add(a,b): return a+b

def subtract(a,b): return a-b

def multiply(a,b): return a*b

def divide(a,b): return a/b



a = float(input("Enter first number: "))

op = input("Enter operation (+,-,*,/): ")

b = float(input("Enter second number: "))



if op == '+':

    print(add(a,b))

elif op == '-':

    print(subtract(a,b))

elif op == '*':

    print(multiply(a,b))

elif op == '/':

    print(divide(a,b))

else:

    print("Invalid operation")

```



## Phase 3:

### Day 21 — Arrays: Maximum Product of Two Numbers



**Problem:**  

Find the maximum product of two numbers in a list.  



**Key Concept:**  

Arrays + Loops + Comparison  



**Example Input/Output:**  

```

Input: [3, 5, -2, 8] → Output: 40 (5*8)

```



**Hints:**  

- **Hint 1:** Consider all pairs of numbers.  

- **Hint 2:** Keep track of the maximum product while iterating.  

- **Hint 3 (Pseudocode):**  

```

def max_product(lst):

    max_prod = float('-inf')

    for i in range(len(lst)):

        for j in range(i+1, len(lst)):

            max_prod = max(max_prod, lst[i]*lst[j])

    return max_prod

```



---



### Day 22 — Strings: First Non-Repeating Character



**Problem:**  

Return the first non-repeating character in a string.  



**Key Concept:**  

Strings + Dictionaries  



**Example Input/Output:**  

```

Input: "swiss" → Output: "w"

```



**Hints:**  

- **Hint 1:** Count frequency of each character using a dictionary.  

- **Hint 2:** Iterate through the string and return the first with count 1.  

- **Hint 3 (Pseudocode):**  

```

def first_non_repeating(s):

    freq = {}

    for char in s:

        freq[char] = freq.get(char,0)+1

    for char in s:

        if freq[char] == 1:

            return char

    return None

```



---



### Day 23 — Math Logic: Armstrong Number



**Problem:**  

Determine if a number is an Armstrong number.  



**Key Concept:**  

Math Logic + Loops  



**Example Input/Output:**  

```

Input: 153 → Output: True (1^3 + 5^3 + 3^3 = 153)

Input: 123 → Output: False

```



**Hints:**  

- **Hint 1:** Calculate the number of digits `n`.  

- **Hint 2:** Sum each digit raised to `n`.  

- **Hint 3 (Function):**  

```

def is_armstrong(num):

    digits = [int(d) for d in str(num)]

    n = len(digits)

    total = sum(d**n for d in digits)

    return total == num

```



---



### Day 24 — Two-Pointer Technique: Pair Sum



**Problem:**  

Check if a list has a pair summing to a target.  



**Key Concept:**  

Two-Pointer Technique + Sorting  



**Example Input/Output:**  

```

Input: [1,3,5,7], target=8 → Output: True (1+7 or 3+5)

```



**Hints:**  

- **Hint 1:** Sort the list.  

- **Hint 2:** Use two pointers, one at start and one at end.  

- **Hint 3 (Function):**  

```

def has_pair_sum(lst, target):

    lst.sort()

    left, right = 0, len(lst)-1

    while left < right:

        s = lst[left]+lst[right]

        if s == target:

            return True

        elif s < target:

            left += 1

        else:

            right -= 1

    return False

```



---



### Day 25 — Hash Maps: Duplicate Element



**Problem:**  

Find if any element appears twice in an array.  



**Key Concept:**  

Hash Maps / Dictionaries  



**Example Input/Output:**  

```

Input: [1,2,3,4,2] → Output: True

Input: [1,2,3] → Output: False

```



**Hints:**  

- **Hint 1:** Use a dictionary or set to track seen elements.  

- **Hint 2:** If an element is already seen, return True.  

- **Hint 3 (Function):**  

```

def has_duplicate(lst):

    seen = set()

    for num in lst:

        if num in seen:

            return True

        seen.add(num)

    return False

```



---



### Day 26 — Sliding Window: Longest Substring Without Repeating Characters



**Problem:**  

Find the length of the longest substring without repeating characters.  



**Key Concept:**  

Sliding Window + Hash Maps  



**Example Input/Output:**  

```

Input: "abcabcbb" → Output: 3 ("abc")

```



**Hints:**  

- **Hint 1:** Use two pointers to maintain a window of unique characters.  

- **Hint 2:** Use a dictionary to track last seen indices.  

- **Hint 3 (Function):**  

```

def longest_unique_substring(s):

    char_index = {}

    start = max_len = 0

    for i, c in enumerate(s):

        if c in char_index and char_index[c] >= start:

            start = char_index[c] + 1

        char_index[c] = i

        max_len = max(max_len, i-start+1)

    return max_len

```



---



### Day 27 — Recursion: Factorial



**Problem:**  

Find factorial recursively.  



**Key Concept:**  

Recursion + Base Case  



**Example Input/Output:**  

```

Input: 5 → Output: 120

```



**Hints:**  

- **Hint 1:** Base case: factorial(0) = 1  

- **Hint 2:** Recursive case: n * factorial(n-1)  

- **Hint 3 (Function):**  

```

def factorial(n):

    if n == 0:

        return 1

    return n * factorial(n-1)

```



---



### Day 28 — Edge Cases: Input Validation



**Problem:**  

Handle empty inputs or invalid data for any of the above problems.  



**Key Concept:**  

Input Validation + Error Handling  



**Example Hints:**  

- **Hint 1:** Check if input list or string is empty before processing.  

- **Hint 2:** Use try/except to handle invalid input types.  

- **Hint 3 (Example):**  

```

def safe_factorial(n):

    if not isinstance(n, int) or n < 0:

        return "Invalid input"

    if n == 0:

        return 1

    return n * safe_factorial(n-1)

```



---



### Day 29 — Review: Re-solve Hardest Problems



**Problem:**  

Re-solve your hardest 3 problems from above without looking up code.  



**Key Concept:**  

Practice + Memory Recall  



**Hints:**  

- **Hint 1:** Focus on logic rather than syntax.  

- **Hint 2:** Try to write pseudocode first.  

- **Hint 3:** Test each solution with multiple examples.



---



### Day 30 — LeetCode Launch: Easy Problems



**Problem:**  

Solve 2 easy LeetCode problems:  

1. **Two Sum**  

2. **Valid Parentheses**  



**Key Concept:**  

Problem Solving + Arrays/Stacks  



**Hints for Two Sum:**  

- Use a dictionary to store visited numbers and their indices.  

- Check if `target - num` exists in dictionary while iterating.  



**Hints for Valid Parentheses:**  

- Use a stack to push opening brackets.  

- Pop and check matching closing brackets.  

- Ensure stack is empty at the end.  



**Example Pseudocode (Two Sum):**  

```

def two_sum(nums, target):

    seen = {}

    for i, num in enumerate(nums):

        if target-num in seen:

            return [seen[target-num], i]

        seen[num] = i

```



**Example Pseudocode (Valid Parentheses):**  

```

def is_valid(s):

    stack = []

    mapping = {')':'(', '}':'{', ']':'['}

    for char in s:

        if char in mapping.values():

            stack.append(char)

        elif char in mapping.keys():

            if not stack or stack[-1] != mapping[char]:

                return False

            stack.pop()

    return not stack

```

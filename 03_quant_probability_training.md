# Module 3: Probability & Counting

## 1. Permutation & Combination

1. In how many different ways can the letters of the word 'LEADING' be arranged in such a way that the vowels always come together?
A) 360
B) 480
C) 720
D) 5040

**Answer:** Option **C**

**Explanation:**
The word 'LEADING' has 7 letters, including 3 vowels (E, A, I) and 4 consonants (L, D, N, G).
Consider the 3 vowels as one letter.
Then, we have 4 consonants + 1 vowel-block = 5 letters.
These 5 letters can be arranged in 5! = 120 ways.
The 3 vowels can be arranged among themselves in 3! = 6 ways.
Total number of ways = (120 x 6) = 720.

2. Out of 7 consonants and 4 vowels, how many words of 3 consonants and 2 vowels can be formed?
A) 210
B) 1050
C) 25200
D) 21400

**Answer:** Option **C**

**Explanation:**
Number of ways of selecting 3 consonants from 7 = 7C3 = 35.
Number of ways of selecting 2 vowels from 4 = 4C2 = 6.
Number of ways of selecting the letters = (35 x 6) = 210.
Each of these 5 letters can be arranged among themselves in 5! ways = 120 ways.
Total number of words formed = (210 x 120) = 25200.

3. How many 3-digit numbers can be formed from the digits 2, 3, 5, 6, 7 and 9, which are divisible by 5 and none of the digits is repeated?
A) 5
B) 10
C) 15
D) 20

**Answer:** Option **D**

**Explanation:**
Since each desired number is divisible by 5, so we must have 5 at the unit place. So, there is 1 way of doing it.
The tens place can now be filled by any of the remaining 5 digits (5 ways).
The hundreds place can now be filled by any of the remaining 4 digits (4 ways).
Required number of numbers = (1 x 5 x 4) = 20.

4. In a group of 6 boys and 4 girls, four children are to be selected. In how many different ways can they be selected such that at least one boy should be there?
A) 159
B) 194
C) 205
D) 209

**Answer:** Option **D**

**Explanation:**
We may have (1 boy and 3 girls) or (2 boys and 2 girls) or (3 boys and 1 girl) or (4 boys).
Total number of ways = (6C1 x 4C3) + (6C2 x 4C2) + (6C3 x 4C1) + (6C4)
= (6 x 4) + (15 x 6) + (20 x 4) + 15
= 24 + 90 + 80 + 15
= 209.
Alternatively: Total selections (10C4) - Selections with 0 boys (4C4) = 210 - 1 = 209.

5. A box contains 2 white balls, 3 black balls and 4 red balls. In how many ways can 3 balls be drawn from the box, if at least one black ball is to be included in the draw?
A) 32
B) 48
C) 64
D) 96

**Answer:** Option **C**

**Explanation:**
Total number of ways of drawing 3 balls from 9 = 9C3 = 84.
Number of ways of drawing 3 balls out of which none is black = 6C3 = 20.
Number of ways of drawing 3 balls containing at least one black ball = (84 - 20) = 64.

---

## 2. Probability

1. Two dice are thrown simultaneously. What is the probability of getting two numbers whose product is even?
A) 1/2
B) 3/4
C) 3/8
D) 5/16

**Answer:** Option **B**

**Explanation:**
Total number of possible outcomes = 6 x 6 = 36.
The product is odd only when both numbers are odd.
There are 3 odd numbers on each die.
Number of outcomes where product is odd = 3 x 3 = 9.
Probability of odd product = 9/36 = 1/4.
Probability of even product = 1 - 1/4 = 3/4.

2. In a lottery, there are 10 prizes and 25 blanks. A lottery is drawn at random. What is the probability of getting a prize?
A) 1/10
B) 2/5
C) 2/7
D) 5/7

**Answer:** Option **C**

**Explanation:**
Total number of outcomes = 10 + 25 = 35.
Number of favorable outcomes (getting a prize) = 10.
Probability = Favorable Outcomes / Total Outcomes
P(Prize) = 10 / 35 = 2/7.

3. From a pack of 52 cards, two cards are drawn together at random. What is the probability of both the cards being kings?
A) 1/15
B) 25/57
C) 35/256
D) 1/221

**Answer:** Option **D**

**Explanation:**
Let S be the sample space.
n(S) = 52C2 = (52 x 51) / (2 x 1) = 1326.
Let E = event of getting 2 kings out of 4.
n(E) = 4C2 = (4 x 3) / (2 x 1) = 6.
P(E) = n(E) / n(S) = 6 / 1326 = 1/221.

4. One card is drawn at random from a pack of 52 cards. What is the probability that the card drawn is a face card (Jack, Queen and King only)?
A) 1/13
B) 3/13
C) 1/4
D) 9/52

**Answer:** Option **B**

**Explanation:**
In a deck of 52 cards, there are 4 suits.
Each suit has 3 face cards (Jack, Queen, King).
Total face cards = 4 x 3 = 12.
Probability of drawing a face card = 12 / 52 = 3/13.

5. A bag contains 4 white, 5 red and 6 blue balls. Three balls are drawn at random from the bag. The probability that all of them are red, is:
A) 1/22
B) 3/22
C) 2/91
D) 2/77

**Answer:** Option **C**

**Explanation:**
Let S be the sample space.
n(S) = 15C3 = (15 x 14 x 13) / (3 x 2 x 1) = 455.
Let E = event of getting 3 red balls out of 5.
n(E) = 5C3 = (5 x 4 x 3) / (3 x 2 x 1) = 10.
P(E) = n(E) / n(S) = 10 / 455 = 2/91.

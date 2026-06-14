# Training Module 3: Probability & Counting Techniques

## 1. Permutation & Combination

**Q1. In how many different ways can the letters of the word 'LEADING' be arranged in such a way that the vowels always come together?**

**Solution:**
*   **Step 1:** Identify vowels and consonants in 'LEADING' (7 letters).
    Vowels: E, A, I (3)
    Consonants: L, D, N, G (4)
*   **Step 2:** Group the vowels together as one single unit since they must always sit together.
    Unit = (EAI).
*   **Step 3:** Arrange this new set of units.
    We have 4 consonants + 1 vowel unit = 5 units total.
    These 5 units can be arranged in $5!$ ways $= 120$ ways.
*   **Step 4:** Arrange the vowels internally.
    Inside the (EAI) unit, the 3 vowels can scramble among themselves in $3!$ ways $= 6$ ways.
*   **Step 5:** Multiply for total permutations.
    Total ways $= 120 \times 6 = 720$.
*   **Final Answer:** 720.

**Q2. Out of 7 consonants and 4 vowels, how many words of 3 consonants and 2 vowels can be formed?**

**Solution:**
*   **Step 1:** Select 3 consonants out of 7. (Selection = Combination)
    $^7C_3 = \frac{7 \times 6 \times 5}{3 \times 2 \times 1} = 35$ ways.
*   **Step 2:** Select 2 vowels out of 4.
    $^4C_2 = \frac{4 \times 3}{2 \times 1} = 6$ ways.
*   **Step 3:** Multiply to find total ways to *select* the group.
    $35 \times 6 = 210$ combinations of letters.
*   **Step 4:** Form words by arranging them.
    Each combination gives you 5 letters. These 5 letters can be arranged in $5! = 120$ ways.
*   **Step 5:** Find total words.
    Total words = $210 \text{ (selections)} \times 120 \text{ (arrangements)} = 25200$.
*   **Final Answer:** 25200.

**Q3. How many 3-digit numbers can be formed from the digits 2, 3, 5, 6, 7 and 9, which are divisible by 5 and none of the digits is repeated?**

**Solution:**
*   **Step 1:** For a number to be divisible by 5, the unit's digit must be 5 or 0. Since we only have '5', the unit's place is fixed.
    Unit's place = 1 way (only digit '5').
*   **Step 2:** Since repetition is not allowed, we have 5 digits left (2, 3, 6, 7, 9) to fill the remaining two spots.
*   **Step 3:** Fill the Hundred's place.
    Any of the remaining 5 digits can be placed here = 5 ways.
*   **Step 4:** Fill the Ten's place.
    Any of the remaining 4 digits can be placed here = 4 ways.
*   **Step 5:** Multiply the possibilities.
    $1 \times 5 \times 4 = 20$.
*   **Final Answer:** 20.

**Q4. In a group of 6 boys and 4 girls, four children are to be selected. In how many different ways can they be selected such that at least one boy should be there?**

**Solution:**
*   **Step 1:** The trick for "at least one" is to calculate Total Ways minus Ways with NONE.
    At least one boy = Total selections - Selections with NO boys (only girls).
*   **Step 2:** Calculate total unrestricted selections (choose 4 from 10).
    $^{10}C_4 = \frac{10 \times 9 \times 8 \times 7}{4 \times 3 \times 2 \times 1} = 210$.
*   **Step 3:** Calculate selections with NO boys.
    This means we select 4 children entirely from the 4 girls.
    $^4C_4 = 1$.
*   **Step 4:** Subtract.
    $210 - 1 = 209$.
*   **Final Answer:** 209.

**Q5. A box contains 2 white balls, 3 black balls and 4 red balls. In how many ways can 3 balls be drawn from the box, if at least one black ball is to be included in the draw?**

**Solution:**
*   **Step 1:** Again, use the "at least one" trick.
    At least one black = Total ways to draw 3 - Ways to draw 3 with NO black balls.
*   **Step 2:** Calculate total unrestricted draws (choose 3 from 9).
    $^9C_3 = \frac{9 \times 8 \times 7}{3 \times 2 \times 1} = 84$.
*   **Step 3:** Calculate draws with NO black balls.
    If we draw no black balls, we must draw our 3 balls from the remaining 6 (2 white + 4 red).
    $^6C_3 = \frac{6 \times 5 \times 4}{3 \times 2 \times 1} = 20$.
*   **Step 4:** Subtract.
    $84 - 20 = 64$.
*   **Final Answer:** 64.

---

## 2. Probability

**Q1. Two dice are thrown simultaneously. What is the probability of getting two numbers whose product is even?**

**Solution:**
*   **Step 1:** Understand the condition. The product of two numbers is even if AT LEAST one of them is even. The product is odd ONLY when BOTH numbers are odd.
*   **Step 2:** Calculate total outcomes.
    $6 \times 6 = 36$ outcomes.
*   **Step 3:** Calculate the probability of the opposite (Product is odd).
    Probability of odd on 1st die = 3/6 = 1/2
    Probability of odd on 2nd die = 3/6 = 1/2
    Probability(Odd AND Odd) = $\frac{1}{2} \times \frac{1}{2} = \frac{1}{4}$.
*   **Step 4:** Subtract from 1 to find the probability of an even product.
    P(Even product) = $1 - \text{P(Odd product)} = 1 - \frac{1}{4} = \frac{3}{4}$.
*   **Final Answer:** 3/4.

**Q2. In a lottery, there are 10 prizes and 25 blanks. A lottery is drawn at random. What is the probability of getting a prize?**

**Solution:**
*   **Step 1:** Find total number of tickets.
    Total = $10 \text{ (prizes)} + 25 \text{ (blanks)} = 35$ tickets.
*   **Step 2:** Find the number of favorable outcomes (winning a prize).
    Favorable = 10.
*   **Step 3:** Calculate probability.
    Probability = $\frac{\text{Favorable}}{\text{Total}} = \frac{10}{35}$.
*   **Step 4:** Simplify the fraction.
    $\frac{10}{35} = \frac{2}{7}$.
*   **Final Answer:** 2/7.

**Q3. From a pack of 52 cards, two cards are drawn together at random. What is the probability of both the cards being kings?**

**Solution:**
*   **Step 1:** Calculate total ways to draw 2 cards from 52.
    $^{52}C_2 = \frac{52 \times 51}{2 \times 1} = 1326$.
*   **Step 2:** Calculate ways to draw 2 kings from the 4 available kings.
    $^4C_2 = \frac{4 \times 3}{2 \times 1} = 6$.
*   **Step 3:** Calculate the probability.
    Probability = $\frac{\text{Favorable draws}}{\text{Total draws}} = \frac{6}{1326}$.
*   **Step 4:** Simplify.
    $\frac{6}{1326} = \frac{1}{221}$.
*   **Final Answer:** 1/221.

**Q4. One card is drawn at random from a pack of 52 cards. What is the probability that the card drawn is a face card (Jack, Queen and King only)?**

**Solution:**
*   **Step 1:** Identify total face cards in a deck.
    Each suit has 3 face cards (J, Q, K).
    There are 4 suits (Hearts, Diamonds, Clubs, Spades).
    Total face cards = $4 \times 3 = 12$.
*   **Step 2:** Calculate probability.
    Probability = $\frac{12}{52}$.
*   **Step 3:** Simplify.
    Divide both by 4: $\frac{3}{13}$.
*   **Final Answer:** 3/13.

**Q5. A bag contains 4 white, 5 red and 6 blue balls. Three balls are drawn at random from the bag. The probability that all of them are red, is:**

**Solution:**
*   **Step 1:** Calculate total number of balls.
    $4 + 5 + 6 = 15$ balls.
*   **Step 2:** Calculate total ways to draw 3 balls from 15.
    $^{15}C_3 = \frac{15 \times 14 \times 13}{3 \times 2 \times 1} = 455$.
*   **Step 3:** Calculate ways to draw 3 red balls from the 5 available red balls.
    $^5C_3 = \frac{5 \times 4 \times 3}{3 \times 2 \times 1} = 10$.
*   **Step 4:** Calculate the probability.
    Probability = $\frac{10}{455}$.
*   **Step 5:** Simplify.
    Divide both by 5: $\frac{2}{91}$.
*   **Final Answer:** 2/91.

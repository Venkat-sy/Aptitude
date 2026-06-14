# Training Module 3: Probability & Counting Techniques

## 1. Permutation & Combination

**Q1. In how many different ways can the letters of the word 'LEADING' be arranged in such a way that the vowels always come together?**
> **Solution:** The word 'LEADING' has 7 letters, with vowels (E, A, I) and consonants (L, D, N, G).
> Treat vowels as one unit: (EAI). We now have 5 items to arrange: (EAI), L, D, N, G.
> They can be arranged in 5! = 120 ways.
> The vowels inside the unit can be arranged in 3! = 6 ways.
> Total ways = 120 * 6 = 720.

**Q2. Out of 7 consonants and 4 vowels, how many words of 3 consonants and 2 vowels can be formed?**
> **Solution:** Number of ways of selecting 3 consonants = $^7C_3 = (7*6*5)/(3*2*1) = 35$.
> Number of ways of selecting 2 vowels = $^4C_2 = (4*3)/(2*1) = 6$.
> Number of ways of selecting the group = $35 * 6 = 210$.
> Once chosen, these 5 letters can be arranged among themselves in 5! ways = 120.
> Total words = 210 * 120 = 25200.

**Q3. How many 3-digit numbers can be formed from the digits 2, 3, 5, 6, 7 and 9, which are divisible by 5 and none of the digits is repeated?**
> **Solution:** For a number to be divisible by 5, it must end with 5.
> Unit's place is fixed with '5' (1 way).
> Hundreds place can be filled by any of the remaining 5 digits (5 ways).
> Tens place can be filled by any of the remaining 4 digits (4 ways).
> Total ways = 1 * 5 * 4 = 20.

**Q4. In a group of 6 boys and 4 girls, four children are to be selected. In how many different ways can they be selected such that at least one boy should be there?**
> **Solution:** Total ways to select 4 children = $^{10}C_4 = (10*9*8*7)/(4*3*2*1) = 210$.
> Ways to select ONLY girls (no boys) = $^4C_4 = 1$.
> Ways with at least one boy = Total - (No boys) = 210 - 1 = 209.

**Q5. A box contains 2 white balls, 3 black balls and 4 red balls. In how many ways can 3 balls be drawn from the box, if at least one black ball is to be included in the draw?**
> **Solution:** Total ways to draw 3 balls = $^9C_3 = (9*8*7)/(3*2*1) = 84$.
> Ways to draw no black balls (i.e. draw from remaining 6) = $^6C_3 = (6*5*4)/(3*2*1) = 20$.
> Ways with at least one black = 84 - 20 = 64.

---

## 2. Probability

**Q1. Two dice are thrown simultaneously. What is the probability of getting two numbers whose product is even?**
> **Solution:** Total outcomes = 6 * 6 = 36.
> Product is odd ONLY if both numbers are odd.
> Probability of odd * odd = (3/6) * (3/6) = 1/4 = 9/36.
> Probability of even product = 1 - P(odd product) = 1 - 1/4 = 3/4.

**Q2. In a lottery, there are 10 prizes and 25 blanks. A lottery is drawn at random. What is the probability of getting a prize?**
> **Solution:** Total tickets = 10 + 25 = 35.
> Total prizes = 10.
> Probability = 10 / 35 = 2/7.

**Q3. From a pack of 52 cards, two cards are drawn together at random. What is the probability of both the cards being kings?**
> **Solution:** Total ways to draw 2 cards = $^{52}C_2 = (52 * 51) / 2 = 1326$.
> Ways to draw 2 kings = $^4C_2 = (4 * 3) / 2 = 6$.
> Probability = 6 / 1326 = 1 / 221.

**Q4. One card is drawn at random from a pack of 52 cards. What is the probability that the card drawn is a face card (Jack, Queen and King only)?**
> **Solution:** Total face cards = 3 per suit * 4 suits = 12.
> Total cards = 52.
> Probability = 12 / 52 = 3 / 13.

**Q5. A bag contains 4 white, 5 red and 6 blue balls. Three balls are drawn at random from the bag. The probability that all of them are red, is:**
> **Solution:** Total balls = 15. Total draws = $^{15}C_3 = (15*14*13)/(3*2) = 455$.
> Favorable draws (all red) = $^5C_3 = (5*4*3)/(3*2) = 10$.
> Probability = 10 / 455 = 2 / 91.

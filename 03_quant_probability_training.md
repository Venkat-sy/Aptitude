# Module 3: Probability & Counting

## 1. Permutation & Combination
**Q1. 'LEADING', arrange with vowels always together:**
**Sol:**
Vowels(EAI) = 1 unit
Consonants(LDNG) = 4 units
Total = 5 units
Arrangement of units = $5! = 120$
Internal arrangement of vowels = $3! = 6$
Total ways = $120 \times 6 = 720$

**Q2. 7 consonants, 4 vowels. Words with 3C, 2V?**
**Sol:**
Select Consonants = $^7C_3 = 35$
Select Vowels = $^4C_2 = 6$
Total selections = $35 \times 6 = 210$
Arrange the 5 letters = $5! = 120$
Total words = $210 \times 120 = 25200$

**Q3. 3-digit numbers from 2,3,5,6,7,9 div by 5. No repeat.**
**Sol:**
Unit's place (ends in 5) = $1$ way
Hundred's place (remaining 5) = $5$ ways
Ten's place (remaining 4) = $4$ ways
Total = $1 \times 5 \times 4 = 20$

**Q4. 6 boys, 4 girls. Select 4 children, at least 1 boy.**
**Sol:**
Total selections = $^{10}C_4 = 210$
Selections with NO boys (only girls) = $^4C_4 = 1$
At least 1 boy = Total - NoBoys
$= 210 - 1 = 209$

**Q5. 2W, 3B, 4R balls. Draw 3, at least 1 black.**
**Sol:**
Total draws = $^9C_3 = 84$
Draws with NO black balls (from the other 6) = $^6C_3 = 20$
At least 1 black = Total - NoBlack
$= 84 - 20 = 64$

---
## 2. Probability
**Q1. Two dice. Prob(Product is even):**
**Sol:**
Total outcomes = $36$
Prob(Odd on 1st) = $1/2$
Prob(Odd on 2nd) = $1/2$
P(Odd Product) = $1/2 \times 1/2 = 1/4$
P(Even Product) = $1 - 1/4 = 3/4$

**Q2. 10 prizes, 25 blanks. P(Prize) = ?**
**Sol:**
Total tickets = $35$
Prizes = $10$
P = $10 / 35 = 2/7$

**Q3. 52 cards, draw 2. Both kings:**
**Sol:**
Ways to draw 2 Kings = $^4C_2 = 6$
Ways to draw 2 cards = $^{52}C_2 = 1326$
P = $6 / 1326 = 1/221$

**Q4. 1 card drawn. Face card (J,Q,K) prob:**
**Sol:**
Face cards per suit = $3$
Total face cards = $3 \times 4 = 12$
P = $12 / 52 = 3/13$

**Q5. 4W, 5R, 6B balls. Draw 3. All red prob:**
**Sol:**
Total balls = $15$
Ways to draw 3 Red = $^5C_3 = 10$
Ways to draw 3 balls = $^{15}C_3 = 455$
P = $10 / 455 = 2/91$

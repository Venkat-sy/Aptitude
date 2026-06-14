# Module 3: Probability & Counting

## 1. Permutation & Combination
**Q1. 'LEADING', arrange with vowels always together:**
**Sol:** Vowels(EAI) = 1 unit. Consonants(LDNG) = 4. Total 5 units. $5! = 120$. Vowels internal = $3! = 6$. Total = $120*6 = 720$.

**Q2. 7 consonants, 4 vowels. Words with 3C, 2V?**
**Sol:** Select: $^7C_3 * ^4C_2 = 35 * 6 = 210$. Arrange 5 letters: $5! = 120$. Total = $210 * 120 = 25200$.

**Q3. 3-digit numbers from 2,3,5,6,7,9 div by 5. No repeat.**
**Sol:** Ends in 5 (1 way). Hundreds (5 ways). Tens (4 ways). Total = $1*5*4 = 20$.

**Q4. 6 boys, 4 girls. Select 4 children, at least 1 boy.**
**Sol:** Total($^{10}C_4$) - NoBoys($^4C_4$) = $210 - 1 = 209$.

**Q5. 2W, 3B, 4R balls. Draw 3, at least 1 black.**
**Sol:** Total($^9C_3$) - NoBlack($^6C_3$) = $84 - 20 = 64$.

---
## 2. Probability
**Q1. Two dice. Prob(Product is even):**
**Sol:** $1 - P(Odd*Odd) = 1 - (1/2 * 1/2) = 1 - 1/4 = 3/4$.

**Q2. 10 prizes, 25 blanks. P(Prize) = ?**
**Sol:** Total = 35. P = $10/35 = 2/7$.

**Q3. 52 cards, draw 2. Both kings:**
**Sol:** $^4C_2 / ^{52}C_2 = 6 / 1326 = 1/221$.

**Q4. 1 card drawn. Face card (J,Q,K) prob:**
**Sol:** 12 face cards. P = $12/52 = 3/13$.

**Q5. 4W, 5R, 6B balls. Draw 3. All red prob:**
**Sol:** Total = 15. $P = ^5C_3 / ^{15}C_3 = 10 / 455 = 2/91$.

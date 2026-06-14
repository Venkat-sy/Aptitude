# Module 4: Logical Reasoning

## 1. Number Series & Coding
**Q1. 1, 9, 25, 49, 81, ?**
**Sol:**
Pattern: Squares of consecutive odd numbers
$1 = 1^2$
$9 = 3^2$
$25 = 5^2$
$49 = 7^2$
$81 = 9^2$
Next base = $11$
$Next = 11^2 = 121$

**Q2. 2, 5, 9, 19, 37, ?**
**Sol:**
Pattern: Alternating $(\times 2 + 1)$ and $(\times 2 - 1)$
$2 \times 2 + 1 = 5$
$5 \times 2 - 1 = 9$
$9 \times 2 + 1 = 19$
$19 \times 2 - 1 = 37$
$Next = (37 \times 2) + 1$
$Next = 74 + 1 = 75$

**Q3. MADRAS -> NBESBT. BOMBAY -> ?**
**Sol:**
Pattern: $+1$ to each letter
$M \rightarrow N$
$A \rightarrow B$
$D \rightarrow E$
Therefore:
$B \rightarrow C$
$O \rightarrow P$
$M \rightarrow N$
Result = CPNCBZ

**Q4. Z = 52, ACT = 48. BAT = ?**
**Sol:**
Rule: $(\text{Alphabet Position}) \times 2$
$Z = 26 \times 2 = 52$
$ACT = (1 + 3 + 20) \times 2 = 24 \times 2 = 48$
$BAT = (2 + 1 + 20) \times 2$
$= 23 \times 2$
$= 46$

**Q5. 15789 -> EGKPT, 2346 -> ALUR. 23549 -> ?**
**Sol:**
Direct Substitution:
$2 \rightarrow A$
$3 \rightarrow L$
$5 \rightarrow G$
$4 \rightarrow U$
$9 \rightarrow T$
Result = ALGUT

---
## 2. Blood Relations & Direction
**Q1. "He is the son of the only son of my mother" (Suresh).**
**Sol:**
"Only son of my mother" = Suresh
Substitute back:
"He is the son of Suresh"
Therefore, Suresh is the Father.

**Q2. Man to lady: "Your mother's husband's sister is my aunt."**
**Sol:**
Lady's "mother's husband" = Lady's Father
His "sister" = Lady's Aunt
Lady's Aunt = Man's Aunt
They share an aunt, so they are siblings.
Relationship = Sister.

**Q3. Walk 5km South, Right turn (West) 3km, Left turn (South) 5km. Dir?**
**Sol:**
Initial = $0,0$
Walk 1 = $5\text{km South}$
Turn Right = $\text{Facing West}$
Walk 2 = $3\text{km West}$
Turn Left = $\text{Facing South}$
Walk 3 = $5\text{km South}$
Total South = $5 + 5 = 10\text{km}$
Total West = $3\text{km}$
Direction = South-West

**Q4. 6 PM hour hand points North. Minute hand at 9:15 PM?**
**Sol:**
Normal 6 PM = Hour hand points South
Given 6 PM = North
Clock is rotated $180^\circ$
Normal 9:15 = Minute hand points East (at the 3)
Rotated $180^\circ$ = West

**Q5. Circle: R, T, V, U, W, S, Q, P.**
**Sol:**
Constraints:
1. $T$ next to $R$ and $V \Rightarrow R-T-V$
2. $P$ is 2nd right of $T \Rightarrow R-T-V-\text{blank}-P$
3. $V$ next to $U \Rightarrow \text{blank is } U \Rightarrow R-T-V-U-P$
Remaining spots filled by constraints.
Final Clockwise = $R, T, V, U, W, S, Q, P$

---
## 3. Syllogisms
**Q1. All dogs are cats. Some cats are rats.**
**Sol:**
Dogs inside Cats.
Rats overlap Cats.
I. Some dogs are rats (False, overlap not guaranteed)
II. No dog is rat (False, separation not guaranteed)
Ans: Either I or II (Complementary pair)

**Q2. Some buildings are chalks. No chalk is toffee.**
**Sol:**
Buildings overlap Chalks.
Toffees separate from Chalks.
I. No building is toffee (False, toffee can touch non-chalk building)
II. All chalks are buildings (False)
Ans: Neither I nor II

**Q3. All windows are doors. No door is a wall.**
**Sol:**
Windows inside Doors.
Walls separate from Doors.
I. Some windows are walls (False, walls can't enter doors)
II. No wall is a door (True, direct reverse)
Ans: Only II follows

**Q4. Some papers are pens. All pencils are pens.**
**Sol:**
Pencils inside Pens.
Papers overlap Pens.
I. Some pens are pencils (True, if all P are p)
II. Some pens are papers (True, reverse overlap)
Ans: Both I and II

**Q5. All buses are cars. All ships are cars.**
**Sol:**
Buses inside Cars.
Ships inside Cars.
I. All cars are ships (False, Cars is the bigger set)
II. All buses are ships (False, no guaranteed overlap)
Ans: Neither I nor II

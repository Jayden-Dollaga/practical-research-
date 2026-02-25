# 🧠 STATISTICS & LINEAR REGRESSION — Detailed Exam Reviewer

---

## 1 — Core idea (quick)

Linear regression models how a dependent variable **y** changes with an independent variable **x** using a straight line:
$$
\boxed{y = bx + a}
$$

* **b** = slope (change in **y** per 1 unit change in **x**)
* **a** = y-intercept (predicted **y** when **x = 0**)
  Units matter: if (y) is ₱ and (x) is m², then **b** is ₱/m² and **a** is ₱.

---

## 2 — Interpreting slope & intercept

* **Slope (b)**: positive → y increases as x increases; negative → y decreases as x increases.
  Example: $(b=10{,}500)$ means **each extra 1 m² adds ₱10,500** to cost.
* **Intercept (a)**: predicted value at $(x=0)$. Sometimes it’s not realistic (e.g., cost for zero area), but always include it in calculations unless model says otherwise.

---

## 3 — Two most common tasks (worked)

### A. Predict y (plug-in)

Given $(y = 10{,}500x + 125{,}000)$. Find cost for $(x=75)$ m².

1. Multiply: $(10{,}500 \times 75 = 787{,}500)$.
2. Add intercept: $(787{,}500 + 125{,}000 = 912{,}500)$.
   **Answer:** ₱912,500.00. (Show units & 2 decimals in exams.)

### B. Solve for x (given y)

If you have ₱1,000,000, how many m² can you build?
$$
1{,}000{,}000 = 10{,}500x + 125{,}000
$$

1. Isolate: $(1{,}000{,}000 - 125{,}000 = 10{,}500x) → (875{,}000 = 10{,}500x)$.
2. Divide: $(x = \dfrac{875{,}000}{10{,}500} = 83.333\ldots )$ → **83.33 m²** (round sensibly).
   **Tip:** Keep enough digits during calc, round at the end.

---

## 4 — How to compute slope **b** from raw data (must-memorize formula)

Given n pairs $((x_i,y_i))$, use:
$$
\boxed{b = \dfrac{n\sum XY - (\sum X)(\sum Y)}{,n\sum X^2 - (\sum X)^2,}}
$$

Then compute intercept:
$$
\boxed{a = \bar{Y} - b\bar{X}} \quad\text{(where }\bar{X}=\tfrac{\sum X}{n},\ \bar{Y}=\tfrac{\sum Y}{n}\text{)}
$$

**Step-by-step compute b from a table**

1. Make columns: (X), (Y), (XY), (X^2).
2. Sum each column: $(\sum X,\ \sum Y,\ \sum XY,\ \sum X^2)$.
3. Plug sums into the (b) formula.
4. Compute (a) using $(\bar{X},\bar{Y})$.

---

## 5 — Extra formulas to know (short list)

* **Line:** $(y = bx + a)$ or $(y = mx + c)$ (same idea)
* **Intercept via sums:** $(a = \dfrac{\sum Y - b\sum X}{n}) (equivalent to (\bar{Y}-b\bar{X}))$
* **Correlation coefficient (sample r):**
  $$
  r = \dfrac{n\sum XY - (\sum X)(\sum Y)}{\sqrt{ \big(n\sum X^2 - (\sum X)^2\big)\big(n\sum Y^2 - (\sum Y)^2\big) }}
  $$
* **Coefficient of determination:** (R^2 = r^2) (proportion of variance explained)

(You may not need to derive r on an exam, but know what it means: |r| close to 1 → strong linear relationship.)

---

## 6 — Interpreting results (what examiners love)

* State slope with units and meaning: *“Slope = 10,500 ₱/m², meaning each additional square meter adds ₱10,500 to predicted cost.”*
* Mention intercept plausibility: *“Intercept = ₱125,000 (predicted base cost at 0 m²) — may be a fixed fee or a modeling artifact; interpret carefully.”*
* When solving for x, round to sensible decimal places and keep units.

---

## 7 — Common pitfalls & exam tips

* **Units:** Always write units (₱, m², days, marks).
* **Order of operations:** Multiply before add.
* **Rounding:** Don’t round intermediate steps too early. Round final result to 2 decimals for currency, 2 decimal places for area unless told otherwise.
* **Check plausibility:** If x or y becomes negative, note it and explain why that’s unrealistic.
* **Show work:** Examiners expect algebraic steps (isolate, divide).
* **Label answers:** “Answer: 83.33 m²” — never just the number.

---

## 8 — Short worked example (absence → grade)

If the model for math grade is $(y = -2x + 94)$ where (x)=number of absences and (y)=grade:

* Interpret slope: each absence reduces predicted grade by 2 points.
* To find max absences to still get grade 80: set (y=80):
  $$
  80 = -2x + 94 \Rightarrow -2x = -14 \Rightarrow x = 7.
  $$
  **Answer:** 7 absences.
  *(This matches the example answer in your reviewer.)* 

---

## 9 — Practice problems (do these and check answers)

1. Given $(y = 800x + 50{,}000)$. Predict (y) when $(x=120)$
   **Answer:** $(y = 800(120)+50{,}000=96{,}000+50{,}000=146{,}000)$.

2. If $(y = 6x + 70)$ and you want $(y=100)$, find (x).
   **Answer:** $(100 = 6x + 70 \Rightarrow 6x = 30 \Rightarrow x=5)$.

3. From raw data: $n=4$, $(\sum X=20), (\sum Y=56), (\sum XY=312), (\sum X^2=132)$. Compute **b**.
   $$
   b=\dfrac{4(312)-20(56)}{4(132)-(20)^2}=\dfrac{1248-1120}{528-400}=\dfrac{128}{128}=1
   $$
   **Answer:** $(b=1)$.

4. For the cost model $(y=10{,}500x+125{,}000)$, what is the predicted cost for 0 m² and is it realistic?
   **Answer:** ₱125,000. Realism: It might be a fixed base fee or non-meaningful if model is extrapolated.

5. If correlation $r = 0.92$, what is $(R^2)$? Interpret.
   **Answer:** $(R^2 = 0.8464)$ → about 84.64% of variance in y explained by x.

---

## 10 — One-page cram sheet (copy to exam sheet)

* Slope formula: $(b=\dfrac{n\sum XY - (\sum X)(\sum Y)}{n\sum X^2 - (\sum X)^2})$
* Intercept: $a = \bar{Y} - b\bar{X}) or (a = \dfrac{\sum Y - b\sum X}{n})$
* Units: slope units = $(units of y)/(units of x)$
* Solve for x: $(x = \dfrac{y-a}{b}) (if (b\neq 0))$
* r formula (memorize if needed) and $(R^2 = r^2)$
* Tips: units, show algebra, round last step, check realism
Bet. Let’s do a full **step-by-step regression computation** using an actual raw dataset — the way it would appear in an exam.

---

# 🧮 Example Raw Data

Suppose we are given:

| X (Hours Studied) | Y (Exam Score) |
| ----------------- | -------------- |
| 2                 | 65             |
| 4                 | 70             |
| 6                 | 75             |
| 8                 | 85             |

We will compute:

* ✅ Slope (**b**)
* ✅ Intercept (**a**)
* ✅ Correlation coefficient $**r**)
* ✅ Final regression equation

---

# STEP 1 — Create Required Columns

We must compute:

* (XY)
* (X^2)
* (Y^2)

| X | Y  | XY  | X² | Y²   |
| - | -- | --- | -- | ---- |
| 2 | 65 | 130 | 4  | 4225 |
| 4 | 70 | 280 | 16 | 4900 |
| 6 | 75 | 450 | 36 | 5625 |
| 8 | 85 | 680 | 64 | 7225 |

---

# STEP 2 — Get the Summations

$$
\sum X = 2+4+6+8 = 20
$$

$$
\sum Y = 65+70+75+85 = 295
$$

$$
\sum XY = 130+280+450+680 = 1540
$$

$$
\sum X^2 = 4+16+36+64 = 120
$$

$$
\sum Y^2 = 4225+4900+5625+7225 = 21975
$$

$$
n = 4
$$

---

# STEP 3 — Compute the Slope (b)

Formula:

$$
b = \frac{n\sum XY - (\sum X)(\sum Y)}{n\sum X^2 - (\sum X)^2}
$$

Substitute values:

Numerator:
$$
4(1540) - (20)(295)
$$

$$
6160 - 5900 = 260
$$

Denominator:
$$
4(120) - (20)^2
$$

$$
480 - 400 = 80
$$

Now divide:

$$
b = \frac{260}{80} = 3.25
$$

✅ **Slope = 3.25**

Meaning: Each additional study hour increases score by **3.25 points**.

---

# STEP 4 — Compute the Intercept (a)

Formula:

$$
a = \bar{Y} - b\bar{X}
$$

First find means:

$$
\bar{X} = \frac{20}{4} = 5
$$

$$
\bar{Y} = \frac{295}{4} = 73.75
$$

Now substitute:

$$
a = 73.75 - (3.25)(5)
$$

$$
a = 73.75 - 16.25
$$

$$
a = 57.5
$$

✅ **Intercept = 57.5**

---

# STEP 5 — Final Regression Equation

$$
\boxed{y = 3.25x + 57.5}
$$

---

# STEP 6 — Compute Correlation Coefficient (r)

Formula:

$$
r = \frac{n\sum XY - (\sum X)(\sum Y)}{\sqrt{(n\sum X^2 - (\sum X)^2)(n\sum Y^2 - (\sum Y)^2)}}
$$

We already know numerator = **260**

Now compute second bracket:

$$
n\sum Y^2 - (\sum Y)^2
$$

$$
4(21975) - (295)^2
$$

$$
87900 - 87025 = 875
$$

Now multiply denominators:

$$
(80)(875) = 70000
$$

Square root:

$$
\sqrt{70000} ≈ 264.58
$$

Now divide:

$$
r = \frac{260}{264.58}
$$

$$
r ≈ 0.983
$$

---

# FINAL RESULTS

* **b = 3.25**
* **a = 57.5**
* **Regression equation:**
  $$
  y = 3.25x + 57.5
  $$
* **r ≈ 0.983**

---

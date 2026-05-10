# Bell Test Setup & Mathematical Thresholds

This guide builds upon the practical setup by providing the explicit mathematical framework required to calculate the thresholds for **Local Realism (Bell's Limit)** and **Quantum Mechanics (Tsirelson's Bound)**.

---

## 1. The Experimental Variables
In a standard CHSH (Clauser-Horne-Shimony-Holt) Bell test, you measure two particles (A and B).
* Alice chooses between two detector settings (angles): $a$ or $a'$.
* Bob chooses between two detector settings (angles): $b$ or $b'$.
* Each measurement results in a binary outcome: $+1$ (detection at the 'transmitted' port) or $-1$ (detection at the 'reflected' port).

## 2. Calculating the Correlation Coefficient $E(	heta_A, 	heta_B)$
For any pair of settings $(	heta_A, 	heta_B)$, you must calculate the expectation value. This is done by counting coincidences ($N$) at the four possible detector output combinations:
* $N(+,+)$ : Both detectors fire in the $+1$ path.
* $N(-,-)$ : Both detectors fire in the $-1$ path.
* $N(+,-)$ : Alice is $+1$, Bob is $-1$.
* $N(-,+)$ : Alice is $-1$, Bob is $+1$.

The correlation coefficient $E$ is calculated as:
$$E(	heta_A, 	heta_B) = rac{N(+,+) + N(-,-) - N(+,-) - N(-,+)}{N(+,+) + N(-,-) + N(+,-) + N(-,+)}$$

## 3. Manual Calculation of the CHSH Statistic ($S$)
Once you have the four coefficients for the four setting pairs, calculate the $S$ value:
$$S = E(a, b) - E(a, b') + E(a', b) + E(a', b')$$

---

## 4. Threshold 1: The Local Realism Limit ($S \leq 2$)
To understand why the threshold is 2, consider a "Hidden Variable" theory where the results are predetermined.

**Mathematical Proof:**
Suppose for any measurement, the result is a fixed value $A(a), A(a'), B(b), B(b') \in \{+1, -1\}$.
The CHSH expression is:
$$S = A(a)B(b) - A(a)B(b') + A(a')B(b) + A(a')B(b')$$
Factorize the terms:
$$S = A(a)[B(b) - B(b')] + A(a')[B(b) + B(b')]$$

Since $B(b)$ and $B(b')$ are either $+1$ or $-1$:
* If $B(b) = B(b')$, then $[B(b) - B(b')] = 0$ and $[B(b) + B(b')] = \pm 2$.
* If $B(b) 
eq B(b')$, then $[B(b) - B(b')] = \pm 2$ and $[B(b) + B(b')] = 0$.

In either case, one term becomes 0 and the other becomes $\pm 2$. Multiplying by $A = \pm 1$ keeps the result at $\pm 2$. Therefore, for any local hidden variable theory:
$$|S| \leq 2$$

---

## 5. Threshold 2: The Quantum Limit ($S = 2\sqrt{2}$)
Quantum mechanics predicts the correlation for entangled photons depends on the difference in angles: $E(	heta_A, 	heta_B) = -\cos(2(	heta_A - 	heta_B))$.

To maximize $S$, we choose the **Bell Angles**:
* $a = 0^\circ$
* $a' = 45^\circ$
* $b = 22.5^\circ$
* $b' = -22.5^\circ$

**Calculation:**
1.  $E(a, b) = \cos(2(0 - 22.5)) = \cos(-45^\circ) = 1/\sqrt{2}$
2.  $E(a, b') = \cos(2(0 - (-22.5))) = \cos(45^\circ) = 1/\sqrt{2}$
3.  $E(a', b) = \cos(2(45 - 22.5)) = \cos(45^\circ) = 1/\sqrt{2}$
4.  $E(a', b') = \cos(2(45 - (-22.5))) = \cos(135^\circ) = -1/\sqrt{2}$

Plug these into the $S$ formula:
$$S = (1/\sqrt{2}) - (-1/\sqrt{2}) + (1/\sqrt{2}) + (1/\sqrt{2})$$
$$S = 4/\sqrt{2} = 2\sqrt{2}  pprox 2.828$$

This value, $2\sqrt{2}$, is known as **Tsirelson's Bound**, the maximum violation allowed by quantum mechanics.

---

## 6. Practical Interpretation
* **Result < 2:** Your data is consistent with classical local realism (or your entanglement quality is poor).
* **Result > 2:** You have successfully demonstrated quantum non-locality. 
* **Result > 2.828:** Your math or your coincidence counting equipment is likely flawed, as this exceeds the physical limits of quantum mechanics.
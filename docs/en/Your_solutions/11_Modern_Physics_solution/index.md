**1. Determine whether each of the following function is one-to-one, onto or both. Derive the inverse function if it exists.**

**a. $f: \mathbf{R} \to \mathbf{R}, f(x) = -3x + 4$**
* **One-to-one:**
    $$f(x_1) = f(x_2)$$
    $$-3x_1 + 4 = -3x_2 + 4$$
    $$-3x_1 = -3x_2$$
    $$x_1 = x_2 \quad (\text{One-to-one})$$
* **Onto:**
    $$y = -3x + 4$$
    $$3x = 4 - y$$
    $$x = \frac{4 - y}{3} \in \mathbf{R} \quad (\text{Onto})$$
* **Both:** Yes.
* **Inverse:**
    $$y = -3x + 4 \implies x = \frac{4 - y}{3}$$
    $$f^{-1}(x) = \frac{4 - x}{3}$$

---

**b. $f: \mathbf{R} \to \mathbf{R}, f(x) = -3x^2 + 4$**
* **One-to-one:**
    $$f(1) = -3(1)^2 + 4 = 1$$
    $$f(-1) = -3(-1)^2 + 4 = 1$$
    $$f(1) = f(-1) \text{ and } 1 \neq -1 \quad (\text{Not one-to-one})$$
* **Onto:**
    $$y = 5 \in \mathbf{R}$$
    $$-3x^2 + 4 = 5 \implies -3x^2 = 1 \implies x^2 = -\frac{1}{3}$$
    $$x \notin \mathbf{R} \quad (\text{Not onto})$$
* **Both:** No.
* **Inverse:** Does not exist.

---

**c. $g: \mathbf{Z} \to \mathbf{Z}, g(n) = 2n$**
* **One-to-one:**
    $$g(n_1) = g(n_2)$$
    $$2n_1 = 2n_2$$
    $$n_1 = n_2 \quad (\text{One-to-one})$$
* **Onto:**
    $$y = 1 \in \mathbf{Z}$$
    $$2n = 1 \implies n = \frac{1}{2}$$
    $$\frac{1}{2} \notin \mathbf{Z} \quad (\text{Not onto})$$
* **Both:** No.
* **Inverse:** Does not exist.

---

**d. $f: \mathbf{Z} \to \mathbf{Z2}, f(n) = 2n$, where $\mathbf{Z2} = \{n \in \mathbf{Z} \mid \exists k \in \mathbf{Z}, n=2k\}$**
* **One-to-one:**
    $$f(n_1) = f(n_2)$$
    $$2n_1 = 2n_2$$
    $$n_1 = n_2 \quad (\text{One-to-one})$$
* **Onto:**
    $$\forall y \in \mathbf{Z2}, \exists k \in \mathbf{Z} \text{ such that } y = 2k$$
    $$f(k) = 2k = y$$
    $$k \in \mathbf{Z} \quad (\text{Onto})$$
* **Both:** Yes.
* **Inverse:**
    $$y = 2n \implies n = \frac{y}{2}$$
    $$f^{-1}(n) = \frac{n}{2}$$

---

**e. $F: P(A) \times P(B) \to P(A \cup B), F((X,Y)) = X \cup Y$, where $A=\{a,b\}, B=\{c,d\}$**
* **One-to-one:**
    $$A \cap B = \emptyset$$
    $$F((X_1, Y_1)) = F((X_2, Y_2)) \implies X_1 \cup Y_1 = X_2 \cup Y_2$$
    $$(X_1 \cup Y_1) \cap A = (X_2 \cup Y_2) \cap A \implies X_1 = X_2$$
    $$(X_1 \cup Y_1) \cap B = (X_2 \cup Y_2) \cap B \implies Y_1 = Y_2$$
    $$(X_1, Y_1) = (X_2, Y_2) \quad (\text{One-to-one})$$
* **Onto:**
    $$\forall Z \in P(A \cup B), Z = (Z \cap A) \cup (Z \cap B)$$
    $$X = Z \cap A \in P(A), \quad Y = Z \cap B \in P(B)$$
    $$F((X, Y)) = X \cup Y = Z \quad (\text{Onto})$$
* **Both:** Yes.
* **Inverse:**
    $$F^{-1}(Z) = (Z \cap A, Z \cap B)$$

---

**f. $N: \Sigma^* \to \mathbf{Z}^{\text{nonneg}}, N(s) = \text{the number of 1's in } s$, where $\Sigma=\{0,1\}$**
* **One-to-one:**
    $$s_1 = \text{"1"}, \quad s_2 = \text{"01"}$$
    $$N(s_1) = 1, \quad N(s_2) = 1$$
    $$N(s_1) = N(s_2) \text{ and } s_1 \neq s_2 \quad (\text{Not one-to-one})$$
* **Onto:**
    $$\forall k \in \mathbf{Z}^{\text{nonneg}}, \text{let } s = \underbrace{11\dots1}_{k \text{ times}}$$
    $$N(s) = k \quad (\text{Onto})$$
* **Both:** No.
* **Inverse:** Does not exist.

<br>

**2. Let $f: \mathbf{R} \to \mathbf{R}, f(x) = x^2 + 1$ and $g: \mathbf{R} \to \mathbf{R}, g(x) = x + 2$. Determine $g \circ f$, $f \circ g$, $f+g$, and $f \cdot g$.**

* **$g \circ f$**
    $$(g \circ f)(x) = g(f(x))$$
    $$g(x^2 + 1) = (x^2 + 1) + 2$$
    $$(g \circ f)(x) = x^2 + 3$$

* **$f \circ g$**
    $$(f \circ g)(x) = f(g(x))$$
    $$f(x + 2) = (x + 2)^2 + 1$$
    $$f(x + 2) = x^2 + 4x + 4 + 1$$
    $$(f \circ g)(x) = x^2 + 4x + 5$$

* **$f+g$**
    $$(f + g)(x) = f(x) + g(x)$$
    $$(f + g)(x) = (x^2 + 1) + (x + 2)$$
    $$(f + g)(x) = x^2 + x + 3$$

* **$f \cdot g$**
    $$(f \cdot g)(x) = f(x) \cdot g(x)$$
    $$(f \cdot g)(x) = (x^2 + 1)(x + 2)$$
    $$(f \cdot g)(x) = x^3 + 2x^2 + x + 2$$

<br>

**3. (a) If $f: \mathbf{R} \to \mathbf{R}$ and $g: \mathbf{R} \to \mathbf{R}$ are both bijections, is $f+g$ also a bijection? Why?**

* $$f(x) = x \quad (\text{Bijection})$$
    $$g(x) = -x \quad (\text{Bijection})$$
    $$(f + g)(x) = x + (-x) = 0$$
    $$(f + g)(1) = 0, \quad (f + g)(2) = 0$$
    $$(f + g)(1) = (f + g)(2) \text{ and } 1 \neq 2$$
    **No.**

<br>

**3. (b) If $f: \mathbf{R} \to \mathbf{R}$ is a function and $c \in \mathbf{R}-\{0\}$, the function $(c \cdot f): \mathbf{R} \to \mathbf{R}$ is defined by $(c \cdot f)(x) = c \cdot (f(x))$. If $f$ is a bijection, is $c \cdot f$ a bijection? Justify your answer.**

* **One-to-one:**
    $$(c \cdot f)(x_1) = (c \cdot f)(x_2)$$
    $$c \cdot f(x_1) = c \cdot f(x_2)$$
    $$f(x_1) = f(x_2) \quad (c \neq 0)$$
    $$x_1 = x_2 \quad (f \text{ is one-to-one})$$
* **Onto:**
    $$y \in \mathbf{R}$$
    $$f(x) = \frac{y}{c} \quad (c \neq 0 \text{ and } f \text{ is onto})$$
    $$(c \cdot f)(x) = c \cdot f(x) = c \cdot \left(\frac{y}{c}\right) = y$$
* **Conclusion:** **Yes.**

<br>

**4. If $f: X \to Y$ and $g: Y \to Z$ are both functions and $g \circ f$ is onto, must both $f$ and $g$ be onto? Prove or give a counterexample.**

* **$g$ Must be Onto:**
    $$\forall z \in Z, \exists x \in X \text{ such that } (g \circ f)(x) = z$$
    $$g(f(x)) = z$$
    $$\text{Let } y = f(x) \in Y. \text{ Then } g(y) = z.$$
* **$f$ Must NOT be Onto:**
    $$X = \{1\}, \quad Y = \{a, b\}, \quad Z = \{2\}$$
    $$f(1) = a \quad (\text{Not onto})$$
    $$g(a) = 2, \quad g(b) = 2 \quad (\text{Onto})$$
    $$(g \circ f)(1) = g(f(1)) = g(a) = 2 \quad (\text{Onto})$$
* **Conclusion:** **No.**

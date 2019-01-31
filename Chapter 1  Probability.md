## 1. Sample Space
(1) Finite
(2) Countable
(3) Uncountable

## 2. Event

## 3. Probability Set Function
Let $B = \{A_1, A_2, \cdots \}  $ 
(1) $P(A) \geq 0 $ for all $A \in B$
(2) $ P(S) = 1 $ 
(3) If $ A_1, A_2, \cdots, \in B$ (i.e. $A_i \cap A_j = \emptyset \hspace{0.5cm} \forall i \neq j )  $ are pairwise mutually exclusive, then $P(\cup_{i=1}^{\infty} A_i ) = \sum(A_i)$

## 4. Properties of p.s.f.
(1) $P(S) = 1$
(2) $P(\emptyset) = 0$
(3) $P(A) \leq 1$
(4) $P(A\cap B^c) = P(A) - P(A \cup B)$
(5) $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
(6) If $A \leq B$, then, $P(A) \leq P(B)$


## 5. Boole's Inequality
If $A_1, A_2, \cdots  $ is a sequence of events, then $$
P(\cup^\infty_{i=1}A_i) \leq \sum_{i=1}^{\infty} P(A_i)
$$

## 6. Conditional Probability
$$
 P(A|B) =  \frac {P(A \cap B)} {P(B)}
$$


## 7. Law of Total Probability

Let $B_1, B_2, \cdots B_n $ is a collection of mutually exclusive and exhaustive events (i.e $\sum^{n}_{i=1} B_i = S) \\$
Then $P(A) = \sum_{i=1}^{n} P(B_i)\cdot P(A|B_i) \\$



## 8. Bayes Theorem

Let $B_1, B_2, \cdots B_n $ is a collection of mutually exclusive and exhaustive events (i.e $\sum^{n}_{i=1} B_i = S) \\$
 Then 
 $$
 P(B_i|A) = \frac{P(B_i) \cdot P(A|B_i)} {\sum_{j=1}^{n}P(B_j)\cdot P(A|B_j)  }
 $$


## 9. Independent Events
$A$ and $B$are independent, then
$$
P(A|B) = P(A) \\
P(A \cup B) = P(A) \cdot P(B)
$$


## 10. Mutually Independent Events
Suppose $A_1,A_2,\cdots, A_n$ are events defined on $S$, 
for any $i_1, \cdots i_k$ from $1$ to $n$, we have
$$
  P(A_{i_1} \cup A_{i_2} \cup \cdots A_{i_k}) = P(A_{i_1})\cdot P(A_{i_2}) \cdots P(A_{i_k})
$$
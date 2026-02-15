\# 🧭 Closest Pair of Points — O(n²)



A clean implementation of the classical computational geometry problem:



> Given \*n\* points in 2D space, find the pair with the minimum Euclidean distance.



---



\## Why squared distance?



We compare squared distances instead of computing square roots:



d² = (x₂ - x₁)² + (y₂ - y₁)²





Since √x is monotonic, ordering is preserved and we avoid unnecessary `sqrt()` calls.



---



\## Algorithm (Naive Approach)



For `n` points:



\- iterate over all unique pairs

\- compute squared distance

\- track the minimum



Number of comparisons:



n(n - 1) / 2





Time complexity:



O(n²)





Space complexity:



O(1)





---



\## Example (used in this repo)



```python

points = \[(0, 0), (3, 4), (1, 1)]

Pairs evaluated:



(0,0) – (3,4) → 25



(0,0) – (1,1) → 2



(3,4) – (1,1) → 13



Result:



Closest pair: ((0, 0), (1, 1))

Squared distance: 2


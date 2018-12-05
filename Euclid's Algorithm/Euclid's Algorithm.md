# Euclid's Algorithm

__1. Greatest Common Divisor__

__2. Euclid's Algorithm__

__3. Extended Euclid__

__4. Solving Modular Linear Equations__

***



## Greatest Common Divisor

> of two integers 'a' and 'b', not both zero, is the largest of the common divisors of 'a' and 'b'; we denote it by gcd(a, b)

* The following are elementary properties of the gcd function:

  * gcd(a, b) = gcd(b, a)
  * gcd(a, b) = gcd(-a, b)
  * gcd(a, b) = gcd(|a|, |b|)
  * gcd(a, 0) = |a|
  * gcd (a, ka) = |a| for and k ∈ z

* GCD recursion theorem

  * For any nonnegative integer 'a' and any positive integer 'b',
  * gcd(a, b) = gcd(b, a mod b)
  * Proof

    *  If we let d = gcd(a, b), b then d|a and d|b.
    * a mod b = a - qb
    * Since 'a mod b' is thus a linear combination of 'a and b', gcd(a, b) | gcd(b, a mod b) implies that d| (a mode b)
    * Therefore, since d|b and d| (a mod b) equivalently that gcd(a, b) | gcd(b, a mod b)

* Greatest Common Divisor
  * want to compute gcd(a, b) where a ≥ 0 and b ≥ 0.
  * We exploit the following property of gcd:
    * gcd(a, b) = gcd(b, a mod b)
  * Examples
    * gcd(12, 15) = gcd(15, 12 mod 15) = gcd(15, 12)
    * gcd(15, 12) = gcd(12, 15 mod 12) = gcd(12, 3) = 3



<br>

## Euclid's Algorithm

``` java
Euclid(a, b)
    if b = 0 then
    	return a
    else
    	return Euclid(b, a mod b)
```

> Example:
>
> Euclid(30, 21) = Euclid(21, 30 mod 21) = Euclid(21, 9)
>
> Euclid(21, 9) = Euclid(9, 21 mod 9) = Euclid(9, 3)
>
> Euclid(9, 3) = Euclid(3, 9 mod 3) = Euclid(3, 0)
>
> Euclid(3, 0) = 3 (by. gcd(a, 0) = |a|)

* Correctness
  * Case: a = b → Euclid(a, b) calls Euclid(b, 0), returns b.
  * Case: a < b → Euclid(a, b) calls Euclid(b, a).
  * Case: a > b → Suppose d = gcd(a, b). If b = 0, then d = a.

<br>

## Extended Euclid

> If d = gcd(a, b) then d = ax + by for some integers x and y.
>
> Example:
>
> ​	gcd(30, 21) = 3
>
> ​	Consider (30 * 21) / 3 = 10 * 21 = 30 * 7 = 210

__Goal:__ Modify Euclid to return x and y.

``` java
Extended-Euclid(a, b)
    if b = 0 then
    	return (a, 1, 0)
    
    (d’, x’, y’) := Extended-Euclid(b, a mod b);
	(d, x, y) := (d’, y’, x’ - └a/b┘y’);
	return (d, x, y)
```

<br>

## Solving Modular Linear Equations

> Consider ax ≡ b(mod n). // it means 'ax mod n' = 'b mod n'
>
> Want to know all x's (mod n) that satisfy this equation.
>
> There may be zero, one, or more than one solution.

__Example 1:__ 

12x ≡ 6 (mod 15).   d = 3 = gcd(a, n) = gcd(12, 15) 

Corresponds to the solution x = 3. Also have x = 8 and x = 13 as solutions.

__Example 2:__ 

12x ≡ 3 (mod 14).  d = 2 = gcd(a , n) = gcd(12, 14)

No Solutions!

__Theorem:__

If b % d  = 0, then there are the solutions. If not, there is no solution.  


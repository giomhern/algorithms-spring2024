# March 18th, 2024

## Example: Fibonacci Numbers

F(n) = {
        0 if n = 0
        1 if n = 1
        F(n - 1) + F(n - 2)
    }

F(n) = F(n - 1) + F(n + 2) => F(n) >= 2F(n - 2) --> F(n) = omega(2^(n / 2))

F(n) = theta(n^2) => produces a lower and upper bound

HMW: F(n) = theta((1 + sqrt(5)/2)^n)

How many bits will we need to represent F(n)?

## Naive Recursive Algorithm

Input: Bit rep of in output

Output: Bit rep of F(n)

if n = 0, return 0

if n - 1, return 1

return fib(n - 1) + fib(n - 2)

## RT Analysis

Tn be the runtime of F(n)

Recurrent relation:

Tn = T(n-1) + T(n-2) +
    {
        theta(n) ~ bit complexity
        1 ~ any automatic operations (unit-cost)
    }

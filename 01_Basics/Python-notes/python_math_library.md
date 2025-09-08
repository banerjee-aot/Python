
# Python `math` Library – Complete Notes

The `math` module in Python provides access to mathematical constants, number theory, power, logarithmic, trigonometric, hyperbolic, and utility functions.  
This guide explains **all functions/constants** with **detailed notes and examples**.

---

## 📌 Importing the Library
```python
import math
```

---

## 🔹 Constants
| Constant | Explanation | Example |
|----------|-------------|---------|
| `math.pi` | Value of π (pi), ratio of circumference to diameter. | `print(math.pi)  # 3.141592653589793` |
| `math.e` | Euler’s number (base of natural log). | `print(math.e)  # 2.718281828459045` |
| `math.tau` | Tau constant (2π). | `print(math.tau)  # 6.283185307179586` |
| `math.inf` | Represents infinity. | `print(math.inf)  # inf` |
| `math.nan` | Not-a-Number (NaN). | `print(math.nan)  # nan` |

---

## 🔹 Number Theoretic Functions
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.ceil(x)` | Rounds `x` UP to nearest integer. | `math.ceil(4.3) → 5` |
| `math.floor(x)` | Rounds `x` DOWN to nearest integer. | `math.floor(4.7) → 4` |
| `math.trunc(x)` | Truncates decimal, keeps integer part. | `math.trunc(4.9) → 4` |
| `math.fabs(x)` | Absolute value (always positive). | `math.fabs(-7) → 7.0` |
| `math.factorial(n)` | Factorial `n!`. | `math.factorial(5) → 120` |
| `math.gcd(a,b)` | Greatest Common Divisor. | `math.gcd(24,36) → 12` |
| `math.lcm(a,b)` | Least Common Multiple. | `math.lcm(12,15) → 60` |

---

## 🔹 Power & Logarithmic Functions
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.exp(x)` | Returns `e^x`. | `math.exp(2) → 7.389` |
| `math.expm1(x)` | Returns `e^x - 1` (better precision for small `x`). | `math.expm1(2) → 6.389` |
| `math.log(x, base)` | Logarithm with custom base. | `math.log(8,2) → 3` |
| `math.log10(x)` | Base-10 logarithm. | `math.log10(1000) → 3` |
| `math.log2(x)` | Base-2 logarithm. | `math.log2(16) → 4` |
| `math.pow(x,y)` | Returns `x^y` (always float). | `math.pow(2,5) → 32.0` |
| `math.sqrt(x)` | Square root of `x`. | `math.sqrt(25) → 5.0` |

---

## 🔹 Trigonometric Functions
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.sin(x)` | Sine of angle (radians). | `math.sin(math.pi/2) → 1.0` |
| `math.cos(x)` | Cosine of angle (radians). | `math.cos(math.pi) → -1.0` |
| `math.tan(x)` | Tangent of angle (radians). | `math.tan(math.pi/4) → 1.0` |

### Inverse Trigonometric
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.asin(x)` | Inverse sine, returns angle in radians. | `math.asin(1) → 1.5708 (π/2)` |
| `math.acos(x)` | Inverse cosine. | `math.acos(0) → 1.5708 (π/2)` |
| `math.atan(x)` | Inverse tangent. | `math.atan(1) → 0.785 (π/4)` |
| `math.atan2(y,x)` | atan(y/x), safer than `atan`. | `math.atan2(1,1) → 0.785 (π/4)` |

---

## 🔹 Hyperbolic Functions
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.sinh(x)` | Hyperbolic sine. | `math.sinh(1) → 1.175` |
| `math.cosh(x)` | Hyperbolic cosine. | `math.cosh(1) → 1.543` |
| `math.tanh(x)` | Hyperbolic tangent. | `math.tanh(1) → 0.761` |
| `math.asinh(x)` | Inverse hyperbolic sine. | `math.asinh(1) → 0.881` |
| `math.acosh(x)` | Inverse hyperbolic cosine. | `math.acosh(2) → 1.316` |
| `math.atanh(x)` | Inverse hyperbolic tangent. | `math.atanh(0.5) → 0.549` |

---

## 🔹 Angle Conversions
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.degrees(x)` | Converts radians → degrees. | `math.degrees(math.pi) → 180.0` |
| `math.radians(x)` | Converts degrees → radians. | `math.radians(180) → 3.14159` |

---

## 🔹 Special Functions
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.erf(x)` | Error function. | `math.erf(1) → 0.8427` |
| `math.erfc(x)` | Complementary error function (1-erf(x)). | `math.erfc(1) → 0.1573` |
| `math.gamma(x)` | Gamma function, generalizes factorial. | `math.gamma(5) → 24.0` |
| `math.lgamma(x)` | Natural log of gamma function. | `math.lgamma(5) → 3.178` |

---

## 🔹 Floating Point Checks
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.isfinite(x)` | True if `x` not inf/nan. | `math.isfinite(10) → True` |
| `math.isinf(x)` | True if `x` is infinity. | `math.isinf(math.inf) → True` |
| `math.isnan(x)` | True if `x` is NaN. | `math.isnan(math.nan) → True` |
| `math.isclose(a,b)` | Compares floats within tolerance. | `math.isclose(0.1+0.2,0.3) → True` |

---

## 🔹 Rounding & Utility Functions
| Function | Explanation | Example |
|----------|-------------|---------|
| `math.modf(x)` | Returns `(fractional, integer)` parts. | `math.modf(5.25) → (0.25, 5.0)` |
| `math.copysign(x,y)` | Returns `x` with sign of `y`. | `math.copysign(5,-2) → -5.0` |
| `math.fmod(x,y)` | Floating-point modulo. | `math.fmod(7,3) → 1.0` |
| `math.remainder(x,y)` | IEEE remainder. | `math.remainder(7,3) → 1.0` |
| `math.prod(iterable)` | Product of iterable elements. | `math.prod([1,2,3,4]) → 24` |
| `math.dist(p,q)` | Euclidean distance between points. | `math.dist([0,0],[3,4]) → 5.0` |
| `math.hypot(x,y)` | sqrt(x²+y²). | `math.hypot(3,4) → 5.0` |
| `math.nextafter(x,y)` | Next float after `x` towards `y`. | `math.nextafter(1.0,2.0)` |
| `math.ulp(x)` | Spacing between `x` and next float. | `math.ulp(1.0) → 2.22e-16` |

---

# ✅ Summary Notes
- Use **constants** (`pi`, `e`, `tau`, `inf`, `nan`) for mathematical calculations.  
- **Number theory functions** help in rounding, factorial, gcd/lcm.  
- **Power & log functions** support exponentials and logarithms.  
- **Trigonometric & hyperbolic functions** use radians by default.  
- **Angle conversions** allow switching between degrees and radians.  
- **Special functions** (Gamma, erf) are useful in statistics/probability.  
- **Floating-point checks** (`isfinite`, `isnan`, `isclose`) are crucial for precision.  
- **Utility functions** like `dist`, `hypot`, `prod` help in geometry and sequences.  

---


```python
# ----------------------------
# Importing math library
# ----------------------------
import math

# ----------------------------
# Constants
# ----------------------------
print(math.pi)       # 3.141592653589793 (Value of π)
print(math.e)        # 2.718281828459045 (Euler’s number)
print(math.tau)      # 6.283185307179586 (Tau = 2π)
print(math.inf)      # Infinity
print(math.nan)      # Not a Number

# ----------------------------
# Number theoretic functions
# ----------------------------
print(math.ceil(4.3))     # 5 (rounds up)
print(math.floor(4.7))    # 4 (rounds down)
print(math.trunc(4.9))    # 4 (truncates decimal)
print(math.fabs(-7))      # 7.0 (absolute value)
print(math.factorial(5))  # 120 (5!)
print(math.gcd(24, 36))   # 12 (greatest common divisor)
print(math.lcm(12, 15))   # 60 (least common multiple)

# ----------------------------
# Power and logarithmic functions
# ----------------------------
print(math.exp(2))        # e^2
print(math.expm1(2))      # e^2 - 1
print(math.log(8, 2))     # log base 2 of 8 = 3
print(math.log10(1000))   # log base 10 of 1000 = 3
print(math.log2(16))      # log base 2 of 16 = 4
print(math.pow(2, 5))     # 32.0 (2^5)
print(math.sqrt(25))      # 5.0 (square root)

# ----------------------------
# Trigonometric functions
# ----------------------------
print(math.sin(math.pi/2))   # 1.0 (sin 90°)
print(math.cos(math.pi))     # -1.0 (cos 180°)
print(math.tan(math.pi/4))   # 1.0 (tan 45°)

# Inverse trigonometric
print(math.asin(1))          # π/2 radians
print(math.acos(0))          # π/2 radians
print(math.atan(1))          # π/4 radians
print(math.atan2(1, 1))      # atan2(y, x) = π/4

# Hyperbolic functions
print(math.sinh(1))          # sinh(1)
print(math.cosh(1))          # cosh(1)
print(math.tanh(1))          # tanh(1)
print(math.asinh(1))         # inverse sinh
print(math.acosh(2))         # inverse cosh
print(math.atanh(0.5))       # inverse tanh

# ----------------------------
# Angle conversion
# ----------------------------
print(math.degrees(math.pi))    # 180 degrees
print(math.radians(180))        # π radians

# ----------------------------
# Special functions
# ----------------------------
print(math.erf(1))        # Error function
print(math.erfc(1))       # Complementary error function
print(math.gamma(5))      # 24.0 (Gamma function, (n-1)!)
print(math.lgamma(5))     # ln(gamma(5))

# ----------------------------
# Floating point operations
# ----------------------------
print(math.isfinite(10))      # True
print(math.isinf(math.inf))   # True
print(math.isnan(math.nan))   # True
print(math.isclose(0.1+0.2, 0.3))  # True (floating comparison)

# ----------------------------
# Rounding functions
# ----------------------------
print(math.modf(5.25))     # (0.25, 5.0) → fractional, integer parts
print(math.copysign(5, -2))# -5.0 (copies sign from -2)
print(math.fmod(7, 3))     # 1.0 (floating-point modulo)
print(math.remainder(7, 3))# 1.0 (IEEE remainder)
print(math.prod([1, 2, 3, 4])) # 24 (product of iterable)
print(math.dist([0,0],[3,4]))  # 5.0 (Euclidean distance)

# ----------------------------
# Utility functions
# ----------------------------
print(math.hypot(3, 4))    # 5.0 (sqrt(x²+y²))
print(math.nextafter(1.0, 2.0)) # Next float after 1 towards 2
print(math.ulp(1.0))       # Distance between 1.0 and next float

```

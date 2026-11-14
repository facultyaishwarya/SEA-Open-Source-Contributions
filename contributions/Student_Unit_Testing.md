# Unit Testing Guide

**Unit testing** is a software testing method where developers test the smallest independent pieces of code, such as individual functions, methods, or classes, in isolation. Running automated checks early in the development cycle verifies that each component produces the expected output for a given input before integrating with the rest of the application.

## Table of Contents
- [Introduction to Unit Testing](#introduction-to-unit-testing)
- [Unit Testing Example](#unit-testing-example)
- [Advantages of Unit Testing](#advantages-of-unit-testing)
- [Conclusion](#conclusion)

---

## Introduction to Unit Testing
Unit testing forms the foundation of the software testing pyramid. Instead of testing an entire application at once, developers isolate specific logic to confirm it behaves properly under normal, boundary, and invalid conditions.

* **Core Purpose:** Validates that each standalone unit of software performs as designed.
* **Isolation:** External dependencies like databases, APIs, or file systems are replaced with simulated objects (mocks or stubs) so tests stay fast and predictable.
* **Automation:** Developers write and run these tests automatically using frameworks such as [Pytest](https://pytest.org) for Python, [Jest](https://jestjs.io) for JavaScript, and [JUnit](https://junit.org) for Java.
* **CI/CD Integration:** Teams link unit tests to continuous integration pipelines (such as GitHub Actions) so tests run automatically on every commit or pull request.

---

## Unit Testing Example
Most unit tests follow the **Arrange, Act, Assert (AAA)** pattern:
1. **Arrange:** Set up the test inputs and preconditions.
2. **Act:** Call the function or method being tested.
3. **Assert:** Verify that the output matches expectations.

Below is a Python function that calculates a discounted price, paired with a test suite using Python's built-in `unittest` module:

```python
import unittest

# 1. The "Unit" of code to be tested
def apply_discount(price, discount_percent):
    if discount_percent < 0 or discount_percent > 100:
        raise ValueError("Discount must be between 0 and 100")
    return price - (price * (discount_percent / 100))

# 2. The Unit Test Suite
class TestDiscountCalculator(unittest.TestCase):

    def test_standard_discount(self):
        # Arrange & Act
        result = apply_discount(100, 20)
        # Assert
        self.assertEqual(result, 80.0)

    def test_invalid_discount_raises_error(self):
        # Assert that an invalid input raises a ValueError
        with self.assertRaises(ValueError):
            apply_discount(100, 150)

if __name__ == "__main__":
    unittest.main()
```

### Running the Test
Save the code above as `test_discount.py` and run it from your terminal:

```bash
python -m unittest test_discount.py
```

---

## Advantages of Unit Testing
Building a reliable unit test suite provides several long-term engineering benefits:

* **Early Bug Detection:** Developers catch logic errors during the coding phase. Fixing a bug locally is much faster and cheaper than fixing it in production.
* **Safer Code Refactoring:** Running existing unit tests immediately alerts you if code cleanup or updates accidentally break established features.
* **Improved Code Design:** Writing testable code encourages smaller, modular, and loosely coupled functions rather than massive, tangled scripts.
* **Faster Debugging:** When a unit test fails, it points directly to the specific function causing the issue without requiring full-system tracing.
* **Living Documentation:** Well-named unit tests show contributors exact examples of how functions should be called and what outputs to expect.

---

## Conclusion
Unit testing acts as an automated safety net for software development. Although writing tests requires extra effort up front, it pays off by lowering debugging costs, preventing regressions, and improving overall code structure. 

> [!NOTE]
> Unit testing does not replace integration or end-to-end testing, as isolated units can still fail when combined. Used alongside broader testing phases, unit testing gives teams the confidence to ship reliable software quickly.

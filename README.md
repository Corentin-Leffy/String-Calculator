# String Calculator

## Source

This is a kata proposed by [Roy Osherove](https://osherove.com/). You can find the exercice [on his website](https://osherove.com/tdd-kata-1).

## Before you start

1. Try not to read ahead .
2. Do one task at a time. The trick is to learn to work incrementally.
3. Make sure you only test for correct inputs. There is no need to test for invalid inputs for this kata.
4. Test First!

## Tasks

* [ ] In a **test-first manner**, create a simple class `StringCalculator` with a method `Add` that takes a `String` and returns an `int`.
  * The method can take **0, 1 or 2 numbers**, and will **return their sum** (for an empty string it will return 0). 
  For example : `“” == 0`, `“1” == 1` , `“1,2” == 3`.
  * Start with the **simplest** test case of an **empty string** and move to **one & two numbers**.
  * Remember to solve things as **simply as possible** so that you force yourself to write tests you did not think about.
  * Remember to **refactor** after each passing test.
  
* [ ] Allow the `Add` method to handle an unknown amount of numbers.

* [ ] Allow the `Add` method to handle **new lines** between numbers (instead of **commas**).
  * The following input is ok:  `“1\n2,3” == 6`.
  * The following is **INVALID input** so do not expect it :  `“1,\n”` (not need to write a test for it).
  
* [ ] Support different delimiters:  to change a delimiter, the beginning of the string will contain a separate line that looks like this: `“//[delimiter]\n[numbers...]”`.
For example `“//;\n1;2” == 3` since the default delimiter is `;`. 
  * **Note**: All existing scenarios and tests should still be supported.

* [ ] Calling `Add` with a negative number will throw an exception `“negatives not allowed”`- and the negative that was passed.     

* [ ] If there are **multiple negatives**, show all of them in the exception message.

* [ ] Using TDD, add a method  to `StringCalculator`called `GetCalledCount`that returns how many times `Add()` was invoked. Remember-Start with a **failing (or even non compiling) test**.

* [ ] Numbers bigger than `1000` should be **ignored**. For example: `2 + 1001 == 2`.

* [ ] Delimiters can be of any length with the following format:  `“//[delimiter]\n”`. For example: `“//[***]\n1***2***3” == 6`.

* [ ] Allow multiple delimiters like this:  `“//[delim1][delim2]\n”`. For example `“//[*][%]\n1*2%3” == 6`.

* [ ] Make sure you can also handle multiple delimiters with **length longer than one** char. For example `“//[**][%%]\n1**2%%3” == 6`.

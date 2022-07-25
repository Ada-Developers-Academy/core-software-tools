# Activity: Code Reviews

This activity is based on the Code Reviews lesson in the Software Tools lesson.

## Goals

The goal of this activity is to introduce and practice pull requests as a way to review code submissions as part of a team project.

| Repository |
| ---------- |
| [Code Reviews](https://github.com/AdaGold/code-reviews) |


## Post Activity Questions

When the activity completes answer the following questions.

You are **not** expected to find every issue with the provided functions.  However list the issues you do find below.

<!-- Question 1 -->
### !challenge

* type: paragraph
* id: 8b18b4ed-5a3a-430a-ab0d-456ff93f21b4
* title: What style/readability issues did you find in the code?

* points: 1
* topics: python, code-reviews

##### !question

What style/readability issues did you find in the code?

##### !end-question

##### !placeholder

What style/readability issues did you find in the code?

##### !end-placeholder

<!-- other optional sections -->
<!-- !hint - !end-hint (markdown, hidden, students click to view) -->
##### !rubric

Students should find the following style/readability issues:

* Variable names are in camelCase
* Variable names are not descriptive
* Some spacing issues

##### !end-rubric

##### !explanation

Some things you may find:

* Some variable names are in camelCase
* Some variable names are not descriptive
* Some spacing issues, for example `x=x//10` instead of `x = x // 10`

##### !end-explanation

### !end-challenge

<!-- Question 2 -->

### !challenge

* type: paragraph
* id: 9fc8f407-17e7-48d4-8077-ba468e183c03
* title: What efficiency issues did you find?
* points: 1
* topics: python, code-reviews

##### !question

What efficiency issues did you find?

##### !end-question

##### !placeholder

What efficiency issues did you find?

##### !end-placeholder

##### !rubric

Students should find the following efficiency issues:

* `twoSum` involves nested loops and O(n^2) time complexity
* `merge_sorted_arrays` merges the two lists without using the fact that the input lists are already sorted resulting in O(n log n) time complexity instead of O(n).

##### !end-rubric

##### !explanation

* `twoSum` involves nested loops and O(n^2) time complexity
* `merge_sorted_arrays` merges the two lists without using the fact that the input lists are already sorted resulting in O(n log n) time complexity instead of O(n).

##### !end-explanation

### !end-challenge

<!-- Question 3 -->

### !challenge

* type: paragraph
* id: b80911df-1d46-45b3-b590-4680abb85882
* title: What testing issues did you find?
* points: 1
* topics: python, code-reviews, testing

##### !question

What testing issues did you find?

##### !end-question

##### !placeholder

What testing issues did you find?

##### !end-placeholder

##### !rubric

Students should find the following testing issues:

* No function has all of it's edge-cases covered

##### !end-rubric

##### !explanation

These are *some*, not all, of the issues present:

* `twoSum` tests do not cover the instance where no two numbers add up to the target.
* `palindrome_number` tests do not cover one digit numbers, or negative numbers.
* `merge_sorted_arrays` tests do not cover the case where the two lists are both empty, or contain overlapping elements.


##### !end-explanation

### !end-challenge


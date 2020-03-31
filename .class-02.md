## Code 201 Reading Assignment Notes - Class 2

_March 31, 2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Text
_Chapter 2 Text (pp.40-61)_

HTMl elements are used to describe the structure of the page.

Structural markup: elements used to describe both headings and paragraphs
Examples include `<b>`(bold) and `<i>` (italic)

Semantic markup: elements that add extra info to the page
Examples include `<em>` (emphasis), `<blockquote>` (blockquote), `<cite>` (citation), `<s>` (strikethrough), `<q>` (quotation)


### Introducing CSS
_Chapter 10 Introducing CSS (pp. 226-245)_

#### CSS Rules
CSS associates style rules with HTML elements.
```
p {
  font-family: Arial;
}
```
`p` is the **selector**.

`font-family: Arial;` is the **declaration**.

The selector indicates which element the rule applies to. The declaration says how the element should be styled.

#### CSS Properties
The CSS declaration sits between the curly braces. It has two parts: a *property* and a *value*, separated by a colon. You can have multiple properties in one declaration, separated by a semi-colon.
```
h1, h2, h3 {
  font-family:Arial;
  color: yellow;
}
```

The above example has two **properties** in the declaration: `font-family` and `color`.

`Arial` is the **value** for `font-family` and `yellow` is the **value** for `color`.

The declaration applies to h1, h2, and h3 elements. The properties indicate what aspects of the element you want to change (for example, color). Values specify the settings for the property (for example, yellow).

#### Using Stylesheets

Link to an external stylesheet - use `<link>' in the `<head>` of a document to tell the browser where to find the CSS file; use this when building a site with more than one page

Internal CSS - use `<style>` element in the `<head>' that includes the CSS

CSS rules cascade - if two or more rules apply to the same element:
- last rule takes precedence
- more specific rule takes precedence (p b is more specific than p)
- `!important` after the property value indicates that it should be more important than other rules applied to the element

CSS rules treat each element as if it appears inside its own box.




### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Basic JavaScript Instructions

_Chapter 2: “Basic JavaScript Instructions” (pp.53-84)_

**Script** - set of instructions a computer can follow

**Statement** - individual instruction or step

**Comments** - explain what your code does

**Variables** - store data the script needs to do its job

#### Declare a variable

`var quantity;` - `var` is the variable keyword, `quantity` is the variable name

If the variable name is more than one word, it's written in *camelCase*, where the first word is all lowercase and any subsequent words have the first letter capitalized.

#### Assign a value to a variable

After you create a variable, you tell it what you want it to store - assign it a value.

`quantity = 3;` - `quantity` is the variable name, `=` is the assignment operator (say "gets" not "equals"), `3` is the variable value

A variable without an assigned value is **undefined**.

### Data Types Stored in Variables

- Numbers

- Strings

- Booleans (true or false)

### Arrays

An array is a variable that contains a list of values.

The values in the array do not have to be the same data type. For example, you can have numbers and strings in the same array.

The index value for the first item in an array is 0, not 1.

#### Expressions and Operators

An expression results in a single value. Expressions rely on operators to allow programmers to create a single value from one or more values. 

For example, ` var color = 'beige';` - is an expression with an assignment operator `=`



### Decisions and Loops

_Chapter 4: “Decisions and Loops” -only up to the section on switch statements (pp.145-162)_

#### Decision Making

Flowcharts are a helpful tool to plan scripts where decisions need to be made about what code to run next. (The code can take more than one path.)

Use a **condition** to determine which path to take. Do this with **comparison operators**.

Examples of **Comparison operators** are `<`,`>`, and `===`

#### Evaluating a condition

```
if (condition is true) {
  do this thing;
  else [
    do this thing;
  ]
}
```
#### Comparison Operators

Usually return **true** or **false**

Best to use strict equal to and not equal to (`===` and`!==`) for equal and not equal comparisons. For strict, it compares the data type and value. 

Example: `'3' == 3` returns true; `'3' === 3` returns false

Usually one operator and two operands

Example:  `(score >= pass)` where `score` and `pass` are operands and `.=` is the operator.

This comparison is also an **expression** because it resolves into a single value (true or false).

An operand can also be an expression since an expression evaluates into a single value.

Example: `((score1 + score2) > (highScore1 + highScore2))`

#### Logical Operators

Allow you to compare the results of more than one comparison operator

`&&` - logical and - tests for more than one condition; if both are true, then it returns true; if either one is false, then it returns false

`||` - logical or - tests at least one condition; if either is true, it returns true, if both are false, it returns false

`!` - logical not - takes a single boolean value and reverses it; `!(2 < 1)` returns true

#### If Statements

If statements check a condition, if if is true, it runs the code in the subsequent code block (in the curly braces)

If/else statements check a condition, if it is true it runs the code in the subsequent code block. If it's false, it runs the code in the code block following the `else`.

```
if (condition is true) {
  do this thing;
  else [
    do this thing;
  ]
}
```


---
[Home page](https://marlene-rinker.github.io/reading-notes/)
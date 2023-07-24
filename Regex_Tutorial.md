# Regular Expression Tutorial: Extracting Phone Numbers from Text

## Intro

This tutorial on using regular expression to extract phone numbers from text. Regex are helpful tools for matching strings, patterns and helpful in extracting information from unstructured data sets be it javsscript, excel, tablue or SAS 7bdat or csv files. 

## Lesson

This regex pattern will differenciate between how phone numbers are written. If you are not aware, there is (123) 456- 7890, 123-456-7890 and 1234567890. There are many others country code that is added in the beginning +1 for US and other counties. Here I'll try and provide a pattern that captures this.

## Table of Contents
1. [Phone Number Extraction Regex: AreaCode](#phone-number-regex)
   - [A. Phone Number Format](#phone-number-format)
2. [Quantifiers](#testing)
3. [International Phone Numbers](#international-numbers)
4. [Conclusion](#conclusion)
5. [About the Author](#author)

## 1. Phone Number Extraction Regex: AreaCode
The first three digits of a phone number and closed with a parentheses, most often seen in the U.S 
The regex to capture an area code enclose in parentheses are
`/\((\d{3})\)/`

## A. Phone Number Extraction Regex: A. Phone Number Format
As said in the ##Lesson, there were three popular ways to write phone numbers(123) 456- 7890, 123-456-7890 and 1234567890.

Examples of each:

A. Format: (123) 456- 7890
The regex to capture a phone number in this format is
 `/\((\d{3})\) \d{3}-\d{4}/`

B. Format 123-456-7890
The regex to capture a phone number in this format is 
`/(\d{3}-\d{3}-\d{4})/`

C. Format 1234567890:
The regex to capture a phone number in this format is 
`/\d{10}/`

## 2. Quantifiers
Quantifiers are used in regular expressions to declare an expectation of something to match (e.g., +), or to specify the number of characters allowed (e.g., {2,6}).

As you see in each format `{}` is used to specifiy how many number of digits/characters are allowed.  Example `/\d{10}/` means 10 characters are allowed. 

## 3. International Numbers
US: +1 (123) 456-7890
Canada: +1 123-456-7890
Australia: +61 1 2345 6789

These are examples of international Numbers which has country codes and different number formats
Regex example to capture international numbers is ex.
`/(\+\d{1,4})?[\s-]*\(?(\d{1,4})\)?[\s-]*(\d{1,4})[\s-]*(\d{1,4})[\s-]*(\d{1,4})/g`

## 4. Conclusion
As the world gets more connected and calling internationally gets cheaper, there is a benefit in learning regex for numbers both domestic and abroad. Above are just a glimpse of what regex can do.

## 5. Author
Bootcamp student, Julius Bags, learning web development. Misunderstood the assignment and this a redo. First attempt wrote out the gist-template.md instead of creating my own. 

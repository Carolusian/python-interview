

```python
# Load necessary packages
import unittest
```

## Example Question: Find all even numbers from a list


```python
def even_numbers(lst):
    def is_even(x):
        """Check whether x is a even number"""
        return x % 2 == 0
    return [x for x in lst if is_even(x)]

class ExampleTest(unittest.TestCase):
    """Example test case"""
    data = [
        ([1,3,6,7,9,2], [6,2])
    ]

    def test_even_numbers(self):
        for [test_list, expected] in self.data:
            actual = even_numbers(test_list)
            self.assertEqual(actual, expected)


example_t = ExampleTest()
example_suite = unittest.TestLoader().loadTestsFromModule( example_t )
unittest.TextTestRunner().run(example_suite)
```

## Question 1: Rotates a matrix 90 degrees


```python
def rotate_matrix(m):
    pass

class MatrixRotationTest(unittest.TestCase):
    """Matrix rotation test case"""
    data = [
        ([
            ['a', 'b'],
            ['c', 'd']
        ], [
            ['c', 'a'],
            ['d', 'b']
        ])
    ]

    def test_rotate_matrix(self):
        for [test_matrix, expected] in self.data:
            actual = rotate_matrix(test_matrix)
            self.assertEqual(actual, expected)

matrix_rotation_t = MatrixRotationTest()
matrix_rotation_suite = unittest.TestLoader().loadTestsFromModule( matrix_rotation_t )
unittest.TextTestRunner().run(matrix_rotation_suite)
```

## Question 2: Using python decorator to wrap the returned string into a HTML tag

### Problem explanation:

```python
def html_tag(tag_name):
    pass

@html_tag('strong')
def function_to_be_decorated(name):
    return "Hello " + name

print(function_to_be_decorated("Donald Trump"))
```

NOTE: Implement html_tag, the result of the above snippet should be: <strong>Hello Donald Trump</strong>


```python
def html_tag(tag_name):
    pass
```

## Question 3: Tracking subclasses

Consider an application that must, at any given time, have access to a list of all subclasses of a particular class. Please implement the `__init__` method of SubclassTracker below:


```python
class SubclassTracker(type):
    def __init__(cls, name, bases, attrs):
        """Please implement here"""
        pass
    
class TrackedClass(object):
    __metaclass__ = SubclassTracker
    _registry = []
    
class ClassOne(TrackedClass):
    pass

class ClassTwo(TrackedClass):
    pass

# Expected output is [<class '__main__.ClassOne', <class '__main__.ClassTwo'>]
TrackedClass._registry
```

## Question 4: Implement Merge Sort  algorithm in an Pythonic way


```python
def merge_sort(lst):
    pass
```

## Question 5: Reverse the String

Given an input string, reverse the string word by word

Example input:
 * Given s = `"InitiumLab is so terrifically awesome"`
 * return `"awesome terrifically so is InitiumLab"`


```python
def reverse_words(str):
    pass

class ReverseWordsTest(unittest.TestCase):
    """Example test case"""
    data = [
        ('InitiumLab is so terrifically awesome', 'awesome terrifically so is InitiumLab')
    ]

    def test_reverse_words(self):
        for [test_list, expected] in self.data:
            actual = even_numbers(test_list)
            self.assertEqual(actual, expected)


reverse_words_t = ReverseWordsTest()
reverse_words_suite = unittest.TestLoader().loadTestsFromModule( reverse_words_t )
unittest.TextTestRunner().run(reverse_words_suite)
```

## Question 6: What is the time & space complexity of the following code

Assume that `random.random()` is an O(1) time, O(1) space function. 


```python
import random

a = 0
b = 0
for i in range(0, N):
    a = a + random.random()

for j in range(0, M):
    b = b + random.random()
```

Answer for Question 6: ???

## Question 7

### Task list:

* Scrape this channel (or another one): https://theinitium.com/channel/hongkong/ . Get structured article list data
* Handle pagination to scrape the whole list of articles
* Answer the following questions:
 * How many articles do we generate each week in this channel?
 * What is the distribution of article title lengths?
 * What is the most frequent keywords in title/ summary?
 * What is the distribution of cover image file sizes?
* For each article in the list, scrape the article page and get detailed information: title, description, date, author, tags, related articles
* Answer the following questions
* Which month/week do we have the largest number of publications in this channel?
* Who are the top 5 authors in terms of number of articles?
* Entity extraction:
 * Use any libraries like RegEx, LXML to extract entities: paragraph, figure, heading, number, wiki, etc
 * What are the most commonly used entities?
 * Make a tag cloud for this channel

## Question 8 (answer using R)

How will you combine multiple different string like "Data", "Science", "in", "R", "and", "Python" as a single string "Data_Science_in_R_and_Python" ?


```python

```

Let's say we have the following activity:

##### 1. Create a list named `my_list` that contains the values `a`, `b` and `c`
```python
my_list = ...
```

We don't care what's the procedure the user employs to solve this. All of the following are valid solutions:
```python
# option 1
my_list = ['a', 'b', 'c']

# option 2
my_list = list("abc")

# option 3
my_list = []
my_list.append('a')
my_list.append('b')
my_list.append('c')
```

The only thing we care is the outcome. Is `my_list` the object that we requested?

So, our assertion will test:

```python
assert my_list == ['a', 'b', 'c']
```

But, if the user clicks on "Check activity" before even defininf the variable, the following error will pop up:

```python
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'my_list' is not defined
```

Which is not so user friendly. So, we can improve it using our framework:

```python
expected_list = ['a', 'b', 'c']
assert_list_variable_equals_variable("my_list", expected_list)
# del expected_list 
```

# TO LEARN #

* https://www.youtube.com/channel/UCCezIgC97PvUuR4_gbFUs5g
* lambda function
* class(object)
* generators
* jupyter notebooks
* inheritance / subclasses
* property decorators
*

* git
* sqlite
* regular expressions


# First-class functions #
  * treat functions as objects
   * can be arguments / return parameters to / from functions
   * can be assigned to variables

# Closures #

 * can return inner functions which can remember variables within scope of their definition
   * "free variable"
   * return func
     * return inner function
   * return func()
     * executes and returns function

``` python
def outer_func(msg):
  def inner_func():
    print(msg)

hi_func = outer_fun("hi")

hi_func()
  -> "hi"
```

# DECORATORS #

* https://www.youtube.com/watch?v=FsAPt_9Bf3U

* function takes functions as input arguments, adds behavior and returns functions
* outer function = "decorator function"
* inner function = "wrapper function"

``` python
def decorator_function(original_function):
  def wrapper_function():
    return original_function()
  return wrapper_function

def display():
  print("test")

decorator_display = decorator_function(display)

decorator_display() # executes display()

```

* use-case: add functionality to existing functions without modifying them
* maintain added functionality in *one* location in code base
* alternative syntax

``` python
@decorator_function
def display():
  print("test")

display() # called "within" decorator function

```

* functions with additional arguments

``` python
@decorator_function
def display_info(name, age):
  print('name = {}, age = {}'.format(name, age))
```

* change necessary:

```python
def decorator_function(original_function):
  def wrapper_function(*args, **kwargs):
    return original_function(*args, **kwargs)
  return wrapper_function
```

* decorator classes (alternative to decorator functions)

```python
class decorator_class(object):
  def __init__(self, orig_func):
    self.orig_func = orig_func

  def __call__(self, *args, **kwargs):
    print("Call method executed before function {}".format(self.orig_func.__name__))
    return self.orig_func(*args, **kwargs)

    @decorator_class
    def display_info(name, age):
      print('name = {}, age = {}'.format(name, age))

display_info('John', 25)

```

## Stacked Decorators ##

 * multiple decorators can be stacked on top of each other
 ``` python
 from functools import wraps

 ...
 @wraps
 def wrapper ...

 ```

## Practical application scenarios ##

 * logging = keeping track about how many times function was called (and what types
 of arguments)
 * timer = measure execution time of functions


 * __name__ now returns correct file name

# MIXED #

np.asarray(['string 1', 'string 2')

z = [1, 2, 3]
sort(z, reverse=True)

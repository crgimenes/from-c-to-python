# From C to Python

I need to deal with a large project written in Python and several other scripting languages and I came from compiled C-like languages like C/C++/Objective-C/Go and so on.

But I know the design patterns and I have experienced friends to help me with the best practices and syntax (and maybe not so best practices), not to mention that it's interesting to get out of the comfort zone.

Luckily I'll just have to deal with Python version 3.6+. This text does not cover older versions.

## Tools to take a look

- ipython
- ipdb
- flake8
- [jupyter notebook](https://jupyter.org/)
- [black](https://github.com/ambv/black)
- [PyPI](https://pypi.org)

## Recommended Books

- Fluent Python

## Things to remember

Trying to program in Python and does not transform Python into a strange C.

---

### not do this

```python
def printf(format, *args):
    sys.stdout.write(format % args)
printf(“received %s”,data)
```

### instead do it

```python
print(f"received {data}", end="")
```

---

### And do not do that either!

```python
true, false, null = True, False, None
```

### RTFM

Read the documentation (obviously) and especially the [PEP 8](https://www.python.org/dev/peps/pep-0008/)

---

## Tips

### Static Analysis Tools

Install static analysis tools is essential because you do not have a compiler criticizing your code and find problems at runtime is bad.

#### Install flake8 manually

`pip install flake8`

#### Enable flake8 in VSC

Go to `Preferences > Settings > Python > Flake8Enabled`

### Backslash

You can break line wherever you want using backslash `\`

```python
if a and \
    b and \
        not b:
...
```

Or you can use parentheses

```python
if (a and
    b and
        not b):
...
```

### Black

The uncompromising Python code formatter (it is the `go fmt` of the Python)

```console
pip install black
```

### Comments

```python
# This is a comment in one line

"""
This is a multiple
line comment,
crazy, right?
"""
```

## Humor

- [tabs vs spaces](https://youtu.be/cowtgmZuai0)
- [Python Environment](https://xkcd.com/1987/)
- Lua: A more pleasant Python. (Gustavo H. M. Silva)
- import antigravity
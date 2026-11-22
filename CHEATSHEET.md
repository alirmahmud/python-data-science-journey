# Python Cheat Sheet

Everything learned so far, in one page. Updated at the end of every finished day.
**Last updated: Day 8 (Lists).** Next up: Day 9 (Tuples and sets).

How to use it: read it before each session (5 min), then do the 5-minute practice quiz in chat.

---

## Day 1: print and comments
```python
print("Hello")            # text needs quotes
print(5 + 3)              # 8   (math is done first)
print("5 + 3")            # 5 + 3   (in quotes = just text)
print("Churn:", 12, "%")  # commas print items with a space between
# anything after # is a comment; Python ignores it
```
- Missing a closing quote or bracket = `SyntaxError`. Read the line the error points to.

## Day 2: variables and types
```python
members = 1500            # int   (whole number)
churn_rate = 3.2          # float (decimal)
name = "Ali"              # str   (text)
is_active = True          # bool  (True / False, capital T and F)
type(name)                # <class 'str'>
members = members + 200   # a variable can be updated
```
- `"Members: " + 1500` is an **error**: you can't `+` text and a number.
  Fix: `"Members: " + str(1500)` or use a comma or an f-string.
- Convert: `int("42")` → 42, `float("3.5")` → 3.5, `str(1500)` → "1500".

## Day 3: operators
| Operator | Meaning | `10 ? 3` |
|---|---|---|
| `+ - *` | add, subtract, multiply | 13, 7, 30 |
| `/` | divide (**always a float**) | 3.333… |
| `//` | whole-number divide (floor) | 3 |
| `%` | remainder | 1 |
| `**` | power | 1000 |

- Order: `**` first, then `* / // %`, then `+ -`. `20 + 3 * 2` = 26.
- `int` with `float` gives `float`: `5 + 2.0` = 7.0. Even `6 / 3` = 2.0.
- Shortcuts: `x += 100`, `x -= 200`, `x *= 2`.
- **Minutes → hours:** `437 // 60` = 7 hours, `437 % 60` = 17 minutes.
- **Even or odd:** `n % 2 == 0` means even.
- `round(3.456, 2)` = 3.46. `round(x)` with no digits gives an int.

## Day 4: strings
```python
city = "Minnesota"
city[0]      # 'M'      first character (counting starts at 0)
city[-1]     # 'a'      last character
city[1:3]    # 'in'     from 1 up to, NOT including, 3
city[-5:]    # 'esota'  last 5
len(city)    # 9
```
| Method | Does |
|---|---|
| `.upper()` `.lower()` `.title()` | change case |
| `.strip()` | remove spaces at the **two ends only** (not in the middle) |
| `.replace("a", "b")` | swap text |
| `.split("-")` | string → list: `"GR-2026-00451".split("-")` → `['GR', '2026', '00451']` |
| `.startswith()` `.endswith()` | True / False |
| `"cancel" in note` | True if the text contains it |

- Methods can be chained: `name.strip().upper()`.
- Methods return a **new** string. `name.upper()` alone does not change `name`.

**f-strings** (the best way to print values):
```python
f"{hours} hours and {mins} minutes"
f"{churn_rate:.2f}%"      # 2 decimals        → 3.07%
f"${revenue:,}"           # thousands comma   → $283,500
f"${revenue:,.2f}"        # comma + 2 decimals → $283,500.00
```
- Order inside the braces is **comma first, then `.2f`**: `:,.2f`. Don't forget the dot: `:2f` is a different thing.

## Day 5: input and type conversion
```python
name = input("Your name? ")              # input() ALWAYS gives a string
age = int(input("Your age? "))           # convert it to do math
price = float(input("Price? "))
```
- `int(3.9)` = **3**. `int()` chops off the decimals; it does not round.
- `round(2.5)` = **2**, `round(3.5)` = 4. Exact .5 goes to the **even** number.
- `bool()` is False only for "empty" things: `0`, `0.0`, `""`. Everything else is True,
  including `bool(" ")` (a space) and `bool("False")` (non-empty text).
- Using a variable name you never created = `NameError`. Check spelling.

## Day 6: practice set 1 (putting it together)
```python
ending = start + signups - cancels
churn_rate = cancels / start * 100
print(f"=== {company.strip().upper()} REPORT ===")
print(f"Churn rate: {churn_rate:.2f}%")
print(f"{name[0]}.{name[1]}.")        # initials: first letter of each word
```
- `"5" * 3` = `'555'` (repeats text). `10 // 3 * 3 + 10 % 3` = 9 + 1 = **10**.

## Day 8: lists
```python
cancels = [46, 38, 52, 41, 60, 35]
cancels[0], cancels[-1], cancels[1:3]   # 46, 35, [38, 52]  (same indexing as strings)
len(cancels), sum(cancels), min(cancels), max(cancels)
sum(cancels) / len(cancels)             # average
```
| Change the list | Does |
|---|---|
| `.append(x)` | add to the end |
| `.insert(0, x)` | add at position 0 |
| `.remove(x)` | delete the first item equal to x |
| `.pop()` | delete and **return** the last item (`.pop(0)` = first) |
| `.sort()` | sort **in place**, returns `None` |

| Look at the list | Does |
|---|---|
| `sorted(lst)` | gives a **new** sorted list, original unchanged |
| `sorted(lst, reverse=True)` | highest first |
| `x in lst` | True / False |
| `lst.index(x)` | position of x |
| `lst.count(x)` | how many times x appears |

- **Find the month with the most cancels:** `months[cancels.index(max(cancels))]`
- String ↔ list: `"a,b,c".split(",")` → list. `" | ".join(lst)` → string.

---

## Traps you've hit (read these twice)
1. **`.sort()` and `print()` return `None`.**
   `b = a.sort()` → `b` is `None`. Use `b = sorted(a)`.
   `total = print(sum(x))` → `total` is `None`. Store first, print after: `total = sum(x)`.
2. **`.strip()` only cleans the ends of one string.** After `" A , B ".strip().split(",")` you get
   `['A ', ' B']`: each item still has spaces. Clean each item (you'll learn the loop for this in Week 3).
3. **f-string format order:** `:,.2f` (comma, dot, digits, f). `:2f` and `:.3f:,` are wrong.
4. **`int()` chops, `round()` rounds**, and `round(2.5)` = 2.
5. **`input()` gives text.** Wrap it in `int()` or `float()` before math.
6. **`bool("False")` is True.** Only empty or zero values are False.
7. **Variable name typos** (`notes` vs `note`, `cancellations` vs `cancels`) cause `NameError`.

---

## Session steps (if you forget how)
**Start**
1. Press the Windows key, type `cmd`, press Enter.
2. `cd %USERPROFILE%\Documents\python-data-science-journey`
3. `git pull`
4. `code .` (opens VS Code in this folder). If that fails: open VS Code, File → Open Folder → pick the folder.
5. In VS Code: left panel → `notebooks` → `phase0-python-basics` → right-click → New File → `dayNN_topic.ipynb`.
6. Top right of the notebook: **Select Kernel** → Python. Run a cell with **Shift + Enter**.

**End**
1. In the notebook: **Restart**, then **Run All** (buttons at the top). Every cell should run.
2. **Ctrl + S** to save.
3. Back in cmd: `git add .` → `git commit -m "Day N"` → `git push`

Think of it as: **pull** = download my latest, **add** = pick what to save, **commit** = label the save, **push** = upload it.

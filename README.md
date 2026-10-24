# Python for Data Science — Learning Journey

Goal: go from zero Python to confidently doing data science (NumPy, Pandas, Matplotlib, scikit-learn).
Pace: 1 hour per day. Tick a box `[x]` when a day is done and commit the change.

**Main sources**
- A Whirlwind Tour of Python (Phase 0): https://github.com/jakevdp/WhirlwindTourOfPython
- Python Data Science Handbook (Phases 1–5): https://github.com/jakevdp/PythonDataScienceHandbook

**Daily routine (60 min)**
1. **START:** open cmd in the repo folder and run `git pull`
2. 5 min: review yesterday's notebook
3. 35 min: lesson, typing every line of code yourself
4. 15 min: exercises
5. **END:** save to GitHub (commands below), then tell Claude "done"

**Git cheat sheet**
```cmd
cd %USERPROFILE%\Documents\python-data-science-journey

:: START of every session
git pull

:: END of every session (change the day number)
git add .
git commit -m "Day 2"
git push
```
Think of it as: **pull** = download my latest, **add** = pick what to save, **commit** = label the save, **push** = upload it.

**Folder layout**
```
notebooks/
  phase0-python-basics/
  phase1-ipython/
  phase2-numpy/
  phase3-pandas/
  phase4-matplotlib/
  phase5-machine-learning/
  phase6-capstone/
```

---

## Phase 0 — Python Basics (4 weeks)

**Week 1: First steps**
- [x] Day 1: Colab setup, first program, `print`, comments
- [ ] Day 2: Variables and data types (int, float, str, bool)
- [ ] Day 3: Arithmetic and operators
- [ ] Day 4: Strings: indexing, slicing, methods, f-strings
- [ ] Day 5: User input and type conversion
- [ ] Day 6: Practice set 1
- [ ] Day 7: Review / catch-up

**Week 2: Collections**
- [ ] Day 8: Lists
- [ ] Day 9: Tuples and sets
- [ ] Day 10: Dictionaries
- [ ] Day 11: Nested data structures
- [ ] Day 12: Comparison and boolean logic
- [ ] Day 13: Practice set 2
- [ ] Day 14: Review / catch-up

**Week 3: Control flow**
- [ ] Day 15: `if` / `elif` / `else`
- [ ] Day 16: `for` loops and `range`
- [ ] Day 17: `while` loops, `break`, `continue`
- [ ] Day 18: List and dict comprehensions
- [ ] Day 19: Errors and `try` / `except`
- [ ] Day 20: Practice set 3
- [ ] Day 21: Review / catch-up

**Week 4: Functions and modules**
- [ ] Day 22: Defining functions, arguments, return values
- [ ] Day 23: Default args, `*args`, `**kwargs`, lambda
- [ ] Day 24: Modules and imports (`math`, `random`, `datetime`)
- [ ] Day 25: Reading/writing files, intro to CSV
- [ ] Day 26: Classes and objects (just enough to read library code)
- [ ] Day 27: Mini project: churn calculator using plain Python
- [ ] Day 28: Phase 0 checkpoint quiz

## Phase 1 — IPython & Jupyter (1 week) · Handbook Ch. 1
- [ ] Day 29: Help, `?`, tab completion
- [ ] Day 30: Magic commands (`%timeit`, `%run`)
- [ ] Day 31: Input/output history, shell commands
- [ ] Day 32: Errors and debugging
- [ ] Day 33: Profiling and timing code
- [ ] Day 34: Practice
- [ ] Day 35: Checkpoint quiz

## Phase 2 — NumPy (3 weeks) · Handbook Ch. 2
- [ ] Week 5 (Days 36–42): Data types, array basics, indexing, slicing, reshaping
- [ ] Week 6 (Days 43–49): Universal functions, aggregations, broadcasting
- [ ] Week 7 (Days 50–56): Boolean masks, fancy indexing, sorting, structured arrays · checkpoint quiz

## Phase 3 — Pandas (5 weeks) · Handbook Ch. 3
- [ ] Week 8 (Days 57–63): Series, DataFrame, Index, selection
- [ ] Week 9 (Days 64–70): Operations, missing data, hierarchical indexing
- [ ] Week 10 (Days 71–77): Concat, merge, join
- [ ] Week 11 (Days 78–84): GroupBy, pivot tables, string operations
- [ ] Week 12 (Days 85–91): Time series, `eval()` / `query()` · mini project on a membership/churn-style dataset

## Phase 4 — Matplotlib & Seaborn (3 weeks) · Handbook Ch. 4
- [ ] Week 13 (Days 92–98): Line, scatter, error bars, histograms
- [ ] Week 14 (Days 99–105): Legends, colorbars, subplots, text and annotation
- [ ] Week 15 (Days 106–112): Customization, Seaborn · checkpoint: recreate a work-style dashboard chart

## Phase 5 — Machine Learning (6 weeks) · Handbook Ch. 5
- [ ] Week 16 (Days 113–119): What is ML, intro to scikit-learn
- [ ] Week 17 (Days 120–126): Hyperparameters and model validation, feature engineering
- [ ] Week 18 (Days 127–133): Naive Bayes, linear regression
- [ ] Week 19 (Days 134–140): Support vector machines, decision trees and random forests
- [ ] Week 20 (Days 141–147): PCA, manifold learning
- [ ] Week 21 (Days 148–154): k-means, Gaussian mixtures, kernel density · checkpoint quiz

## Phase 6 — Capstone (2 weeks)
- [ ] Week 22 (Days 155–161): Pick dataset, clean, explore, visualize
- [ ] Week 23 (Days 162–168): Build model (e.g., churn prediction), evaluate, write up results

---

## Progress Log
| Date | Day | What I learned | Stuck on |
|------|-----|----------------|----------|
| 2026-10-24 | 1 | Colab, `print()`, comments, strings vs numbers, reading a SyntaxError | GitHub save from Colab failed; used download/upload |

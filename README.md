# CFG Homework 3 – Implementation

> University of Bucharest – *Formal Languages and Automata Theory*  

This repository contains an **interactive Python 3 program** that lets you:

1. **Define** a context‑free grammar (CFG) from the keyboard;
2. **Generate** random strings from the grammar (limit 10 chars, 5 samples);
3. Show a **left‑ or right‑most derivation** for a given target string;
4. **Recognise** whether a string belongs to the CFG's language.

---

## 🛠️ How to Run

```bash
python3 main.py


# 📘 Short Explanation of the Code

This Python program allows users to **create and explore a context-free grammar (CFG)** interactively from the command line.

---

## 🔧 What the Code Does

It helps you:

- Define a CFG by entering rules manually
- Generate random words in the CFG's language
- Show derivation steps for a word
- Check if a word belongs to the language defined by the CFG

---

## 📦 Key Components

### 1. `CFG` Class

Holds the grammar:

- `terminals`: set of terminal symbols (e.g., a, b, c)
- `nonterminals`: set of nonterminal symbols (e.g., S, A)
- `R`: a dictionary of productions (e.g., `S -> aSb | #`)
- `S`: the start symbol

### 2. Grammar Input

- `cfg.parse()`: reads the start symbol and productions from the user
- Format: `S -> aSb | #` (use `#` to represent lambda ε)

### 3. Derivation Functions

- `derivate(cfg, s, pos)`: applies one production rule at a specific position
- `left_derivation()` and `right_derivation()`: apply derivations from the leftmost or rightmost nonterminal
- `generate_random()`: recursively expands nonterminals to generate valid strings (limited to 10 characters)

### 4. Word Recognition

- `derivation_gen()`: recursively simulates derivations and builds a path to the target string (if it can be derived from the start symbol)

---

## 🖨️ Output Behavior

- Prints 5 random valid strings from the CFG
- Asks for a string and displays its derivation path if valid
- Tells whether a string belongs to the language

---

## ✅ Summary

This script fulfills key CFG operations:

- ✅ CFG input
- ✅ Word generation
- ✅ Word validation
- ✅ Derivation tracing


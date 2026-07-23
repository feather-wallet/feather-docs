---
title: Additional seed entropy from dice rolls
nav_title: Additional seed entropy from dice rolls
category: advanced
---

You can use dice rolls or coin flips to generate extra entropy in addition to entropy provided by your system for the creation of a Polyseed.

This may be useful if:

- You want to create a seed in an environment that may have insufficient entropy (such a live operating system or virtual machine)
- You do not want to rule out the possibility that your operating system has flaws that weaken the entropy provided by its random number generator

Polyseed requests 19 bytes (= 152 bits) of entropy. This tool assumes your system provides no entropy in determining how many rolls you must throw. Regardless, it will use system entropy _in addition_ to entropy generated from rolls/flips to reduce the impact of human error. **Do not write down the outcome of your dice rolls or coin flips.** This information can not be used to recreate your seed.

## Usage

To access the tool, click **Create a new wallet** on the main menu. On the next page, press **Crtl + K**.

Select whether to use dice rolls or coin flips. 

### Using dice

Select how many sides your die has. Using a die with more sides reduces the number of rolls you need to throw.

- D6: 59 rolls
- D12: 42 rolls
- D20: 36 rolls

The die must indicate numbers 1 through N, where N is the number of sides of the die. Do not use dice that skip numbers (2, 4, 6, 8, 10, 12) or ones that include the number 0.

You may throw multiple dice in one go, but **all dice must have the same number of sides**. Do not mix a D6 with a D20, etc.

If you throw multiple dice, scan the throwing area from left to right to determine which rolls to enter first. Do not sort the dice by outcome. Do not re-roll dice, even if the outcome looks "non-random".

For example, if you roll:

```
⚃       ⚄
    ⚁
             ⚀
```

Enter `4 2 5 1` in the entry box and press **Next roll**. 

You must only enter actual dice rolls. Do not enter 'random' numbers from your head.

Add more rolls until **Rolls left** reaches zero, then click **Create polyseed**.

The new Polyseed is automatically filled into the wallet creation wizard. **Don't forget to write it down.**

### Using coins

Flip a coin, if it lands on heads press **Heads**, it lands on tails press **Tails**. Repeat this process until "Flips left" reaches zero, then click **Create polyseed**.

The new Polyseed is automatically filled into the wallet creation wizard. **Don't forget to write it down.**

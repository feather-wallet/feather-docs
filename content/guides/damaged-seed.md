---
title: Recovering a damaged Polyseed
nav_title: Recovering a damaged Polyseed
category: advanced
---

Use this guide if you are trying to restore your wallet from seed, but your seed phrase is damaged or incomplete.

### Common scenarios

- Some of the words are unintelligible (bad handwriting, smudges, etc.)
- Some of the words are incomplete (cut off, shorthand, etc.)
- One or two words are completely missing (but you know their place in the seed)

The Seed Recovery tool can't help you if you don't know the order of the seed words.

### Before you begin

- Make sure the seed phrase consists of (or consisted of) 16 words
  - If you only have 12 words, you may have an Electrum (Bitcoin) seed
  - If you only have 14 words, you may have a legacy Feather seed
  - If you have 24/25 words, you may have a standard Monero seed

This tool is can only help recover Polyseeds.

### Check the wordlist

If the handwriting is unintelligible or obscured it might help to look at the wordlist in order to determine what was written:

https://raw.githubusercontent.com/bitcoin/bips/master/bip-0039/english.txt

If you can't unambiguously identify a word, go to the next step.

### Use the Seed Recovery tool

To access the Seed Recovery tool, click 'Restore wallet from seed' on the main menu. On the next page, press '**Ctrl + K**'.

Enter each word you know in the correct box. Regex is supported for partial words.

**Examples**:

- If you know the word begins with 'his', just enter: `his`
- If you know the word ends with 'ory', add a dollar sign at the end: `ory$`
- If you know the word starts with 'hi' and ends with 'y': `^hi.*y$`
- If you know the word contains the string 'si': `.*si.*`
- If you know the word is either 'history' or 'victory': `history|victory`
- If you don't know a word, leave the field blank.

Click '**Check**' to start the recovery. Recovery will take exponentially longer the more information is missing. 
In some cases, recovery is infeasible. Wait until the progress bar is full or click '**Cancel**' if the search is taking too long.

If the tool reports that the word is not in the wordlist:

- Check the spelling
- Make sure the Regex is valid
- If multiple words do not exist in the wordlist, you may not have a Polyseed

# RandomWordGenerator

A pair of classes to randomly generate words given a set of consonants, vowels, maximum tolerable syllable structure and maximum word length in syllables.

## Inputs

### Consonants and Vowels

Consonant and vowel inventories should be passed into the WordGenerator object on initialization as arrays of single-character strings.

The inventories are then passed along to the SyllableGenerator object created on initialization so that it can pull randomly from each of them to generate syllables.

### Syllable Structure

This should be a string consisting of only "C" and "V" characters (representing Consonant and Vowel respectively) and represents the most complex possible syllable for the generated words. The string must match the following regular expression: `^[C]*[V]+[C]*$`. The string must start with any number of "C" (or 0), have at least one "V", and end with 0 or any number of "C".

The syllable generator will also generate other permutations of the given structure: if "CVC" is passed in, the generator will also return syllables that follow the "CV", "V" and "VC" patterns, as well. 

For example, languages like Japanese can tolerate, with some special exceptions, syllables only as complex as "CV", meaning a consonant followed by a vowel. English, on the other hand, can often have syllables as complex as "CCCVCCC", as in the word "strength".

### Length

This represents the maximum number of syllables per word. Generated words will have syllables between 1 and this number of syllables long.

## Future Directions

- [ ] Validate inputs to prevent problems with garbage input.
- [ ] Allow groups of consonants/vowels and more syllable types for more granular control over generated words/syllables.
- [ ] Create another class that takes in phonological rules and applies them to generated words for more natural sounding words.

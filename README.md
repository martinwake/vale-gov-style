# Use Vale to check for GOV.UK style
A style package for the [prose linting tool Vale](https://vale.sh/) to check against the [GOV.UK A-Z Style Guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style).

## Things to note

- This is not a spellchecker. Vale comes with a built in US spellcheck dictionary but I haven't managed to find and implement a good en-GB one, and there are good enough options elsewhere.
  
- It doesn't check against every entry in the style guide. Some are general discussions like “Abbreviations” which are difficult to automate; others are just too discursive. In the "words to avoid" list, some are common words which should only be avoided in certain contexts (for example, when used as verbs rather than nouns).

## What is in this repository
Vale uses "packages" to manage style rules. [Read more about Vale packages](https://vale.sh/docs/topics/packages/)

This repository contains a Vale style package, `gov-uk.zip`, which includes the following YAML files: 

- Avoid.yml
- Hyphens-spacing.yml
- Lower-case.yml
- Upper-case.yml

Vale uses these to check your writing against:
- capitalisation, hyphenation and spacing rules (together these make up about 70% of the entries in the A-Z style guide)
- the list of [words to avoid](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#words-to-avoid) 

## Thanks
After going round in circles for a long time with various tools I found out about Vale from a talk given by [@sabrinaharris](https://github.com/sabrinaharris) about [this project](https://github.com/sabrinaharris/linting-prototype), which uses Vale to lint technical documentation against a broader set of style rules.

# Check for GOV.UK style
This repository contains rules for the [style checking tool Vale](https://vale.sh/) that check against the [GOV.UK A-Z Style Guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style) and [Words to avoid list](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#words-to-avoid).

## Things to note

- This is not a spellchecker. Vale comes with a built in US spellcheck dictionary but I haven't managed to find and implement a good en-GB one, and there are good enough options elsewhere.
  
- It doesn’t include every entry from either source. Some style guide entries are general discussions like “Abbreviations” which are difficult to automate; others are just too discursive. In the "words to avoid" list, some are common words which should only be avoided in certain contexts (for example, when used as verbs rather than nouns).

## What is in this repository
Vale uses "packages" to manage style rules. [Read more about Vale packages](https://vale.sh/docs/topics/packages/)

This repository contains a Vale style package, `gov-uk.zip`, which includes the following YAML files: 

- Avoid.yml
- Hyphens-spacing.yml
- Lower-case.yml
- Upper-case.yml

Vale uses these to check your writing against:
- capitalisation, hyphenation and spacing rules from the GOV.UK A-Z Style Guide (together these make up about 70% of the entries in the guide)
- the list of words to avoid

## Acknowlegments
After going round in circles for a long time with various tools I found out about Vale from a talk given by [@sabrinaharris](https://github.com/sabrinaharris) about [this project](https://github.com/sabrinaharris/linting-prototype), which uses Vale to lint technical documentation against a broader set of style rules.

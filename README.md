# Check for GOV.UK style
This repository contains rules for the [style checking tool Vale] (https://vale.sh/) that check against the [GOV.UK A-Z guidelines](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style) and [Words to avoid list](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#words-to-avoid).

## Things to note
- This project isn't associated with GOV.UK or GDS. 

- It’s not a spellchecker. Vale comes with a built in US spellcheck dictionary but I haven't managed to find and implement a good en-GB one, and there are good enough options elsewhere.
  
- It doesn’t include all the rules from the A-Z style guide. Some entries are general discussions like “Abbreviations” which are difficult to automate; others are just too discursive. It turns out that nearly 70% of the rules in the style guide are to do with capitalisation or hyphenation, so I’ve focused on those. 

## What is in this repository
This repository contains a single zip file `gov-uk.zip`, which includes the following rules:

- Avoid.yml
- Hyphens-spacing.yml
- Lower-case.yml
- Upper-case.yml

## Acknowlegments
After going round in circles for a long time with various tools I found out about Vale from a talk given by @sabrinaharris about [this project](https://github.com/sabrinaharris/linting-prototype), which uses Vale to lint technical documentation.

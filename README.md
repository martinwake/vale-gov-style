# Use Vale to check for GOV.UK style
A style package for the [prose linting tool Vale](https://vale.sh/) that implements the [GOV.UK A-Z Style Guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style).

## Things to note

- __As of 5 Dec 2024 the project needs updating to work with the current version of Vale__. As far as I can see there are some structural changes meaning that some things previously done with `Styles` are now done with `Vocabularies`. [v3.0.0 release notes](https://github.com/errata-ai/vale/releases/tag/v3.0.0)

- This is not a spellchecker. Vale comes with a built in US spellcheck dictionary (which this package doesn't check against for obvious reasons) but I haven't managed to find and implement a good en-GB one, and there are good enough options elsewhere.
  
- It doesn't check against every entry in the style guide. Some are general topics like “Abbreviations” which are difficult to automate; others are just too discursive. In the "words to avoid" list, some are common words which should only be avoided in certain contexts (for example, when used as verbs rather than nouns).

## What is in this repository
Vale uses "packages" to manage style rules. [Read more about Vale packages](https://vale.sh/docs/topics/packages/)

This repository contains a Vale style package, `gov-uk.zip`, which includes the following YAML files: 

- Avoid.yml
- Hyphens-spacing.yml
- Lower-case.yml
- Upper-case.yml

These rules will check your writing for:
- capitalisation, hyphenation and spacing (together these make up about 70% of the entries in the A-Z style guide)
- the list of [words to avoid](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style#words-to-avoid) 

## To do

* __5 Dec 2024: Update project to latest version of Vale__
* Write basic how-to for getting Vale up and running
* Try out GitHub Actions and GitHub Codespaces
* Some kind of automation to keep the rules up to date when the style guide changes. Possibly based on JSON or screen scraping?
* An interface that doesn't need the command line. This project is mainly aimed at content people who don't always have access to (or confidence with) command line tools or npm packages.


## Thanks
After going round in circles for a long time with various tools I found out about Vale from a talk given by [@sabrinaharris](https://github.com/sabrinaharris) about [this project](https://github.com/sabrinaharris/linting-prototype), which uses Vale to lint technical documentation against a broader set of style rules.

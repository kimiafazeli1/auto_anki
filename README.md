



 # Auto Anki

[![ForTheBadge built-with-love](http://ForTheBadge.com/images/badges/built-with-love.svg)](https://github.com/SmayanaReddy/auto_anki)

![Build Status](https://img.shields.io/badge/build-passing-green)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5745931.svg)](https://doi.org/10.5281/zenodo.5745931)
![codecov](https://img.shields.io/badge/codecov-85%25-green)

[![GitHub license](https://img.shields.io/github/license/SmayanaReddy/auto_anki)](https://github.com/SmayanaReddy/auto_anki/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/SmayanaReddy/auto_anki)](https://github.com/SmayanaReddy/auto_anki/issues)
[![GitHub issues-closed](https://img.shields.io/github/issues-closed/SmayanaReddy/auto_anki)](https://github.com/SmayanaReddy/auto_anki/issues?q=is%3Aissue+is%3Aclosed)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/SmayanaReddy/auto_anki/pulls)
![version](https://img.shields.io/badge/version-3.0-blue)
![github workflow](https://github.com/SmayanaReddy/SRIJAS/actions/workflows/unit_test.yml/badge.svg)
![github workflow](https://github.com/SmayanaReddy/SRIJAS/actions/workflows/style_checker.yml/badge.svg)
![github workflow](https://github.com/SmayanaReddy/SRIJAS/actions/workflows/main.yml/badge.svg)
![github workflow](https://github.com/SmayanaReddy/SRIJAS/actions/workflows/code_cov.yml/badge.svg)

## [Demo Video](https://drive.google.com/file/d/12h5izedNfEth56KhbKFRBYDFKU2PPChQ/view?usp=sharing) 

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#why-should-you-use-auto-anki">Why should you use Auto Anki?</a></li>
    <li><a href="#check-out-the-video">Check out the video!</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#code-documentation">Code Documentation</a></li>
    <li><a href="#how-to-contribute">How to Contribute</a></li>
    <li><a href="#future-roadmap">Future RoadMap</a></li>
   <li><a href="#contributors">Contributors</a></li>
   <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

Auto Anki generates flash-cards from your lectures, which you can study with ease! Auto Anki builds on [Anki](https://apps.ankiweb.net/), an intelligent flash-card tools for remembering things.

Example QA from lecture            |  Example QA from lecture
:-------------------------:|:-------------------------:
![](https://github.com/usmanwardag/auto_anki/blob/main/figs/anki_1.png)  |  ![](https://github.com/usmanwardag/auto_anki/blob/main/figs/anki_2.png)

If you are someone who struggles to memorise concepts taught in class, or faces difficulty during revision, or if you are just too lethargic to take notes, then Auto-Anki is for you!

<img src="https://media.giphy.com/media/nMjVMvWm2JIT8Rd1Gt/giphy.gif" width="300" height="300">

Auto Anki extracts important concepts from lectures, and frames questions based on it. It searches for the answers on the web and extracts the most relevant answers. Auto Anki combines with the powerful features of Anki that let you rate the difficulty level of every question to make it easy for you to memorize tough questions.

## Why should you use Auto Anki?

- You want to summarize everything in a lecture to flash cards, which you can then memorize.
- You already use Anki, but have to create the flash cards for lectures manually.
- You want to break down the lecture pdf into questions and answers.
- You want to create simple flashcards for easy memorisation and revision.

<img src="https://media.giphy.com/media/7TMZ8O1bbf1UAnS4Ve/giphy.gif" width="400" height="300">
We know :)

## Check out the video!
https://user-images.githubusercontent.com/32881355/144337381-2c38d27d-9118-497e-a664-5d0433fedca7.mp4


# Installation

- Clone the repository 
 ` git clone https://github.com/SmayanaReddy/auto_anki
- Install all requirements
 ` pip install -r requirements.txt`
- Install project as Python package
 ` pip install .`
- Clone Anki library
 ` git clone https://github.com/kerrickstaley/genanki; cd genanki`
- Install Anki library
 ` python setup.py install`

## Code Documentation

Documentation of the entire codebase is generated using [Pycco](https://github.com/pycco-docs/pycco). 
You can find the documentation [here](https://github.com/SmayanaReddy/auto_anki/tree/main/docs).

If you are a developer, and want to update documentation:

- Install Pycco
  `pip install pycco`
- Use Pycco to generate docs.
  `pycco auto_anki/**/*.py -p`
  
## Code Coverage

For checking code coverage, 
- Install Coverage (https://pypi.org/project/coverage/)
  `pip install coverage`
- For generating the report run
  `coverage run user_cli.py`
- For viewing the report run
  `coverage report`

| Name              | Stmts | Miss | Cover |
|-------------------|-------|------|-------|
| anki.py           | 14    | 3    | 83%  |
| extract_sizes.py  | 55    | 6    | 89%   |
| google_search.py  | 13    | 2    | 87%  |
| user_cli.py       | 53    | 7    | 87%   |
| wordprocessing.py | 125   | 23   | 81%   |
| TOTAL             | 260   | 57   | 85%   |
 

## How to Contribute
  
We would be happy to receive contributions! If you'd like to, please go through our [CONTRIBUTING.md](https://github.com/SmayanaReddy/auto_anki/blob/main/CONTRIBUTING.md). 

For any feedback, issues, or bug reports, please create an issue [here](https://github.com/SmayanaReddy/auto_anki/issues/new).

## Future RoadMap
#### Build a browser extension with the current functionality
  - A browser extension which will extract contents of the current webpage which the user is on and produce a new deck of anki cards based on the material.
#### Improve word extraction logic
  - Currently Spacy is being used to extract noun phrases from each slide/page of the document. Then the high frequency noun phrases are calculated and used in the final search query. However this causes an issue when every slide has the document’s author name and email address listed. The author name is considered as a noun phrase, and since it appears on every slide has a high frequency, and thus appears on the final search query.


## Contributors

* Keith Tran (ktran24@ncsu.edu)
* Benyamin Tabarsi(btaghiz@ncsu.edu)
* Kimia Fazeli(kfazeli@ncsu.edu)
* mfaizan@ncsu.edu


## Acknowledgements
We have built this code on top of the stack from the project [
](https://github.com/SmayanaReddy/auto_anki)https://github.com/SmayanaReddy/auto_anki


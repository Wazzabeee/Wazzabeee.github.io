---
name: Plagiarism checker
tools: [Python, Pdf, Similarity, Docx, Beautifoulsoup, bs4, Plagiarism, Similarity-Score, Txt, Odt, Plagiarism-Checker, Plagiarism-Detection, Side-by-sidediff, Plagiarism-Detector]
image: ../assets/img/portfolio/plagiarism_checker/plagiarism_checker.gif
description: Make plagiarism detection easier. This script will find similar sentences between given files and highlight them in a side by side comparison.
---
## About
This program will proccess pdf, txt, docx, and txt files that can be found in the given input directory, find similar sentences, calculate similarity percentage, display a similarity table with links to side by side comparison where similar sentences are highlighted.

This project was made part of my internship at the "Human Computer Humans Interacting with Computers at University of Primorska" lab (HICUP Lab).

## Usage

```
Usage: main.py input_directory [OPTIONS]

  Perform a similarity analysis of all text files available in given input directory.
  Developped by Clément Delteil -> (Github: wazzabeee)


Options:
  -block_size, -s  Set minimum number of consecutive and similar words detected. (Default is 2)
  -out_dir, -o     Set the output directory for html files. (Default is creating a new directory)
  -help, -h        Show this message and exit.
```

## How to use
```bash
# Clone this repository
$ git clone https://github.com/Wazzabeee/plagiarism_checker

# Go into the repository
$ cd plagiarism_checker

# Install requirements
$ pip3 install -r requirements.txt

# Run the app
$ python main.py C:/Users/Desktop/papers -s 2 -o C:/Users/Desktop/results
```

## First run
On the first run you might get :
- an ImportError from pdfminer library 
``` 
ImportError: cannot import name 'uint_value' from 'pdfminer.pdftypes' (C:/.../pdfminer/pdftypes.py)
```
To fix this, please uninstall pdfminer3k and pdfminer.six via 
``` pip uninstall pdfminer3k ```
``` pip uninstall pdfminer.six ```
Then install them again via 
``` pip install pdfminer3k ```
``` pip install pdfminer.six ```


- a TypeError from Slate3k library 
```
TypeError __init__() missing 1 required positional arg 'parser' in "C:/.../slate3k/classes.py
```
To fix this you'll need to modify `class PDF(list):` in `C:/.../slate3k/classes.py`. In `def __init__()` change both `if PYTHON 3:` to `if not PYTHON 3:` on lines 58 and 72.

## Recommandations
- Please make sure that all text files are closed before running the program.
- In order to get the best results please provide text files of the same languages.
- Pdf files that are made from scanned images won't be processed correctly.
- If a specific file is not processed correctly feel free to [contact me](mailto:<clement.delteil@utbm.fr>) so that I can address the issue.

## Used Software and Libraries
- Programming language: Python
- Libraries : beautifoulsoup, nltk
- Source control: GitHub
- Other tools: PyCharm

<p class="text-center">
{% include elements/button.html link="https://github.com/Wazzabeee/plagiarism_checker" text="Code" %}
</p>

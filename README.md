# Creating a structured data set from the canada.ca/news articles

Programmer and Author: David Hobson

Date: August 28th,  2020

## Purpose and Overview

Within this repository you’ll find a collection of programs intended to collect and structure the information relevant to the BIGS program that can be found in the articles on the *canada.ca/news* website. 

The programs seek to complete three tasks: 

1. cleaning up the text in the articles, 

2. calibrating and applying a natural language processor to label relevant information in the text, and 

3. extracting and restructuring the meaningful information that can be found in the labelled text.

Please note that these programs do not contain the actual web scraper to extract the articles from the *canada.ca/news* website, and the programs assume that this information has already been scraped. At the time of writing this, this information has been stored on a database on MongoDB, and the programs use this as a starting point to retrieve the articles.

Although these programs complete three tasks, you may notice that there are more than three programs in this repository! This is mainly to narrow down the working number of articles before the Natural Language Processor is applied, and also to perform some basic descriptive statistics on the articles themselves, but is not related to building the structured data set. 

The final structured dataset produced by the programs can be found in the *Program Dataset* file in the **excel_sheets** directory. The same dataset in a more readable form is found in the *Program Dataset (Concise)* file.

## Program Overviews

All programs are written in Python 3, however each program has been included as an Jupyter Notebook (.ipynb) file for easier use and better visualization.

The Natural Langauge Processor employed is the one from the *spaCy* package. The *pandas* package in Python is used frequently to manipulate data and for integration with Microsoft Excel. For connection with MongoDB, the *pymongo* package is used.

For comprehensive descriptions of each of the programs, as well as the approaches taken by each program, please consult the *About the Programs* and *Appendix* Word files in the **documentation** directory. 

## File Organization

The repository contains the following files:

1) Cleaning up the Articles.ipynb

2) Finding Articles with Program Streams.ipynb

2.5) Statistics on the Articles.ipynb

3) Applying the NER.ipynb

4) Extracting Useful Information.ipynb

- **data**
    - cleaned_articles_dictionary.json
    - cleaned_articles.json
    - labelled_text.bin
- **documentation**
    - About the Programs.docx
    - Appendix.docx
- **excel_sheets**
    - Departments and Programs.xlsx
    - Program Dataset.xlsx

The **data** directory is where all of the output files for the programs are stored.

The **documentation** directory contains all of the documents describing the program.
- *About the Programs* gives an overview of each of the progams 
- *Appendix* provides more in-depth details and other extra content

The **excel_sheets** directory contains all of the Excel files used by the programs. 
- *Departments and Programs* contains spreadsheets of the departments, program streams, and PIFs relevant to BIGS, as well as equivalent names
- *Program Dataset* gives the current structured dataset produced by the programs
- *Program Dataset (Concise)* gives the same dataset as *Program Dataset* but in a more readable format

## Compilation and Launch Instructions

Before running the programs, please ensure that the *pandas*, *pymongo*, and *spaCy* packages are all installed. If this it not the case, it is recommended that the user install Anaconda as a package manager, as all the necessary packages needed to run the programs are included with Anaconda. Please see Anaconda's website for details on installing Anaconda.

To run the programs, please download this repository and run this directory in the Jupyter Notebook application. (To do this in the command prompt, navigate to this directory and run the command "jupyter notebook", and your browser should launch, navigating you to the application.)

Please note that all programs in this repository were initially written using a macOS system. For use on a Windows machine, please change the file paths in applicable commands where necessary.

For programs that involve connections to MongDB, please enter your Database Username and Password in the section of the code at the beginning where the connection to MongoDB is made. For more information or for troublshooting related to connecting to Mongo, please see section 7 in the *Appendix* (located in the **documentation** folder) entitled, *Connecting to Mongo remotely (for Python, using pymongo)*.


# Creating a structured data set from the canada.ca/news articles

These programs intend to collect and structure the information relevant to the BIGS government initiative program from articles on the *canada.ca/news* website. 

The programs seek to complete three tasks: 

1. cleaning up the text in the articles, 

2. calibrating and applying a natural language processor to label relevant information in the text, and 

3. extracting and restructuring the meaningful information that can be found in the labelled text.

Although these programs complete three tasks, you may notice that there are more than three programs in this repository! This is mainly to narrow down the working number of articles before the Natural Language Processor is applied, and also to perform some basic descriptive statistics on the articles themselves, but is not related to building the structured data set. 

The final structured dataset produced by the programs can be found in the *Program Dataset* file in the **excel_sheets** directory. The same dataset in a more readable form is found in the *Program Dataset (Concise)* file.

All programs are written in Python 3. The Natural Langauge Processor employed is from *spaCy*, and *pymongo* is used for integration with MongoDB.

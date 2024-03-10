21k-3281
Rana Wahaj Ahmed
# Information Retrieval Assignment README
vIntroduction
This project implements an Information Retrieval (IR) system using a Boolean Model. It demonstrates how different indexes work in retrieving queries from a collection of research papers.

# Abstract
This project aims to create inverted and positional indexes for a set of research papers to facilitate a Boolean Model of IR. It preprocesses the documents, tokenizes them, and creates indexes for efficient query retrieval.
Tools and Libraries
The project utilizes the following tools and libraries:
•	Python 3.x
•	NLTK (Natural Language Toolkit)
o	Installation: pip install nltk
•	Tkinter (for GUI)
o	Pre-installed with Python
•	

# Dataset
The dataset consists of 20 research papers in English language extracted from PDFs.

# Approach to Solution
The solution involves the following steps:
•	Preprocessing: Removal of special characters, tokenization, and stemming.
•	Tokenizing: Splitting text into individual words or tokens.
•	Stemming: Reducing tokens to their root form using Porter Stemmer.
•	Inverted Index Creation: Inserting stemmed tokens into the inverted index.
•	Query Processing: Implementing Boolean query processing.
•	Positional Index Creation: Creating positional inverted index for proximity queries.
•	Proximity Query Processing: Retrieving documents with terms at specified proximity.
•	GUI Implementation: Creating a user-friendly interface using Tkinter.


# Data Structures
Inverted Index:
The inverted index is built using a dictionary data structure. Each term in the index serves as a key, with its corresponding value being a list of document IDs where the term appears. This structure allows for efficient lookup of documents containing specific terms. Additionally, the document IDs are sorted within the lists to facilitate faster retrieval and processing of Boolean queries.
Positional Index:
The positional inverted index also utilizes a dictionary-based approach. However, in addition to storing document IDs, it maintains the positions of terms within documents. For each term, the associated value is a list of dictionaries, where each dictionary represents a document ID and its corresponding list of term positions. This structure enables proximity queries by preserving the positional information of terms, allowing for precise retrieval of documents based on proximity constraints.


# Building Inverted Index
The stemmed_tokezized_and_inserted_to_inverted_index function tokenizes and stems each document and inserts the terms into the inverted index. It ensures that each term is associated with the respective document IDs.

# Processing Boolean Query
The query_processing function parses and evaluates Boolean queries. It utilizes stack-based evaluation to process AND, OR, and NOT operations efficiently.

# Creating Positional Index
The stemmed_tokezized_and_inserted_to_positional_inverted_index function constructs the positional inverted index. It stores each term along with the document ID and the positions of the term in the document.

# Processing Proximity Query
The proximity_query function retrieves documents containing terms with specified proximity. It compares the positions of terms in the positional inverted index to find matches.

# GUI Implementation
The GUI allows users to choose between Inverted Index and Positional Index. It provides input fields for queries and proximity values, along with buttons to execute the queries.

# Features
•	Preprocessing pipeline for document cleaning.
•	Support for Boolean queries with AND, OR, and NOT operations.
•	Positional index for proximity queries.
•	User-friendly GUI for easy interaction.

# How to Run Code
•	Install Python and required libraries.
•	Download the dataset and extract it.
•	Run the main script IR_assignment.py.
•	Make sure to change the path of directory in IR_assignment.py to the directory where you extracted dataset.




# How to Test It
Test Case 1: Boolean query   cancer AND learning 
Test Case 2: Boolean query    feature AND selection AND redundency
Test Case 3: Proximity query  NOT model 
Test Case 4: Boolean query   feature AND selection AND classification
Test Case 5: Proximity query  NOT classification  AND NOT feature 


Test Case 6: Boolean query   artificial intelligence (proximity 15) 
Test Case 7: Boolean query    overview historical (proximity 15)
Test Case 8: Proximity query  abstract number (proximity 15)





# Conclusion
This project demonstrates the implementation of an IR system using a Boolean Model. It provides efficient indexing techniques and query processing methods for retrieving relevant documents from a collection.


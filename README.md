# KHADEEJAH-
Introduction
The objective of this assignment was to develop a search engine using MapReduce, capable of processing a large dataset of Wikipedia articles. The search engine consists of several components, including word enumeration, document count, indexing, and query processing, each implemented as a separate MapReduce job.

Implementation Details
Word Enumeration (WordEnumeration class): This component extracts words from each document in the dataset and emits key-value pairs where the word is the key and the count is 1. It counts the occurrences of each word across all documents.

Document Count (DocumentCount class): This component calculates the total count of documents in the dataset and emits key-value pairs where each word is associated with its total count across all documents.

Indexer (Indexer class): This component builds an inverted index of the dataset, where each word is associated with a list of documents containing that word along with their term frequency (TF). It calculates the TF-IDF (Term Frequency-Inverse Document Frequency) score for each word-document pair.

Query Processor (QueryProcessor class): This component processes user queries against the index built by the Indexer. It calculates the TF-IDF score for each document containing the query terms and returns the ranked list of documents based on their relevance to the query.

Execution Workflow
Data Preparation: The Wikipedia dataset is provided as a zip file containing millions of articles. The file is read using the read_file_from_zip() function, which extracts the contents of the zip file.

MapReduce Jobs Execution: Each component of the search engine is implemented as a separate MapReduce job using the mrjob library. The jobs are executed sequentially, with each job processing the data emitted by the previous job.

Processing Pipeline:

Word Enumeration job extracts words and counts their occurrences.
Document Count job calculates the total count of documents.
Indexer job builds an inverted index with TF-IDF scores.
Query Processor job processes user queries against the index and returns relevant documents.
Challenges and Solutions
Zip File Parsing: Initially, there were issues with parsing the zip file containing the dataset. This was resolved by ensuring that the correct file path was provided and verifying the integrity of the zip file.

Query Flexibility: The search engine was initially hardcoded to process a single query string. To make the search engine more flexible, the query string was made a parameter that can be specified at runtime.

Conclusion
In conclusion, the developed search engine demonstrates the capabilities of MapReduce in processing large datasets efficiently. By implementing various components such as word enumeration, indexing, and query processing, the search engine can effectively retrieve relevant information from a vast collection of documents. Further enhancements could include optimization techniques for improving performance and scalability.

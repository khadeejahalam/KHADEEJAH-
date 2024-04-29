Project Report: Developing a Basic Search Engine with Apache Hadoop

Introduction:
The objective of this project was to develop a basic search engine using Apache Hadoop, focusing on distributed storage and processing capabilities. The project aimed to address the challenges of handling large datasets efficiently and demonstrate proficiency in the MapReduce paradigm.

Dataset Description:
The dataset used for this project was a subset of the English Wikipedia dump provided by Wikimedia, containing around 5 million articles. Each article was represented by four columns: ARTICLE_ID, TITLE, SECTION_TITLE, and SECTION_TEXT.

Approach:
1. **Understanding Apache Hadoop**: Before diving into development, we thoroughly reviewed Apache’s MapReduce Tutorial to understand the capabilities and configurations of MapReduce.

2. Organizing the Project: We organized the project by creating a public GitHub repository and following best practices for collaborative development. Incremental commits were made to track progress and avoid last-minute uploads.

3. Testing: To accelerate the development process, local testing was conducted on a smaller dataset to verify the correctness of the code.

4. Using Cloud Computing: While we had the option to implement a local Apache Hadoop cluster, we opted to explore cloud computing platforms like Microsoft Azure Cloud, leveraging their $200 free credit for the first month and clustering controls.

Development:
The development process can be divided into several key components:

1. Word Enumeration: This task involved scanning the corpus to generate a set of unique words and assigning a unique ID to each word. We implemented this task using MapReduce.

2. Document Count: Similar to Word Enumeration, Document Count calculated the Inverse Document Frequency (IDF) for each term or the number of documents in which each term appeared. It was also implemented with MapReduce.

3. Indexer: The Indexer computed a machine-readable representation of the entire document corpus by generating a TF/IDF representation for each document. This task was parallelized using MapReduce.

4. Query Processing: The Ranker Engine generated a vectorized representation for the query and calculated the relevance function between the query and each document using MapReduce.

File Paths:
- Input Path: `/Downloads/enwiki-20170820.csv`
- Word Enumeration Output Path: `/Home/word_enum_output`
- Document Count Output Path: `/Home/count_output`
- Indexer Output Path: `/Home/output_data`

Conclusion:
Through this project, we gained a solid understanding of big data processing fundamentals, distributed storage, and processing in Apache Hadoop. By leveraging the MapReduce paradigm, we successfully developed a basic search engine capable of handling large datasets efficiently. Moving forward, we aim to explore more advanced techniques and optimize performance for real-world applications.

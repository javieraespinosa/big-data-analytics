---
title: Instructions
linktitle: Instructions
type: book
weight: 20
toc: true
---

Given a collection of WARC files (and working in teams), you will have to:

1. Profile the content of the WARC files using a **quantitative approach**.
1. Explore the WARC files following a **data science approach** (i.e., hypothesis definition and validation).
1. Present your findings to a jury and peers during a **demofest**.

The following sections describe each of these phases in detail.

### Phase 1: Data Profiling

The objective of this phase is to help you get acquainted with the data (i.e., understand data structure, numerical values distribution, identifying outliers and null values). 

**Example**:

*   Count all media types contained in a WARC file (e.g., images, webpages, videos).
*   Plot the distribution of media types and their storage space usage.

<mark>The list of **statistics to compute** is in the [Queries](../queries) section.</mark>

> **Note**: For phase 1, the usage of **Apache Spark is mandatory**. 

### Phase 2: Data Exploration

Once you have a basic understanding of your dataset’s content, you can do a more in deep analysis following the scientific principle:

1. Formulate a `hypothesis` or `research question` according to the insight you obtained in the previous task.

1. Validate it using analytics techniques (e.g., natural language processing, machine learning, data mining, graph analytics). 

**Example**

* **Hypothesis**: Writers prefer public blog platforms (e.g., Blogger, WordPress) rather than creating/installing their websites from scratch.

* **Validation**: Web pages can contain a [meta tag](https://www.w3schools.com/tags/tag_meta.asp) describing the technology used for producing the web page. For instance: 

    ```html
        <meta name="generator" content="WordPress 3.0.1" /> 
    ```

    By counting the frequency of occurrences of this metatag in the dataset, it is possible to identify the most popular platforms used in the litterature community. 

> **Note**: For phase 2, the usage of **Apache Spark is optional**



### Phase 3: Demofest

The final phase consists of preparing a **presentation** and a **poster** to report your findings during the **demofest**. 

The presentation and poster must answer the following questions:

* What data do you work with (which data collection, its volume MB, etc.)?
* How did you divide the work among team members?
* What hypothesis did you propose? Why?
* What type of Spark operations did you apply (Did they work? Did they provide expected results?)
* What is the architecture of the infraestructure that you used? How the components and libraries interact with your Notebook(s)?
* Conclusions (go back to the learning outcomes and discuss which ones could be achieved or not through the exercise)

The presentation and poster should be complemented with a "demo" (e.g., using a notebook, a visualization tool or a video) showing your findings and the technical aspects involving your analysis. 

For this phase, you can <mark>**use the [Archives Unleashed New York Datathon](https://archivesunleashed.org/new-york/) projects as reference**</mark>.


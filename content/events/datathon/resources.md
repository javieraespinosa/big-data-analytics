---
title: Resources
linktitle: Resources
type: book
weight: 40
---

{{<toc>}}

### Dataset

{{% callout warning %}}
**Do not dowload the files using the web browser!**  
Use the code provided in the notebooks instead.
{{% /callout %}}

* [LIFRANUM datasets](https://drive.google.com/drive/folders/1mg1n3ojNwg8J61WWMdlO6M344EE6x1Yc?usp=sharing)
* [LIFRANUM input URLs](https://docs.google.com/spreadsheets/d/1A7NndS96T7c3nH45M2isuxb9c1awbfsw/edit?usp=sharing&ouid=111004351597243537219&rtpof=true&sd=true)

The WARC files are organized into 4 categories:

```
    WARC collection        Size
    ====================================
    Lifranum-method        2.84 Gb
    Cartoweb               336 Mb
    autres                 721 Mb
    Repo-ecriture-num      158 Mb
```
 
Each category name corresponds to the methodology used in the [LINFRANUM](https://projet-lifranum.univ-lyon3.fr/) project for defining the web crawler input list. For each `url` in the list, the web crawler retrieved:

* all ressources **1-level away** from the URLs used as input (see [LIFRANUM curated URLs](https://docs.google.com/spreadsheets/d/1A7NndS96T7c3nH45M2isuxb9c1awbfsw/edit?usp=sharing&ouid=111004351597243537219&rtpof=true&sd=true))

* all ressources (i.e., **recursively**) **within the same domain** 


### Notebooks

{{% callout note %}}
**Docker compatible notebooks** available at the **[Datathon repository](https://github.com/javieraespinosa/big-data-analytics-datathon)**.
{{% /callout %}}

* [Datathon WebArchives Demo](https://drive.google.com/file/d/1rKWC1OjhQNVIryelRTrX9uN3_E8yx92e/view?usp=sharing) notebook

* [Datathon WebArchives Quickstart](https://colab.research.google.com/drive/1aL5O2gQBvseLvp61ll_iU48n_HyHkY91?usp=sharing) notebook

* [Datathon WebArchives & Graph Analytics](https://github.com/javieraespinosa/big-data-analytics-datathon/blob/main/notebooks/03-WebArchives%20Graph%20Analytics.ipynb)

* [Collecting Data from Blogger via the API](https://colab.research.google.com/drive/1Ss260r20PwfQunYWvuLjZ2Ljcnu9kSlZ?usp=sharing) notebook

* [AUT text analysis](https://github.com/archivesunleashed/notebooks/blob/main/datathon-nyc/parquet_text_analyis_popline.ipynb) notebook



### Visualization Tools

* [Gephi](https://gephi.org/): Graph Visualization Platform
    - see [Gephi quick tutorial](https://gephi.org/tutorials/gephi-tutorial-quick_start.pdf)

* [Voyant tools](https://voyant-tools.org/): analysis environment for digital texts. 
    - see [Voyant Tutorial](https://voyant-tools.org/docs/#!/guide/tutorial)

* [Rawgraphs](https://www.rawgraphs.io/)

* [Plotly Express](https://plotly.com/python/plotly-express/) (python library)


### Online docs

* [Spark by Examples](https://sparkbyexamples.com)
* [Archives Unleashed Tools (0.91.0)](https://aut.docs.archivesunleashed.org/docs/0.91.0/home): Framework for analyzing web archives with Apache Spark
* [Spark (3.0.0)](https://spark.apache.org/docs/3.0.0/)
    * [Spark SQL Built-in Functions](https://spark.apache.org/docs/3.0.0/api/sql/index.html) 
    * [Spark Dataframe API](https://spark.apache.org/docs/3.0.0/api/python/pyspark.sql.html#pyspark.sql.DataFrame)


### Posters

* [Posters 2022](https://drive.google.com/drive/folders/11PvmV_nnVIX1aoCPT09o9FFQLW4Auln7?usp=share_link)

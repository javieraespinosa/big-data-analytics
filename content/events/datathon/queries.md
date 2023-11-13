---
title: "Profiling Queries (phase 1)"
linktitle: ⭐ Queries TODO
type: book
weight: 50
---

## Schema

To answer the profiling queries, you need to extend the dataframe returned by the AUT [.webpages()](https://aut.docs.archivesunleashed.org/docs/0.91.0/dataframe-schemas#web-pages) method as shown in the **extended schema** below. 

Note that:

* all new columns are derivated from the `url` column.
* the derivation can be done using the [tldextract](https://github.com/john-kurkowski/tldextract) and [urllib.parse](https://docs.python.org/3/library/urllib.parse.html) libraries.


**Extended Schema**

<pre>
df.webpages() 
|
|-- crawl_date                  
|-- mime_type_web_server        
|-- mime_type_tika              
|-- language                    
|-- content                     
|-- url:                         http://forums.news.cnn.com:80/
    |-- url_host_name:           forums.news.cnn.com
    |-- url_domain:              cnn
    |-- url_subdomain:           forums.news
    |-- url_tld:                 com
    |-- url_registered_domain:   cnn.com
    |-- url_domain_reversed:     com.cnn.news.forums
    |-- url_protocol:            http
    |-- url_host_port:           80
</pre>


`Optional` (see [HTTP header fields](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields))

<pre>
    url_host_ip         192.168.1.10                                cf. log.txt file
    content_length      Content-Length: 348                         cf. content’s HTTP header 
    content_charset     Content-Type: text/html; charset=utf-8      cf. content’s HTTP header
</pre>


## Queries

The following queries must be computed usning the WARC data collection of your choice.

### Domain names

1. Which are the **top registered domains** (see [example](https://commoncrawl.github.io/cc-crawl-statistics/plots/domains.html))?

    * `#` urls per domain
    * `%` domain urls in collection

1. Which are the **Top TLD & gTLDs domains** (see [example](https://commoncrawl.github.io/cc-crawl-statistics/plots/tld/latestcrawl.html))?

    * see [What Is a TLD?](https://kinsta.com/knowledgebase/what-is-a-tld/) for more information

1. Identify **domains having more than one TLD** (e.g., `amazon/.com/.fr`).

1. Identify **subdomains** for each domain.


### URLs

5. Compute the **distribution of the URLs components**. For instance:
    * `http`/`https`
    * `port` number

1. Count the **number of words** used in URLs
    * e.g., split URLs at `.` (dot) and `-` (hyphen)

### Web pages content

7. Compute the **list of languages** used in webpages?

1. Compute the **distribution** of: 
    * `MIME types` (see [example](https://commoncrawl.github.io/cc-crawl-statistics/plots/mimetypes))
    * `languages` (see [example](https://commoncrawl.github.io/cc-crawl-statistics/plots/languages))
    * `charsets` (see [example](https://commoncrawl.github.io/cc-crawl-statistics/plots/charsets)) (**optional**)

1. Identify **page titles** (**optional**)


### Collection & Hosts

10. **How many pages, per language**, were collected per host?

1. What is the **total number of bytes** that was collected by the crawler for each host?

1. What is the **ratio between the webpages and Web ressources** that were collected per host? (**optional**)

1. For each host, **list the servers IPs** to which the crawler interacted to. Then, determine whether custom domains point to any of these hosts (**optional**)


### Images

14. Identify the **largest/smallest image** in the dataset (`width` x `height`)

1. Identify the images appearing in the data collection under different names (i.e., **images having the same MD5 hash**)

1. Find images shared between more than 2 domains ([example](https://aut.docs.archivesunleashed.org/docs/0.91.0/image-analysis#pythondf))



### Web graph
15. Identify **domains with strong/weak connectivity**

### Multimedia
16. Compute the statistics of the multimedia files within the data collection (**optional**)
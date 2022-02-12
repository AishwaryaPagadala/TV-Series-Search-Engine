# TV-Series-Search-Engine

In this project we aim to build a TV-Series search engine using Wikipedia pages as the
knowledge base. We built a multi-threaded Web crawler using JSOUP that recursively traverses
through webpages using a given link and indexes them on the disk. We used Apache Lucene to
index the documents iteratively, and fetch results for user queries.


INSTRUCTIONS OF DEPLOYING CRAWLER AND LUCENE INDEXING 

1. To run the crawler run the crawler script file ./crawler.sh located in src/cralwer directory

$:./cralwer.sh <wikipedia-url> <output-directory-path> <depth - number of documents to crawl>
<number of threads>
Arguments:
<wikipedia-url> - eg: https://en.wikipedia.org/wiki/Friends
  
2. To run the Lucene Indexer run the indexer script file ./indexer.sh located in src/indexer
directory
  
$:./indexer.sh <input-directory> <outputdirectory> <query string>
Arguments:
#java indexer <input directory> <outputdirectory> <query string>
#<input directory> - location where crawler stored documents
#<output directory> - location where Indexer should store indexed files of FSDirectory()
#query string - query string
java indexer $1 $2 $3

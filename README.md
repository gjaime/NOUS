# NOUS : Construction and Querying of Dynamic Knowledge Graphs
Automated construction of knowledge graphs remains an expensive technical challenge that 
is beyond the reach for most enterprises and academic institutions. 
NOUS is an end-to-end framework for developing custom knowledge graphs driven 
analytics for arbitrary application domains. 
The uniqueness of our system lies A) in its combination of curated KGs along with 
knowledge extracted from unstructured text, B) support for advanced trending and explanatory 
questions on a dynamic KG, and C) the ability to 
answer queries where the answer is embedded across multiple data sources.

## Introduction	
NOUS provides complete suite of capabilities needed to build a domain specific knowledge graph 
from streaming data. This includes 
1) Natural language processing(NLP), 
2) Entity and relationship mapping, 
3) Confidence Estimation using Link Prediction. 
4) Rule Learning/Trend Discovery using Frequent Graph Mining
5) Question Answering using Graph Search 

### NOUS Project Structure :

* TripleExtractor: Contains NLP code, takes text document as input 
and produces triples of the for
subject, predicate, object 
* EntityDisambiguation : Entity linking to a given KB, (implements the algorithm in 
Collective Entity Linking in Web Text: A Graph-based Method, Han et al, SIGIR 2011)  
* Mining : Given a streaming graph, find frequent patterns
* Search : Given a attributed graph and entity pairs, return all paths 
* Link Prediction: Confidence estimation of each link in the graph using Naive Bayes 

### How to build and execute NOUS:
#### Prerequisites
* Java 1.7 OR above
* Maven 3.0 or above
* Apache Spark 2.0 OR above
* Scala 2.10
* HDFS File System (Optional)

### 2.2 Build
 Clone github repository 

` clone https://github.com/streaming-graphs/NOUS.git NOUS `

 Perform maven build in any of the module : `TripleExtractor` OR `Mining` Ex:
 
 ```bash
 cd [Repo_Home]/TripleExtractor
 mvn package
 ```
Here `[Repo_Home]` is the path to your cloned directory `NOUS`. 

### 2.3 Run Hello World
NOUS is organized into multiple modules that support the KB workflow. Each module 
contains README and data to run the examples.
For algorithmic and implementation details please refer to `NOUS paper in DesWeb 2017`. 

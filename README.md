# GML-on-Multi-Tables
The tutorial website for KDD 2024 tutorial Graph Machine Learning Meets Multi-Table Relational Data.

## What you will learn

While graph machine learning, and notably graph neural networks (GNNs), have gained immense traction in recent years, application is predicated on access to a *known input graph* upon which predictive models can be trained.  And indeed, within the most widely-studied public evaluation benchmarks such graphs are provided, with performance comparisons conditioned on curated data explicitly adhering to this graph.  However, in real-world industrial applications, the situation is often quite different. Instead of a known graph, data are originally collected and stored across multiple tables in a repository with ambiguous or incomplete relational structure.  Hence, there exists an gap from the raw data typically stored as multiple tables to the predictive architectures powered by GNNs or complementary tabular models.

In this tutorial, we review existing tools and strategies that can be combined to address the challenges of predictive modeling over relational data native to multiple tables, but with no explicit relational structure granted a priori.  This involves tracing a comprehensive path through related table discovery and fuzzy table joining, column alignment, automated relational database (RDB) construction, extracting graphs from RDBs, graph sampling, and finally, graph-centric trainable predictive architectures.  Although efforts to build deployable systems that integrate all of these components while minimizing manual effort remain in their infancy, this tutorial will nonetheless reduce barriers to entry and help steer the graph ML community towards promising research directions and wider real-world impact.

## Prerequisites

Although this tutorial is suitable for audiences with a general knowledge of machine learning, we specifically target researchers or scientists who have interest in training predictive models on relational data such as tables and graphs. Acquaintance with related techniques such as graph neural networks or tabular models is recommended to appreciate some of the finer details, but not required as we will summarize introductory material.

## Presenter bio


**Quan Gan** (https://github.com/BarclayII) is a Senior Applied Scientist at Amazon. His research interests include heterogeneous graph neural networks, algorithm unrolling, and the application of graph neural networks to domains such as tabular data and hypergraph networks. He obtained his Master's degree at New York University and Bachelor's degree at Fudan University.

![](https://jermainewang.github.io/assets/images/profile.png)
**Minjie Wang** (https://github.com/jermainewang) is a Senior Applied Scientist at Amazon. Previously he obtained his Ph.D. degree from New York University. His research focus is the interdisciplinary area of machine learning and system design, including building deep learning systems with high usability and performance, as well as applying machine learning in system optimization. He is also an open-source enthusiast, the founder and major contributor of many well-known open source projects such as Minerva, Apache MXNet, MinPy, and the Deep Graph Library (DGL). Among them, Minerva has been described as a "Modern AI Engine" by NVIDIA, while Apache MXNet was at one point the deep learning framework of choice at AWS; DGL is one of the most popular frameworks for developing and applying graph neural networks.

![](http://nebula.wsimg.com/7ca45e977c5a2f29ba48799cea45e86f?AccessKeyId=146529ABA7789B138972&disposition=0&alloworigin=1)
**David Wipf** is a Principal Research Scientist at Amazon and an IEEE Fellow. Prior to industry positions at Amazon and Microsoft Research, he received a B.S. degree with highest honors from the University of Virginia, and M.S. and Ph.D. degrees from the University of California, San Diego as an NSF Fellow in Vision and Learning in Humans and Machines. He was later an NIH Postdoctoral Fellow at the University of California, San Francisco. His current research interests include deep generative models and graph neural networks. He is the recipient of numerous fellowships and awards including the 2012 Signal Processing Society Best Paper Award. He has previously delivered 5 tutorials at top-tier conferences.

## Tutorial outline

The study of learning from relational data, encompassing formats such as graphs and tables, boasts a long-standing history and a wealth of literature. However, the landscape of real-world relational data presents many more challenges as an explicit schema or clear structure is often lacking, unlike the graph or tabular benchmarks often studied in academic settings. Recognizing these hurdles, our tutorial is structured into three distinct sessions, each designed to address the core challenges encountered when working with such complex data. These sessions will guide participants through the critical processes of structural discovery and the selection of predictive architectures suitable for a variety of data types. Our aim is to present a practical, end-to-end learning pipeline that attendees can adapt to tackle a wide array of problems.

### Session.1: Introduction to graph-centric predictive pipelines for multi-table data

We will start with an overview of different multi-table data scenarios such as RDBs, data lakes, semi-structured data, etc., accompanied by practical business scenarios such as recommender systems, abnomaly detection and so on to connect with the audience. We then overview general-purpose graph-centric predictive pipelines for predictive modeling over multi-table data, with details to follow in later sessions below. % To make the description more concrete, we will present several concrete realizations of this framework which relate our topics with the well-known literature on graph neural networks, feature engineering and AutoML.

### Session.2: From multi-table data to RDBs and graphs

We will first introduce concrete examples whereby data schema information is missing and illustrate its impact. We will then discuss the various schema discovery steps and available tools used to transition from raw multi-table data into RDBs with explicit relational structure.  For ML researchers who are not familiar with RDBs, we will have a gentle introduction to the relevant concepts including foreign keys, primary keys, entity-relationship diagrams, etc.  Finally, we will detail multiple ways for extracting heterogeneous graphs from RDBs with different characteristics.

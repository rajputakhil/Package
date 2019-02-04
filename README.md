Python Package
====

## Instructions to execute a Python package having two funcitons
1. Create a folder named 'package'
2. Create an empty file titled '__int__.py' (this will tell the interpreter that its a Python package)
3. Create a file named 'fn1.py' with a function in it.
4. Create a file named 'fn2.py' with another function in it.
5. Create a file named 'test.py' with a set of instructions to execute fn1 and fn2 functions
6. Open Terminal and Log into the folder 'Package'
7. Type in the follwoing command to execute the test.py file:

```bash
$ git clone https://github.com/rajputakhil/package.git
$ cd package
$ chmod a+x test.py
```

8. Type "python test.py" to execute the Python code





# Introduction

ADAM is a library and command line tool that enables the use of [Apache
Spark](https://spark.apache.org) to parallelize genomic data analysis across
cluster/cloud computing environments. ADAM uses a set of schemas to describe
genomic sequences, reads, variants/genotypes, and features, and can be used
with data in legacy genomic file formats such as SAM/BAM/CRAM, BED/GFF3/GTF,
and VCF, as well as data stored in the columnar
[Apache Parquet](https://parquet.apache.org) format. On a single node, ADAM
provides competitive performance to optimized multi-threaded tools, while
enabling scale out to clusters with more than a thousand cores. ADAM's APIs
can be used from Scala, Java, Python, R, and SQL.

## Why ADAM?

Over the last decade, DNA and RNA sequencing has evolved from an expensive,
labor intensive method to a cheap commodity. The consequence of this is
generation of _massive amounts of genomic and transcriptomic data_. Typically,
tools to process and interpret these data are developed with a focus on
excellence of the results generated, not on __scalability__ and
__interoperability__. A typical _sequencing workflow_ consists of a suite
of tools from quality control, mapping, mapped read preprocessing, to variant
calling or quantification, depending on the application at hand. Concretely,
this usually means that such a workflow is implemented as tools glued together
by scripts or workflow descriptions, with data written to files at each step.
This approach entails three main bottlenecks: 

  1. __scaling the workflow__ comes down to scaling each of the individual
     tools,
  2. the __stability of the workflow__ heavily depends on the consistency of
     intermediate file formats, and
  3. __writing to and reading from disk__ is a major slow-down.

We propose here a transformative solution for these problems, by replacing
ad-hoc workflows by the [ADAM framework](http://bdgenomics.org/), developed
in the [Apache Spark](http://spark.apache.org/) ecosystem.

ADAM enables the high performance in-memory cluster computing functionality
of Apache Spark on genomic data, ensuring efficient and fault-tolerant
distribution based on data parallelism, without the intermediate disk
operations required in traditional distributed approaches.

Furthermore, the ADAM and Apache Spark approach comes with an additional
benefit. Typically, the endpoint of a sequencing pipeline is a file with
processed data for a single sample: e.g. variants for DNA sequencing, read
counts for RNA sequencing, etc. The real endpoint, however, of a sequencing
experiment initiated by an investigator is __interpretation__ of these data
in a certain context. This usually translates into (statistical) analysis of
multiple samples, connection with (clinical) metadata, and interactive
visualization, using data science tools such as R, Python, Tableau and
Spotfire. In addition to scalable distributed processing, Apache Spark also
allows __interactive data analysis__ in the form of analysis notebooks
(Spark Notebook, Jupyter, or Zeppelin), or direct connection to the data in
R and Python.

# Getting Started

## Building from Source

You will need to have [Apache Maven](http://maven.apache.org/) version 3.1.1 or
later installed in order to build ADAM.

> **Note:** The default configuration is for Hadoop 2.7.3. If building against
> a different version of Hadoop, please pass `-Dhadoop.version=<HADOOP_VERSION>`
> to the Maven command.

```bash
$ git clone https://github.com/bigdatagenomics/adam.git
$ cd adam
$ mvn install
```

### Installing Spark

You'll need to have a Spark release on your system and the `$SPARK_HOME` environment variable pointing at it;
prebuilt binaries can be downloaded from the [Spark website](http://spark.apache.org/downloads.html).

# Documentation

ADAM's documentation is available at http://adam.readthedocs.io.

ADAM's core API documentation is available at http://javadoc.io/doc/org.bdgenomics.adam/adam-core-spark2_2.11.

# The ADAM/Big Data Genomics Ecosystem

ADAM builds upon the open source [Apache Spark](https://spark.apache.org),
[Apache Avro](https://avro.apache.org), and [Apache
Parquet](https://parquet.apache.org) projects. Additionally, ADAM can be
deployed for both interactive and production workflows using a variety of
platforms.

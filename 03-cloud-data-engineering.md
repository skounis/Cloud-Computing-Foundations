# Cloud Data Engineering
[Cloud Data Engineering](https://www.coursera.org/learn/cloud-data-engineering-duke/home/week/1) Duke University

## Week I
### Overview - Welcome to the course
* Create pipelines
* Serverless
* Batch or Streaming
* Big data
* ETL Pipelines

#### Objectives
* Data Engineering Applications in the Cloud
* Best practices with regard to end of the Moors law
* Best practices for big data solutions

#### Resources
* [AWS Academy](https://aws.amazon.com/training/a`wsacademy/) 
* [Google Qwiklabs](https://go.qwiklabs.com/)
* [Microsoft Learn](https://learn.microsoft.com/en-us/training/)
* [AWS and Lambda - Beginner’s Guide to Writing AWS Lambda Functions in Python](https://github.com/noahgift/awslambda)

#### Project overview
Serverless Data Engineering Pipeline
* Timer kicks off a serverless job - CloudWatch Timer
* Producer Lambda pulls from Serverless Database - DynamoDB
* A queue gets data - SQS 
* Consumer Lambda is listening for SQS events
* Sentiment Analysis - AWS Comprehend
* Store - S3 

### End of Moore's Law

#### Objectives
* Approaches to concurrency. Network, Process, GPU
* Chip types. 
* ASIC use cases: Application Specific Integrated Circuit
* CUDA: Compute Unified Device Architecture, an API for NVidia

#### Python and Concurrency
* Python locks the threads to one core - GIL
* Use the cloud for building a concurrent system. AWS Lambda and SQS


#### The end of Moore's Law
> The end of growth of single program speed really occurred right around this period of the last 40 years. 
> -- Dr. David Paterson 

* CPU is designed to do a lot of things. A general purpose unit
* GPU is desinged to do things in parallel
* TPU is designe for parallelization for a specific workload

#### CUBA and Numba
https://numba.pydata.org/

Notes and links
https://github.com/noahgift/cloud-data-analysis-at-scale/blob/master/topics/end-of-moores-law.md

Google Colab: https://github.com/noahgift/cloud-data-analysis-at-scale/blob/master/GPU_Programming.ipynb


#### What is ASIC
Application specific integrated circuit. Chip for a purpose. Designed for one thing/purpose
* TPU: Tensor procesing unit.
* GPU: Graphics programming - Very parallel operations
* NCS: Intel Neural Compute Stick


#### Taking Advantage of Colab Pro
Profesional version of Colab

#### The End of Moore's Law
From 
* https://noahgift.github.io/cloud-data-analysis-at-scale/topics/end-of-moores-law.html

References
* https://storage.googleapis.com/nexttpu/index.html
* Step by step example: Just in Time compiler (JIT) or a GPU using a library like numba and a hosted runtime like Google Colab.
    * https://github.com/noahgift/cloud-data-analysis-at-scale/blob/master/GPU_Programming.ipynb
    

### Building Distributing Systems
#### Introduction
* Instumentation
* CAP Theorem
* Amdahl's Law
* Elasticity: Response to higher load 
* Highly available: Respond to a request despite the increased trafic 
* Debuggin Python

Objectives
* Develop distributed systems that apply software engineering best practices

#### Logging and Instrumentation Distributed Systems
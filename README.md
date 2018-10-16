# Text summarization and visualization using watson studio

We will demonstrate a methodology to summarize & visualize text using Watson Studio. Text summarization is the process of creating a short and coherent version of a longer document. There are two methods to summarize the text, extractive & abstractive summarization. We will focus on extractive summarization which involves the selection of phrases and sentences from the source document to make up the new summary. Techniques involve ranking the relevance of phrases in order to choose only those most relevant to the meaning of the source. Some of the advantages of text summarization are below as per the [source](https://machinelearningmastery.com/gentle-introduction-text-summarization) 

`Summaries reduce reading time.
When researching documents, summaries make the selection process easier.
Text summarization improves the effectiveness of indexing.
Text summarization algorithms are less biased than human summarizers.
Personalized summaries are useful in question-answering systems as they provide personalized information.
Using automatic or semi-automatic summarization systems enables commercial abstract services to increase the number of texts they are able to process.`

When the reader has completed this code pattern, they will understand how to:

* Quickly summarize the text from documents & news feeds.
* Create topic modeling on the text to extract important topics.
* Create visualizations for better understanding of the data.
* Analyze the text for further processing to generate recommendations.

# Architecture Diagram

![](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/blob/master/doc/source/images/architecture.png)

1.  User logs into Watson Studio, creates an instance which includes object storage.
2.  User uploads the data file to the object storage.
3.  User imports a Jupyter Notebook from the URL.
4.  User runs the processing techniques & creates a statistical model for topics in the notebook.
5.  User explores the visualization in the notebook and can export the output to object storage.

## Included components

* [IBM Watson Studio](https://www.ibm.com/cloud/watson-studio): Analyze data using RStudio, Jupyter, and Python in a configured, collaborative environment that includes IBM value-adds, such as managed Spark.

* [IBM Cloud Object Storage](https://console.bluemix.net/catalog/services/cloud-object-storage): An IBM Cloud service that provides an unstructured cloud data store to build and deliver cost effective apps and services with high reliability and fast speed to market. This code pattern uses Cloud Object Storage.

* [Jupyter Notebooks](http://jupyter.org/): An open-source web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text.

## Featured technologies

* [Data Science](https://developer.ibm.com/code/technologies/data-science/): Systems and scientific methods to analyze structured and unstructured data in order to extract knowledge and insights.
* [Analytics](https://developer.ibm.com/code/technologies/analytics/): Analytics delivers the value of data for the enterprise.
* [Python](https://www.python.org/): Python is a programming language that lets you work more quickly and integrate your systems more effectively.

# Watch the Video

[![](http://img.youtube.com/vi/LZYnfrnkmwk/0.jpg)](https://youtu.be/LZYnfrnkmwk)


# Steps

Follow these steps to setup and run this code pattern. The steps are
described in detail below.

1. [Create an account with IBM Cloud](#1-create-an-account-with-ibm-cloud)
1. [Create a new Watson Studio project](#2-create-a-new-watson-studio-project)
1. [Create the notebook](#3-create-the-notebook)
1. [Add the data](#4-add-the-data)
1. [Insert the credentials](#5-insert-the-credentials)
1. [Run the notebook](#6-run-the-notebook)
1. [Analyze the results](#7-analyze-the-results)

## 1. Create an account with IBM Cloud

Sign up for IBM [**Cloud**](https://console.bluemix.net/). By clicking on create a free account you will get 30 days trial account.

## 2. Create a new Watson Studio project

Sign up for IBM's [Watson Studio](http://dataplatform.ibm.com/). 

Click on New project and select Data Science as per below.

![](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/blob/master/doc/source/images/new_project.PNG)

Define the project by giving a Name and hit 'Create'.

![](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/blob/master/doc/source/images/define_project.PNG)

By creating a project in Watson Studio a free tier ``Object Storage`` service will be created in your IBM Cloud account.

## 3. Create the notebook

* Open [IBM Watson Studio](https://dataplatform.ibm.com).
* Click on `Create notebook` to create a notebook.
* Select the `From URL` tab.
* Enter a name for the notebook.
* Optionally, enter a description for the notebook.
* Enter this Notebook URL: https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/blob/master/notebook/Text_Summarize_and_Visualize.ipynb
* Select the runtime (1vCPU and 4GBRAM)
* Click the `Create` button.

![](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/blob/master/doc/source/images/create_notebook.PNG)

## 4. Add the data

[Clone this repo](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio)
Navigate to [data](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/tree/master/data) and save the file on the disk.

Use `Find and Add Data` (look for the `10/01` icon)
and its `Files` tab. From there you can click
`browse` and add data file from your computer.

![](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/blob/master/doc/source/images/add_file.png)

Note: The data file is in the `data` directory

## 5. Insert the credentials

Select the cell below `Read the Data` section in the notebook.

Use `Find and Add Data` (look for the `10/01` icon) and its `Files` tab. You should see the file names uploaded earlier. Make sure your active cell is the empty one created earlier. Select `Insert to code` (below your file name). Click `Insert credentials` from drop down menu.

![](https://github.com/IBM/text-summarization-and-visualization-using-watson-studio/blob/master/doc/source/images/insert_cred.png)

## 6. Run the notebook

When a notebook is executed, what is actually happening is that each code cell in
the notebook is executed, in order, from top to bottom.

Each code cell is selectable and is preceded by a tag in the left margin. The tag
format is `In [x]:`. Depending on the state of the notebook, the `x` can be:

* A blank, this indicates that the cell has never been executed.
* A number, this number represents the relative order this code step was executed.
* A `*`, this indicates that the cell is currently executing.

There are several ways to execute the code cells in your notebook:

* One cell at a time.
  * Select the cell, and then press the `Play` button in the toolbar.
* Batch mode, in sequential order.
  * From the `Cell` menu bar, there are several options available. For example, you
    can `Run All` cells in your notebook, or you can `Run All Below`, that will
    start executing from the first cell under the currently selected cell, and then
    continue executing all cells that follow.
    
## 7. Analyze the results





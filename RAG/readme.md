# Retrieval-Augmented Generation
# In-Context Learning
Generate product description given a list of product attributes. Use retrieval-augmented generation, where you provide an LLM with examples before asking it to generate a description. Using OpenAI embeddings, select the example of a product that's similar to the one you need to generate a description for. 

## Notebook 
The notebook is supposed to be run on Microsoft Fabric, for which you need an active subscription. You also need an Azure subscription to create a resource group for PostgreSQL database and a Key Vault, and an OpenAI API key. The notebook can be imported through "Data Engineering" or "Data Science" view on Microsoft Fabric, and should be attached to an existing Lakehouse (make sure to make it a default Lakehouse for that notebook, too).

Run *RAG_data_prep.ipynb* first to preprocess the data, then run *RAG_main.ipynb*.

## Data
Two .csv files should be put in the *data/* folder for the code to work: *attributes.csv* and *product_descriptions.csv*. A small, truncated version of both files (attributes/descriptions for 10 products) is provided for user convenience.
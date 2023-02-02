# E-commerce data streaming platform
Data streaming platform using Kafka, Spark Streaming and MongoDB via Docker-Compose

The data used here is a e-commerce data from Kaggle, available here :
https://www.kaggle.com/datasets/carrie1/ecommerce-data

The goal is to build an end-to-end platform from the data transformation to the data storage into MongoDB.

There will be a last part which consists in visualising the documents (stored in MongoDB) through a Streamlit app.

## Project steps
- loading and transforming the data from csv into json format
- creating the API, used to ingest data into Kafka
	- in a first time, it will be used with PostMan in order to unitary test our API
	- later, the input client API will be used to send the "real" data into the end-to-end-platform
- building and deploying the API container with Kafka, using docker-compose
- adding the Spark Streaming layer (inside a Jupyter notebook container)
- starting the mongodb container
- preparing the MongoDB database and collection
- create the Python script to be able to process the data into Spark from Kafka and to write it in MongoDB
- create the input client API, used to retrieve the original data and send it to the ingest API
- create and run the Streamlit app, used to visualise our data
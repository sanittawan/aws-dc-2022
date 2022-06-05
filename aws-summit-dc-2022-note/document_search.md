## Search and Discovery with NLP
main service: Amazon Kendra

- most data are unstructured e.g. images, documents, audio files 
- challenges are inccurate keyword, implementation, maintenance 

Tradition search returns list of documents, but Kendra can give better answer by understanding natural language and returns document ranking
- provides search index
- does not need code or ML experience
- Kendra also provides connectors like S3

### Tune search relevance
1. incremental learning. Learn from previous interactions with re-ranking documents
2. tuning, content boosting and synonyms. Boost based on index sources, authors, freshness, import custom business-related synonyms

### Use cases
- enterprise search for internal web
- customer service like call center assistant, website search, self-service 
- embedded search

### Kendra system
- data ingestion > result optimization > deployment
- textract used for pdf that are not OCR, Rekognition for images, Comprehend etc. 
- Kendra provides dashboard with metrics such as misses, top search, top key words
- comparison with Amazon Elasticsearch and Kendra
- index can be updated according to your customized schedule
- natural language cabability should enable Kendra to understand grammatically incorrect search phrases
- Kendra also come with free tier
- DIY by going to AWS AI services and Amazon SageMaker
- or work with AWS professional services and solutions lab
- it might not be as opened as one thinks. Might need to check the token and access system and connection with Cognito

### Steps
1. create the search index 
    - set IAM role. First thing is giving the right permission
    - encryption
    - Kendra developer edition (testing) and enterprise (for production)
2. add data 
    - data sources can be in multiple languages
    - Once added, Kendra will crawl the data source to synchronize the data sources
3. search
    - you can give feedback on the search results by clicking thumb up or down


### Q&A
- How to deal with search term hierachy. but there is advanced tuning like "sematic search"
- What's the detail about searhching across many languages

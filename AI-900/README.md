# AI-900 Study Notes

AI-900 Exam guide: https://docs.microsoft.com/en-gb/learn/certifications/exams/ai-900

LEARNING PATH 1: Get started with artificial intelligence (AI-900) 

LEARNING PATH 2: Explore visual tools for machine learning (AI-900)

LEARNING PATH 3: Explore computer vision (AI-900)



---

## LEARNING PATH 1: Get started with artificial intelligence (AI-900) 

### [Get started with artificial intelligence](https://learn.microsoft.com/en-us/training/paths/get-started-with-artificial-intelligence-on-azure/)

### What is AI?

AI - Software that imitatates human behavior and capabilities

- Machine Learning
- Anomaly Detection
- Computer Vision
- Natural Language Processing
- Knowledge Mining

### Understand machine learning

Use massive amount of data for training machine learning models that can predict future outcomes

Machine learning in Microsoft Azure

- Automated Machine learning
- Azure Machine learning designer
- Data and compute management
- Pipelines

### Understanding anomaly detection

Analyses data overtime and detect unusual changes 

- Anomaly Detection service API

### Understand computer vision

AI dealing with Visual Processing

Common Computer Vision tasks,

- Image Classification
- Object Detection
- Semantic Segmentation
- Image Analysis
- Face Detection
- OCR - Optical Character Recognition

Computer Vision in Microsoft Azure

- Computer Vision
- Custom Vision
- Face
- Form Recognition

### Understand natural language processing

AI dealing with undesrtanding written and spoken language

Natural language processing (NLP) in Microsoft Azure

- Language
- Translator
- Speech
- Azure Bot

### Understand knowledge mining

Extracting information from large amount of unstructured data

Knowledge mining in Microsoft Azure

- Azure Cognitive Search

### Challenges and risks with AI

- Bias results
- Errors causing harm
- Data exposure 
- Not compatible for everyone
- User's need to trust complexity
- Liability issues for decisions

### Understand Responsible AI

- Fairness - not biased for anyone
- Reliability and safety
- Privacy and Security 
- Inclusiveness - must empower everyone
- Transparency - user's should be aware
- Accountability - governance structure

## LEARNING PATH 2: Explore visual tools for machine learning (AI-900) 

### [Use Automated Machine Learning in Azure Machine Learning](https://learn.microsoft.com/en-us/training/modules/use-automated-machine-learning/)

### Machine Learning

Uses mathematics and statistics to create a model that can predict future unknown values

Supervised machine learning approach

- Regression: predict a continuous value
- Classification: determine a binary class label

Unsupervised machine learning approach

- Clustering: used to determine labels by grouping similar information into label groups

### Azure Machine Learning studio

Train and deploy effective with a lot of simplicity and automation

You must create Workspace in your Azure subscription first

Computer Resources you can create,

- Computer Instances
- Computer Clusters
- Inference Clusters
- Attached Compute

Azure Automated Machine Learning

- Automated machine learning capability that automatically tries multiple pre-processing techniques and model-training algorithms in parallel

...

WIP

## LEARNING PATH 3: Explore computer vision (AI-900) 

### [Analyze images with the Computer Vision service](https://learn.microsoft.com/en-us/training/modules/analyze-images-computer-vision/)

Azure resources for Computer Vision

- Computer Vision
- Cognitive Services (includes Computer Vision and other capabilities ex: Text & Language)

Computer Vision capabilities

- Describe image
- Tagging Visual features
- Detecting Objects
- Detecting Brands
- Detecting Faces
- Categorizing an image
- Detect domain specific content
- OCR
- Generate thumbnails, moderate content, etc

### [Classify images with the Custom Vision service](https://learn.microsoft.com/en-us/training/modules/classify-images-custom-vision/)

Uses of image classification

- Product identification 
- Disaster investigation
- Medical diagnosis

Classification - predict which category or class something belogs to.
Image classification is a machine learning technique.

Convolutional neural networks (CNNs) - to uncover patterns in the pixels that correspond to particular classes

Azure resources for Custom Vision

- Custom Vision - dedicated resource can be training, a prediction, or both
- Cognitive Services - eneral cognitive services resource, includes Custom Vision with many other

It is possble to mix and match, ex: use a dedicated Custom Vision resource for training, but deploy your model to a Cognitive Services resource for prediction. This can only be done in same region! 

Model evaluation

- Precision - the model predicted 10 images are oranges, but only 8 were actually oranges, then the precision is 0.8 (80%)
- Recall - the model prediction 7 images are apples, but there are 10 images of apples, then the recall is 0.7
- AP - Average prediction combination of previous two

### [Detect objects in images with the Custom Vision service](https://learn.microsoft.com/en-us/training/modules/detect-objects-images-custom-vision/)

Uses of object detection

- Detecting tumors
- Driver assistance
- Checking for building safety

Use Custom Vision or Congnitive Services resource, but better with a mix

To train an object detection model, you need to create a Custom Vision project based on your training resource

Steps:
Image tagging - Custom Vision portal provides a graphical interface, for training data set up
Model training and evaluation
Using the model for prediction

### [Detect and analyze faces with the Face service](https://learn.microsoft.com/en-us/training/modules/detect-analyze-faces/)

Face detection

Facial analysis - information on facial features
Facial recognition - indentify a paticular face

Microsoft Azure provides multiple cognitive services,

- Computer Vision - basic face detection
- Video Indexer - Detect faces in a video
- Face - Blur, Exposure, Glasses, Head Pose, Noise, Occlusion

Following are restricted and customers should fill intake form,

- The ability to compare faces for similarity
- The ability to identify named individuals in an image

### [Read text with the Computer Vision service](https://learn.microsoft.com/en-us/training/modules/read-text-computer-vision/)

Use the Computer Vision service to read text

The Read API - scanned large documents
- This is an asynchronous service
- Structure returned - Pages, Lines, Words

### [Analyze receipts with the Form Recognizer service](https://learn.microsoft.com/en-us/training/modules/analyze-receipts-form-recognizer/)

Process receipt or invoices data

Azure Form Recognizer
Two options,
- Pre built receipt model
- Custom model - trained with your data

## LEARNING PATH 3: Explore natural language processing (AI-900) 

### [Analyze text with the Language service](https://learn.microsoft.com/en-us/training/modules/analyze-text-with-text-analytics-service/)

Evaluate different aspects of a document or phrase, in order to gain insights into the content of that text

In Microsoft Azure, the Language cognitive service 

- Determine language of a document
- Perform sentiment analysis
- Extract key phrases
- Identify and categorize entities

### [Recognize and synthesize speech](https://learn.microsoft.com/en-us/training/modules/recognize-synthesize-speech/)

Two main capabilities:
- Speech recognition - acoustic model -> language model -> to text
- Speech synthesis - tokenizes text -> prosodic units (such as phrases, clauses, or sentences) 

Azure resources for the Speech service
- Speech resource - only for speech service
- Cognitive Services resource - including other services as well

Available APIs,
- Speech-To-Text-API - Real time transcription, batch transcription features
- Text-To-Speech-API - Speech synthesis voices features

 

...

WIP

---

That's all the notes, good luck with the AZ-204 exam! ^_^ 

-Udara Alwis

# AWS Certified AI Practitioner (AIF-C01) Exam Questions

### Question #31

**Question:** An AI practitioner has a database of animal photos. The AI practitioner wants to automatically identify and categorize the animals in the photos without manual human effort. Which strategy meets these requirements?

* **A. Object detection**
* B. Anomaly detection
* C. Named entity recognition
* D. Inpainting

**Correct Answer:** **A. Object detection**

**Exam Perspective Hint:** Object detection locates and classifies objects within image or video data automatically. Named Entity Recognition (NER) is an NLP technique for text, not images. Inpainting is used to reconstruct or fill in missing/damaged parts of an image.


### Question #32

**Question:** A company wants to create an application by using Amazon Bedrock. The company has a limited budget and prefers flexibility without long-term commitment. Which Amazon Bedrock pricing model meets these requirements?

* **A. On-Demand**
* B. Model customization
* C. Provisioned Throughput
* D. Spot Instance

**Correct Answer:** **A. On-Demand**

**Exam Perspective Hint:** On-Demand pricing lets you pay per token with zero long-term commitment. Provisioned Throughput requires 1-month or 6-month term commitments for guaranteed capacity.


### Question #33

**Question:** Which AWS service or feature can help an AI development team quickly deploy and consume a foundation model (FM) within the team's VPC?

* A. Amazon Personalize
* B. **Amazon SageMaker JumpStart**
* C. PartyRock, an Amazon Bedrock Playground
* D. Amazon SageMaker endpoints

**Correct Answer:** **B. Amazon SageMaker JumpStart**

**Exam Perspective Hint:** **Amazon SageMaker JumpStart** provides **Pre-Trained Model**, `That can you Quickly Deploy with few clicks`.

* • It deploys the model directly into your dedicated Amazon SageMaker infrastructure, the model runs entirely within your team's Virtual Private Cloud (VPC), giving you full control over network security, data isolation, and private VPC endpoints.

* **Amazon SageMaker EndPoint** - You can consume Model after deployment.

### Question #34

**Question:** How can companies use large language models (LLMs) securely on Amazon Bedrock?

* **A. Design clear and specific prompts. Configure AWS Identity and Access Management (IAM) roles and policies by using least privilege access.**
* B. Enable AWS Audit Manager for automatic model evaluation jobs.
* C. Enable Amazon Bedrock automatic model evaluation jobs.
* D. Use Amazon CloudWatch Logs to make models explainable and to monitor for bias.

**Correct Answer:** **A. Design clear and specific prompts. Configure AWS Identity and Access Management (IAM) roles and policies by using least privilege access.**

**Exam Perspective Hint:** Security on AWS centers around access control—specifically, configuring IAM permissions following the principle of least privilege.


### Question #35

**Question:** A company has terabytes of data in a database that the company can use for business analysis. The company wants to build an AI-based application that can build a SQL query from input text that employees provide. The employees have minimal experience with technology. Which solution meets these requirements?

* **A. Generative pre-trained transformers (GPT)**
* B. Residual neural network
* C. Support vector machine
* D. WaveNet

**Correct Answer:** **A. Generative pre-trained transformers (GPT)**

**Exam Perspective Hint:** GPT models (LLMs) excel at natural language processing tasks, such as translating natural human language instructions directly into executable SQL queries.

**Correct Answer: A. Generative pre-trained transformers (GPT)**

### Detailed Explanation

The task described is **Text-to-SQL generation** (converting plain English queries from non-technical employees into valid SQL syntax to query a database).

* **Generative Pre-trained Transformers (GPT):** GPT models are large language models (LLMs) trained to process natural language inputs and generate structured outputs, including programming languages and database query languages like SQL. They allow non-technical employees to simply type plain text questions (e.g., *"Show me total sales for last month"*) and generate the corresponding SQL code (`SELECT SUM(sales) FROM transactions WHERE month = 'last_month'`) automatically.


### Why the Other Options Are Incorrect

* **B. Residual neural network (ResNet):** These are deep convolutional neural networks primarily designed for **computer vision tasks** (such as image classification and object recognition). They cannot process or translate natural language into SQL code.

* **C. Support vector machine (SVM):** SVM is a traditional supervised classical ML algorithm used for **classification or regression** tasks on tabular data. It cannot generate structured code sequences or interpret complex natural language queries.

* **D. WaveNet:** WaveNet is a deep generative model specifically designed for **generating raw audio signals** (used in Text-to-Speech models like Amazon Polly). It has no capability for code generation or SQL translation.

### Exam Hint for AIF-C01

Whenever a scenario asks for converting **natural language text into code, SQL queries, or structured scripts** for non-technical users, always choose **Generative Pre-trained Transformers (GPT)** or **Large Language Models (LLMs)**.


### Question #36

**Question:** A company built a deep learning model for object detection and deployed the model to production. Which AI process occurs when the model analyzes a new image to identify objects?

* A. Training
* **B. Inference**
* C. Model deployment
* D. Bias correction

**Correct Answer:** **B. Inference**

**Exam Perspective Hint:** Inference is the runtime phase when a trained model processes new, unseen data to generate predictions or classifications.


### Question #37

**Question:** An AI practitioner is building a model to generate images of humans in various professions. The AI practitioner discovered that the input data is biased and that specific attributes affect the image generation and create bias in the model. Which technique will solve the problem?

* **A. Data augmentation for imbalanced classes**
* B. Model monitoring for class distribution
* C. Retrieval Augmented Generation (RAG)
* D. Watermark detection for images

**Correct Answer:** **A. Data augmentation for imbalanced classes**

**Exam Perspective Hint:** Data augmentation generates synthetic training examples to balance underrepresented classes or demographics, mitigating data-driven bias.


### Question #38

**Question:** A company is implementing the Amazon Titan foundation model (FM) by using Amazon Bedrock. The company needs to supplement the model by using relevant data from the company's private data sources. Which solution will meet this requirement?

* A. Use a different FM.
* B. Choose a lower temperature value.
* **C. Create an Amazon Bedrock knowledge base.**
* D. Enable model invocation logging.

**Correct Answer:** **C. Create an Amazon Bedrock knowledge base.**

**Exam Perspective Hint:** Knowledge Bases for Amazon Bedrock implement RAG (Retrieval-Augmented Generation), allowing foundation models to securely fetch context from private data sources.


### Question #39

**Question:** A medical company is customizing a foundation model (FM) for diagnostic purposes. The company needs the model to be transparent and explainable to meet regulatory requirements. Which solution will meet these requirements?

* A. Configure the security and compliance by using Amazon Inspector.
* **B. Generate simple metrics, reports, and examples by using Amazon SageMaker Clarify.**
* C. Encrypt and secure training data by using Amazon Macie.
* D. Gather more data. Use Amazon Rekognition to add custom labels to the data.

**Correct Answer:** **B. Generate simple metrics, reports, and examples by using Amazon SageMaker Clarify.**

**Exam Perspective Hint:** Amazon SageMaker Clarify provides tools for detecting potential bias and providing model explainability reports and feature importance metrics.


### Question #40

**Question:** A company wants to deploy a conversational chatbot to answer customer questions. The chatbot is based on a fine-tuned Amazon SageMaker JumpStart model. The application must comply with multiple regulatory frameworks. Which capabilities can the company show compliance for? (Choose two.)

* A. Auto scaling inference endpoints
* **B. Threat detection**
* **C. Data protection**
* D. Cost optimization
* E. Loosely coupled microservices

**Correct Answers:** **C. Data protection** & **B. Threat detection**

**Exam Perspective Hint:** 

- B. Threat detection: Regulatory frameworks often require companies to have the ability to detect and respond to threats, ensuring that sensitive data is protected from unauthorized access or misuse. Amazon services like Amazon GuardDuty can help with threat detection, which is an important part of compliance.
- C. Data protection: Compliance with regulatory frameworks typically involves ensuring that data is securely stored and processed. Amazon SageMaker provides built-in data protection features such as encryption, and it is essential to comply with privacy regulations like GDPR, HIPAA, etc. This ensures that sensitive data is properly handled.

## Question 51
**Scenario:** A company needs to choose a model from Amazon Bedrock to use internally. The company must identify a model that generates responses in a style that the company's employees prefer. What should the company do to meet these requirements?

- A. Evaluate the models by using built-in prompt datasets.
- B. Evaluate the models by using a human workforce and custom prompt datasets.
- C. Use public model leaderboards to identify the model.
- D. Use the model InvocationLatency runtime metrics in Amazon CloudWatch when trying models.

* **Correct Answer:** **B**
* **Why:** Evaluating response style preference (human preference) specifically requires human feedback (reinforcement learning from human feedback or human evaluation) using custom prompts representative of the company’s internal style requirements. Amazon Bedrock supports Model Evaluation using human evaluation workforces (internal or AWS-managed).
* **Hint:** When a requirement specifies matching subjective qualities like company-specific tone, style, or employee preference, human evaluation with custom prompt datasets is required.



## Question 52
**Scenario:** A student at a university is copying content from generative AI to write essays. Which challenge of responsible generative AI does this scenario represent?

- A. Toxicity
- B. Hallucinations
- C. Plagiarism
- D. Privacy

* **Correct Answer:** **C**
* **Why:** Submitting AI-generated content as one's own work without attribution or copying existing text generated by a model constitutes plagiarism and academic dishonesty.
* **Hint:** Look at the action being performed: copying content and presenting it as original student work directly maps to plagiarism.



## Question 53
**Scenario:** A company needs to build its own large language model (LLM) based on only the company's private data. The company is concerned about the environmental effect of the training process. Which Amazon EC2 instance type has the LEAST environmental effect when training LLMs?

- A. Amazon EC2 C series
- B. Amazon EC2 G series
- C. Amazon EC2 P series
- D. Amazon EC2 Trn series

* **Correct Answer:** **D**
* **Why:** Amazon EC2 **Trn1** (Trainium) instances are custom-built by AWS specifically for deep learning training. They offer high performance while delivering up to 50% cost-to-train savings and superior energy efficiency compared to equivalent GPU-based instances (such as P or G series), reducing carbon footprint and environmental impact.
* **Hint:** Remember AWS silicon optimization: **Trn** = **Training** (Trainium, high energy efficiency/sustainability for LLM training), **Inf** = **Inference** (Inferentia).



## Question 54
**Scenario:** A company wants to build an interactive application for children that generates new stories based on classic stories. The company wants to use Amazon Bedrock and needs to ensure that the results and topics are appropriate for children. Which AWS service or feature will meet these requirements?

- A. Amazon Rekognition
- B. Amazon Bedrock playgrounds
- C. Guardrails for Amazon Bedrock
- D. Agents for Amazon Bedrock

* **Correct Answer:** **C**
* **Why:** **Guardrails for Amazon Bedrock** allows you to implement customizable safety, privacy, and content moderation boundaries for your generative AI applications (e.g., filtering out unsafe topics, hate speech, profanity, or harmful content suitable for sensitive audiences like children).
* **Hint:** Anytime you see requirements around filtering out inappropriate topics, enforcing safety policies, or preventing sensitive content output in Bedrock, choose **Guardrails**.



## Question 55
**Scenario:** A company is building an application that needs to generate synthetic data that is based on existing data. Which type of model can the company use to meet this requirement?

- A. Generative adversarial network (GAN)
- B. XGBoost
- C. Residual neural network
- D. WaveNet

* **Correct Answer:** **A**
* **Why:** **Generative Adversarial Networks (GANs)** consist of two neural networks (a generator and a discriminator) competing against each other to create realistic synthetic data (images, tabular data, text) that mirrors the distribution of real training data.
* **Hint:** XGBoost is for tabular classification/regression, ResNet is for computer vision image classification, and GANs are specifically designed to *generate* synthetic realistic data samples.



## Question 56
**Scenario:** A digital devices company wants to predict customer demand for memory hardware. The company does not have coding experience or knowledge of ML algorithms and needs to develop a data-driven predictive model. The company needs to perform analysis on internal data and external data. Which solution will meet these requirements?

- A. Store the data in Amazon S3. Create ML models and demand forecast predictions by using Amazon SageMaker built-in algorithms that use the data from Amazon S3.
- B. Import the data into Amazon SageMaker Data Wrangler. Create ML models and demand forecast predictions by using SageMaker built-in algorithms.
- C. Import the data into Amazon SageMaker Data Wrangler. Build ML models and demand forecast predictions by using an Amazon Personalize Trending-Now recipe.
- D. Import the data into Amazon SageMaker Canvas. Build ML models and demand forecast predictions by selecting the values in the data from SageMaker Canvas.

* **Correct Answer:** **D**
* **Why:** **Amazon SageMaker Canvas** is a visual, no-code interface that enables business analysts and teams with no coding or ML experience to generate accurate ML predictions and demand forecasting models.
* **Hint:** Keyword pairing: "No coding experience" + "predictive model/forecasting" $\rightarrow$ **Amazon SageMaker Canvas**.



## Question 57
**Scenario:** A company has installed a security camera. The company uses an ML model to evaluate the security camera footage for potential thefts. The company has discovered that the model disproportionately flags people who are members of a specific ethnic group. Which type of bias is affecting the model output?

- A. Measurement bias
- B. Sampling bias
- C. Observer bias
- D. Confirmation bias

* **Correct Answer:** **B**
* **Why:** **Sampling bias** occurs when the data collected to train the model is not representative of the real-world environment or true population distribution (e.g., underrepresenting or overrepresenting certain groups in training footage), leading the model to perform unequally across demographic groups.
* **Hint:** When an algorithm disproportionately targets or misclassifies a demographic group due to unrepresentative training data, it is primarily a **sampling bias** issue.



## Question 58
**Scenario:** A company is building a customer service chatbot. The company wants the chatbot to improve its responses by learning from past interactions and online resources. Which AI learning strategy provides this self-improvement capability?

- A. Supervised learning with a manually curated dataset of good responses and bad responses
- B. Reinforcement learning with rewards for positive customer feedback
- C. Unsupervised learning to find clusters of similar customer inquiries
- D. Supervised learning with a continuously updated FAQ database

* **Correct Answer:** **B**
* **Why:** **Reinforcement Learning (RL)** uses a reward-and-penalty mechanism. By rewarding the model when it receives positive feedback from customer interactions, the chatbot dynamically learns to improve and optimize its response strategy over time.
* **Hint:** "Self-improvement," "learning from interactions," and "rewards/feedback" are classic hallmarks of **Reinforcement Learning** (e.g., RLHF).



## Question 59
**Scenario:** An AI practitioner has built a deep learning model to classify the types of materials in images. The AI practitioner now wants to measure the model performance. Which metric will help the AI practitioner evaluate the performance of the model?

- A. Confusion matrix
- B. Correlation matrix
- C. R2 score
- D. Mean squared error (MSE)

* **Correct Answer:** **A**
* **Why:** A **confusion matrix** is a fundamental evaluation tool for classification models (such as image classification). It summarizes prediction results by showing true positives, false positives, true negatives, and false negatives across classes.
* **Hint:** $R^2$ score and MSE (Mean Squared Error) are used for *regression* tasks, whereas a **Confusion Matrix** is used for *classification* tasks.



## Question 60
**Scenario:** A company has built a chatbot that can respond to natural language questions with images. The company wants to ensure that the chatbot does not return inappropriate or unwanted images. Which solution will meet these requirements?

- A. Implement moderation APIs.
- B. Retrain the model with a general public dataset.
- C. Perform model validation.
- D. Automate user feedback integration.

* **Correct Answer:** **A**
* **Why:** **Moderation APIs** (such as Amazon Rekognition Image Moderation) automatically analyze images before displaying them to users to detect and filter out inappropriate, explicit, or unwanted visual content in real time.
* **Hint:** To prevent returning unsafe or unwanted visual content directly to users, implementing an automated **moderation API** is the standard architectural control.

# AWS Certified AI Practitioner (AIF-C01) - Exam Questions

## Question #61
An AI practitioner is using an Amazon Bedrock base model to summarize session chats from the customer service department. The AI practitioner wants to store invocation logs to monitor model input and output data. Which strategy should the AI practitioner use?

- **A.** Configure AWS CloudTrail as the logs destination for the model.
- **B.** Enable invocation logging in Amazon Bedrock.
- **C.** Configure AWS Audit Manager as the logs destination for the model.
- **D.** Configure model invocation logging in Amazon EventBridge.

* **Correct Answer:** **B**


## Question #62
A company is building an ML model to analyze archived data. The company must perform inference on large datasets that are multiple GBs in size. The company does not need to access the model predictions immediately. Which Amazon SageMaker inference option will meet these requirements?

- **A.** Batch transform
- **B.** Real-time inference
- **C.** Serverless inference
- **D.** Asynchronous inference

* **Correct Answer:** **A**


## Question #63
Which term describes the numerical representations of real-world objects and concepts that AI and natural language processing (NLP) models use to improve understanding of textual information?

- **A.** Embeddings
- **B.** Tokens
- **C.** Models
- **D.** Binaries

* **Correct Answer:** **A**


## Question #64
A research company implemented a chatbot by using a foundation model (FM) from Amazon Bedrock. The chatbot searches for answers to questions from a large database of research papers. After multiple prompt engineering attempts, the company notices that the FM is performing poorly because of the complex scientific terms in the research papers. How can the company improve the performance of the chatbot?

- **A.** Use few-shot prompting to define how the FM can answer the questions.
- **B.** Use domain adaptation fine-tuning to adapt the FM to complex scientific terms.
- **C.** Change the FM inference parameters.
- **D.** Clean the research paper data to remove complex scientific terms.

* **Correct Answer:** **B**


## Question #65
A company wants to use a large language model (LLM) on Amazon Bedrock for sentiment analysis. The company needs the LLM to produce more consistent responses to the same input prompt. Which adjustment to an inference parameter should the company make to meet these requirements?

- **A.** Decrease the temperature value.
- **B.** Increase the temperature value.
- **C.** Decrease the length of output tokens.
- **D.** Increase the maximum generation length.

* **Correct Answer:** **A**


**Hints**

* **Temperature** controls the randomness and creativity of the model's responses.
* **Lowering the temperature** (closer to `0`) makes the model's output more deterministic, consistent, and predictable because it continuously selects the most probable tokens. This is ideal for tasks like sentiment analysis, where consistent and repeatable classification is required.
* **Increasing the temperature** increases randomness and variability, leading to more creative or varied responses to the same prompt.

### Why the Other Options are Incorrect:

* **B. Increase the temperature value:** This would make the output more random and creative, leading to less consistent answers.



## Question #66
A company wants to develop a large language model (LLM) application by using Amazon Bedrock and customer data that is uploaded to Amazon S3. The company's security policy states that each team can access data for only the team's own customers. Which solution will meet these requirements?

- **A.** Create an Amazon Bedrock custom service role for each team that has access to only the team's customer data.
- **B.** Create a custom service role that has Amazon S3 access. Ask teams to specify the customer name on each Amazon Bedrock request.
- **C.** Redact personal data in Amazon S3. Update the S3 bucket policy to allow team access to customer data.
- **D.** Create one Amazon Bedrock role that has full Amazon S3 access. Create IAM roles for each team that have access to only each team's customer folders.

* **Correct Answer:** **A**


## Question #67
A medical company deployed a disease detection model on Amazon Bedrock. To comply with privacy policies, the company wants to prevent the model from including personal patient information in its responses. The company also wants to receive notification when policy violations occur. Which solution meets these requirements?

- **A.** Use Amazon Macie to scan the model's output for sensitive data and set up alerts for potential violations.
- **B.** Configure AWS CloudTrail to monitor the model's responses and create alerts for any detected personal information.
- **C.** Use Guardrails for Amazon Bedrock to filter content. Set up Amazon CloudWatch alarms for notification of policy violations.
- **D.** Implement Amazon SageMaker Model Monitor to detect data drift and receive alerts when model quality degrades.

* **Correct Answer:** **C**


## Question #68
A company manually reviews all submitted resumes in PDF format. As the company grows, the company expects the volume of resumes to exceed the company's review capacity. The company needs an automated system to convert the PDF resumes into plain text format for additional processing. Which AWS service meets this requirement?

- **A.** Amazon Textract
- **B.** Amazon Personalize
- **C.** Amazon Lex
- **D.** Amazon Transcribe

* **Correct Answer:** **A**

## Question #69
An education provider is building a question and answer application that uses a generative AI model to explain complex concepts. The education provider wants to automatically change the style of the model response depending on who is asking the question. The education provider will give the model the age range of the user who has asked the question. Which solution meets these requirements with the LEAST implementation effort?

- **A.** Fine-tune the model by using additional training data that is representative of the various age ranges that the application will support.
- **B.** Add a role description to the prompt context that instructs the model of the age range that the response should target.
- **C.** Use chain-of-thought reasoning to deduce the correct style and complexity for a response suitable for that user.
- **D.** Summarize the response text depending on the age of the user so that younger users receive shorter responses.

* **Correct Answer:** **B**


## Question #70
Which strategy evaluates the accuracy of a foundation model (FM) that is used in image classification tasks?

- **A.** Calculate the total cost of resources used by the model.
- **B.** Measure the model's accuracy against a predefined benchmark dataset.
- **C.** Count the number of layers in the neural network.
- **D.** Assess the color accuracy of images processed by the model.

* **Correct Answer:** **B**

# AWS Certified AI Practitioner (AIF-C01) Exam Questions (Page 8)

### Question #71
An accounting firm wants to implement a large language model (LLM) to automate document processing. The firm must proceed responsibly to avoid potential harms. What should the firm do when developing and deploying the LLM? (Choose two.)
- A. Include fairness metrics for model evaluation.
- B. Adjust the temperature parameter of the model.
- C. Modify the training data to mitigate bias.
- D. Avoid overfitting on the training data.
- E. Apply prompt engineering techniques.


* **Correct Answer:** **A and C**



### Question #72
A company is building an ML model. The company collected new data and analyzed the data by creating a correlation matrix, calculating statistics, and visualizing the data. Which stage of the ML pipeline is the company currently in?
- A. Data pre-processing
- B. Feature engineering
- C. Exploratory data analysis
- D. Hyperparameter tuning

* **Correct Answer: C**

Why Option C (Exploratory Data Analysis) is Correct

- Exploratory Data Analysis (EDA) is the stage where you analyze datasets to summarize their main characteristics, often using statistical graphics and data visualization methods. Key tasks in EDA include:

  - Calculating summary statistics (mean, median, standard deviation).

  - Creating correlation matrices to identify relationships between variables.

  - Plotting histograms, scatter plots, and box plots to understand data distribution and spot outliers.

| Option | Stage | Primary Goal / Key Tasks |
| --- | --- | --- |
| A. Data pre-processing | Data Preparation | Cleaning noisy data, handling missing values, deduplication, and normalization/scaling. |
| B. Feature engineering | Data Transformation | Creating new features from raw data (e.g., One-Hot Encoding, PCA, binning, extracting text tokens) to improve model accuracy. |
| D. Hyperparameter tuning | Model Optimization | Adjusting algorithm configuration settings (learning rate, batch size, epoch count) during or between training runs using tools like Amazon SageMaker Automatic Model Tuning. |


### Question #73
A company has documents that are missing some words because of a database error. The company wants to build an ML model that can suggest potential words to fill in the missing text. Which type of model meets this requirement?
- A. Topic modeling
- B. Clustering models
- C. Prescriptive ML models
- D. BERT-based models

* **Correct Answer: D**

**Correct Answer: D. BERT-based models**

### Detailed Explanation

* **BERT (Bidirectional Encoder Representations from Transformers)** uses a training technique called **Masked Language Modeling (MLM)**. In MLM, words in a sentence are randomly masked (hidden), and the model learns to predict those missing words based on the context of the words both to the left and to the right (bidirectional). This makes BERT natively suited for filling in missing text or completing incomplete sentences.

### Why the Other Options Are Incorrect

* **A. Topic modeling:** Used for unlabelled text classification and discovering hidden themes across large document collections (e.g., using LDA or Amazon Comprehend to group customer feedback into topics like "Billing", "Shipping", or "Product Quality"). It cannot predict specific missing words.
* **B. Clustering models:** Unsupervised learning algorithms (like K-Means) designed to group similar data points together based on feature similarity. They are not language models and cannot generate or suggest text.
* **C. Prescriptive ML models:** Analytics/ML models focused on recommending specific actions to achieve a target outcome (e.g., "reduce price by 5% to maximize profit"). They do not operate on natural language masked sequence completion.

### Mentor Tip for AWS AI Practitioner Exam

When you see **"fill in missing words"**, **"masked language"**, or **"bidirectional context understanding"** in an exam question, instantly map it to **BERT / Transformer Encoders**. If the scenario instead asks to **"generate new text from scratch"** or **"continue writing a story"**, map it to **Autoregressive / Decoder models (like GPT)**.


### 1. Transformer Types & Architectures

#### **BERT (Encoder-Only)**

* **Exam Trigger Words:** *Bidirectional context, fill in missing words, masked language modeling (MLM), search relevance, sentiment classification, entity recognition.*
* **Exam Hint:** If the scenario mentions evaluating text from **both directions simultaneously** or finding **missing/hidden tokens**, pick BERT/Encoder models.

#### **Decoder-Only Models (GPT, Llama, Claude)**

* **Exam Trigger Words:** *Autoregressive, next-token prediction, text generation, story completion, chatbot, code generation, creative writing.*
* **Exam Hint:** Choose this when the goal is to **generate new text from left to right** or extend an existing prompt.

#### **Encoder-Decoder Models (T5, BART)**

* **Exam Trigger Words:** *Sequence-to-Sequence (Seq2Seq), machine translation, text summarization, rephrasing, conditional generation.*
* **Exam Hint:** Choose this when the input text format/length is transformed into a **completely different output sequence** (e.g., English to French or a 10-page report to a 1-paragraph summary).

### 2. Traditional Machine Learning & Deep Learning Models

#### **SVM (Support Vector Machine)**

* **Exam Trigger Words:** *Decision boundary, hyperplane, maximum margin, high-dimensional space, linear/binary classification, structured/tabular data.*
* **Exam Hint:** Think of "drawing a line to separate two distinct groups." It is a classic supervised algorithm for tabular binary classification.

#### **RNN (Recurrent Neural Network)**

* **Exam Trigger Words:** *Sequential data, time-series forecasting, historical dependency, internal memory, vanishing gradient problem.*
* **Exam Hint:** Standard RNNs process data **step-by-step in order**. If a question mentions historical sequences or time series (without requiring massive transformer scale), think RNN/LSTM.

#### **CNN (Convolutional Neural Network)**

* **Exam Trigger Words:** *Computer vision, image classification, spatial features, object detection, pixel grid analysis, sliding filters/convolutions.*
* **Exam Hint:** Any classical deep learning question involving **images, medical scans, camera feeds, or visual quality inspection** points directly to CNNs.

#### **WaveNet**

* **Exam Trigger Words:** *Raw audio generation, speech synthesis, text-to-speech (TTS), natural human voice generation.*
* **Exam Hint:** If the question explicitly mentions generating **high-fidelity audio waveforms** directly from text inputs, think WaveNet or Amazon Polly.

#### **GAN (Generative Adversarial Network)**

* **Exam Trigger Words:** *Generator vs. Discriminator, synthetic image generation, competing neural networks, deepfakes, realistic synthetic data.*
* **Exam Hint:** Look for the two opposing roles: one network *creates fake data* and the other *detects if it is fake*.

#### **XGBoost (Extreme Gradient Boosting)**

* **Exam Trigger Words:** *Gradient boosted decision trees, tabular/structured data, classification and regression, ensemble learning, Amazon SageMaker built-in algorithm.*
* **Exam Hint:** If the scenario involves predicting tabular values (like customer churn, credit score, house prices, or fraud) and asks for high accuracy on structured data, **XGBoost** is almost always the answer.

### Quick Recall Matrix for AIF-C01

| Term | Target Data Type | Primary Function | One-Line Exam Rule |
| --- | --- | --- | --- |
| **BERT** | Text | Context / Masked Text | Reads left + right simultaneously. |
| **Decoder-Only** | Text | Text Generation | Generates text next token at a time. |
| **Encoder-Decoder** | Text | Translation / Summary | Transforms Input Sequence $\rightarrow$ Output Sequence. |
| **SVM** | Tabular Data | Classification | Finds the optimal separating boundary line. |
| **RNN** | Time Series / Text | Sequential Processing | Remembers previous sequence steps. |
| **CNN** | Images / Video | Vision & Feature Extraction | Extracts visual patterns using filters. |
| **WaveNet** | Audio | Text-to-Speech | Creates realistic raw audio waveforms. |
| **GAN** | Images / Synthetic | Media Generation | Generator fights Discriminator to produce realistic media. |
| **XGBoost** | Structured Tables | Prediction / Ranking | Trees learning iteratively from previous tree mistakes. |



### Question #74
A company wants to display the total sales for its top-selling products across various retail locations in the past 12 months. Which AWS solution should the company use to automate the generation of graphs?
- A. Amazon Q in Amazon EC2
- B. Amazon Q Developer
- C. Amazon Q in Amazon QuickSight
- D. Amazon Q in AWS Chatbot

* **Correct Answer: C**

### Question #75
A company is building a chatbot to improve user experience. The company is using a large language model (LLM) from Amazon Bedrock for intent detection. The company wants to use few-shot learning to improve intent detection accuracy. Which additional data does the company need to meet these requirements?
- A. Pairs of chatbot responses and correct user intents
- B. Pairs of user messages and correct chatbot responses
- C. Pairs of user messages and correct user intents
- D. Pairs of user intents and correct chatbot responses

* **Correct Answer: C**

### Question #76
A company is using few-shot prompting on a base model that is hosted on Amazon Bedrock. The model currently uses 10 examples in the prompt. The model is invoked once daily and is performing well. The company wants to lower the monthly cost. Which solution will meet these requirements?
- A. Customize the model by using fine-tuning.
- B. Decrease the number of tokens in the prompt.
- C. Increase the number of tokens in the prompt.
- D. Use Provisioned Throughput.

* **Correct Answer: B**

### Question #77
An AI practitioner is using a large language model (LLM) to create content for marketing campaigns. The generated content sounds plausible and factual but is incorrect. Which problem is the LLM having?
- A. Data leakage
- B. Hallucination
- C. Overfitting
- D. Underfitting

* **Correct Answer: B**

### Question #78
An AI practitioner trained a custom model on Amazon Bedrock by using a training dataset that contains confidential data. The AI practitioner wants to ensure that the custom model does not generate inference responses based on confidential data. How should the AI practitioner prevent responses based on confidential data?

- A. Delete the custom model. Remove the confidential data from the training dataset. Retrain the custom model.
- B. Mask the confidential data in the inference responses by using dynamic data masking.
- C. Encrypt the confidential data in the inference responses by using Amazon SageMaker.
- D. Encrypt the confidential data in the custom model by using AWS Key Management Service (AWS KMS).

* **Correct Answer: A**

* **Bcz Once model has been trained, You can't mask, hide confidencial data. Bcz Model will give output using its Trained Dataset which has confidencial data. So you will have to delete model**.



### Question #79
A company has built a solution by using generative AI. The solution uses large language models (LLMs) to translate training manuals from English into other languages. The company wants to evaluate the accuracy of the solution by examining the text generated for the manuals. Which model evaluation strategy meets these requirements?

- A. Bilingual Evaluation Understudy (BLEU)
- B. Root mean squared error (RMSE)
- C. Recall-Oriented Understudy for Gisting Evaluation (ROUGE)
- D. F1 score

* **Correct Answer: A**

* **BLEU (Bilingual Evaluation Understudy):**

  * **Primary Exam Keyword: Machine Translation Quality, N-Gram Precision.**

  * **What it measures: Compares generated machine translation against reference human translations.**

* **ROUGE (Recall-Oriented Understudy for Gisting Evaluation):**

  * **Primary Exam Keyword: Document Summarization, Recall.**
  * **What it measures: How much of the reference text was captured by the generated text.**

* **LLM-as-a-Judge / Human Evaluation:**

  * **Primary Exam Keyword: Semantic Accuracy, Contextual Understanding, Faithfulness.**
  * **What it measures: Evaluates whether the translated text preserves the exact meaning and tone requested in the prompt.**

### Question #80
A large retailer receives thousands of customer support inquiries about products every day. The customer support inquiries need to be processed and responded to quickly. The company wants to implement Agents for Amazon Bedrock. What are the key benefits of using Amazon Bedrock agents that could help this retailer?

- A. Generation of custom foundation models (FMs) to predict customer needs
- B. Automation of repetitive tasks and orchestration of complex workflows
- C. Automatically calling multiple foundation models (FMs) and consolidating the results
- D. Selecting the foundation model (FM) based on predefined criteria and metrics

* **Correct Answer: B**

### Question #81
Which option is a benefit of ongoing pre-training when fine-tuning a foundation model (FM)?

- A. Helps decrease the model's complexity
- B. Improves model performance over time
- C. Decreases the training time requirement
- D. Optimizes model inference time

* **Correct Answer: B**

### Question #82
What are tokens in the context of generative AI models?
- A. Tokens are the basic units of input and output that a generative AI model operates on, representing words, subwords, or other linguistic units.
- B. Tokens are the mathematical representations of words or concepts used in generative AI models.
- C. Tokens are the pre-trained weights of a generative AI model that are fine-tuned for specific tasks.
- D. Tokens are the specific prompts or instructions given to a generative AI model to generate output.

* **Correct Answer: A**

### Question #83
A company wants to assess the costs that are associated with using a large language model (LLM) to generate inferences. The company wants to use Amazon Bedrock to build generative AI applications. Which factor will drive the inference costs?

- A. Number of tokens consumed
- B. Temperature value
- C. Amount of data used to train the LLM
- D. Total training time

* **Correct Answer: A**



### Question #84
A company is using Amazon SageMaker Studio notebooks to build and train ML models. The company stores the data in an Amazon S3 bucket. The company needs to manage the flow of data from Amazon S3 to SageMaker Studio notebooks. Which solution will meet this requirement?

- A. Use Amazon Inspector to monitor SageMaker Studio.
- B. Use Amazon Macie to monitor SageMaker Studio.
- C. Configure SageMaker to use a VPC with an S3 endpoint.
- D. Configure SageMaker to use S3 Glacier Deep Archive.

* **Correct Answer: C**

### Question #85
A company has a foundation model (FM) that was customized by using Amazon Bedrock to answer customer queries about products. The company wants to validate the model's responses to new types of queries. The company needs to upload a new dataset that Amazon Bedrock can use for validation. Which AWS service meets these requirements?

- A. Amazon S3
- B. Amazon Elastic Block Store (Amazon EBS)
- C. Amazon Elastic File System (Amazon EFS)
- D. AWS Snowcone

* **Correct Answer: A**

### Question #86
Which prompting attack directly exposes the configured behavior of a large language model (LLM)?

- A. Prompted persona switches
- B. Exploiting friendliness and trust
- C. Ignoring the prompt template
- D. Extracting the prompt template

* **Correct Answer: D Prompt Injections**

### Question #87
A company wants to use Amazon Bedrock. The company needs to review which security aspects the company is responsible for when using Amazon Bedrock. Which security aspect will the company be responsible for?

- A. Patching and updating the versions of Amazon Bedrock
- B. Protecting the infrastructure that hosts Amazon Bedrock
- C. Securing the company's data in transit and at rest
- D. Provisioning Amazon Bedrock within the company network



### Question #88
A social media company wants to use a large language model (LLM) to summarize messages. The company has chosen a few LLMs that are available on Amazon SageMaker JumpStart. The company wants to compare the generated output toxicity of these models. Which strategy gives the company the ability to evaluate the LLMs with the LEAST operational overhead?

- A. Crowd-sourced evaluation
- B. Automatic model evaluation
- C. Model evaluation with human workers
- D. Reinforcement learning from human feedback (RLHF)

* **Correct Answer: B**

### Question #89
A company is testing the security of a foundation model (FM). During testing, the company wants to get around the safety features and make harmful content. Which security technique is this an example of?

- A. Fuzzing training data to find vulnerabilities
- B. Denial of service (DoS)
- C. Penetration testing with authorization
- D. Jailbreak

* **Correct Answer: D**

- Jailbreaking is a technique used to bypass the safety features and restrictions of a foundation model (FM). The goal is to manipulate the model into generating harmful, inappropriate, or otherwise unintended content, despite the safeguards in place. This is often done to test the robustness of the model's safety mechanisms.


### Question #90
A company needs to use Amazon SageMaker for model training and inference. The company must comply with regulatory requirements to run SageMaker jobs in an isolated environment without internet access. Which solution will meet these requirements?

- A. Run SageMaker training and inference by using SageMaker Experiments.
- B. Run SageMaker training and inference by using network isolation.
- C. Encrypt the data at rest by using encryption for SageMaker geospatial capabilities.
- D. Associate appropriate AWS Identity and Access Management (IAM) roles with the SageMaker jobs.

* **Correct Answer: B**

* **VPC configuration with private subnets (no internet gateway)**

* **Enabling Network Isolation / Internet-free mode on the model training job**

* **VPC Endpoints (AWS PrivateLink) for accessing S3 and internal AWS services**.

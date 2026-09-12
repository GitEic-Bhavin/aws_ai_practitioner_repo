# Amazon SageMaker - Overview

## What is Amazon SageMaker?

**Amazon SageMaker** is one of the most important machine learning services on AWS.

It is a **fully managed service** designed for:

- Developers
- Data scientists

They can use SageMaker to:

- Build machine learning models
- Train machine learning models
- Tune machine learning models
- Deploy machine learning models
- Monitor the performance of predictions and models

### Why is SageMaker useful?

Normally, doing all the machine learning processes in one place can be difficult.

When you start training a machine learning model, you need **compute resources or servers**, and **provisioning** them can also be difficult.

- **Provisioning** means setting up and making the required compute resources, such as servers, available for use.

SageMaker handles these things for you **in one place**.

---

## Example: Predicting an AWS Exam Score

Suppose you want to build a model to predict your next AWS exam score.

First, you need **historical data**. You can collect this data through a survey by asking students:

- Number of years of experience in IT
- Number of years of experience with AWS
- How long they have spent on the course
- Their exam score

The **exam score is the output** that we want the model to predict.

For example, students may provide exam scores such as:

- 670
- 890
- 934

After collecting as many rows of historical data as possible, you can build a machine learning model directly on SageMaker.

SageMaker helps you:

- Train the model
- Tune the model

Once the model is built, a new student who has not passed the exam yet can provide:

- 3 years of experience in IT
- 1 year of experience with AWS
- 10 hours spent on the course

The model applies what it learned from the historical data and may predict:

> The student will pass the exam with a score of **906**.

So, all of these activities can happen directly on SageMaker.

---

## SageMaker - End-to-End ML Service

SageMaker can support the machine learning process from data collection to model monitoring.

The overall process is:

1. **Collect and prepare data**
2. **Build and train machine learning models**
3. **Deploy the models**
4. **Monitor the performance of predictions and models**
5. Go back to the first stage and improve the data collection based on what is learned from the model's performance

This makes SageMaker a **one-stop place for machine learning**.

---

## Built-in Algorithms

SageMaker has many **built-in algorithms** for different machine learning tasks.

### 1. Supervised Algorithms

SageMaker supports supervised learning algorithms such as:

- **Linear Regression** → used for regression problems.
- **Classification** → used to classify data into different categories.
- **KNN (K-Nearest Neighbors)** → can be used for classification.

### 2. Unsupervised Algorithms

SageMaker also supports unsupervised learning algorithms such as:

- **PCA (Principal Component Analysis)**
  - Used to **reduce the number of features** in a dataset.
  - In simple words, PCA reduces the number of variables/features while keeping important information.

- **K-means**
  - Used to find **groups in data**.
  - These groups are called **clusters**.

- **Anomaly Detection**
  - Used to find datasets or data points that look different from the normal data.
  - For example, it can be used for **fraud detection**.

### 3. Textual Algorithms

SageMaker can also be used for machine learning on text.

Examples include:

- **NLP (Natural Language Processing)**
- Text summarization

**NLP** means working with human language using machine learning.

### Image Processing

SageMaker also supports image processing, such as:

- Image classification
- Image detection

These examples show that SageMaker provides many built-in algorithms and can act as a **one-stop place for machine learning**.

---

## Automatic Model Tuning (AMT)

**Automatic Model Tuning (AMT)** is a SageMaker feature that automatically tries different parameter combinations to improve model performance.

Suppose you already have a model, but you want to find a better configuration for it.

You could manually try different parameter combinations, but SageMaker can do this automatically using AMT.

First, you define the **objective metric**:

- The objective metric tells SageMaker **what you want to optimize**.

AMT can then automatically handle:

- **Hyperparameter ranges** → the possible ranges of values that SageMaker can try for the model's hyperparameters.
- **Research strategy** → how SageMaker should navigate through the hyperparameter ranges.
- **Tuning duration** → how long the tuning job should run.
- **Early stop condition** → when to stop a tuning job that is not performing well.

The process is:

1. Define the **objective metric**.
2. SageMaker automatically chooses the **hyperparameter ranges**.
3. SageMaker determines the **research strategy**.
4. SageMaker determines how long the tuning job should run.
5. SageMaker can stop a poorly performing tuning job using the **early stop condition**.

So, you simply say:

> We want to optimize for **this objective metric**.

SageMaker does the rest.

### Benefits of AMT

- Saves time
- Saves money
- Reduces manual tuning work
- Helps find better model configurations
- Avoids wasting money on **suboptimal configurations** by stopping poorly performing jobs early

---

## SageMaker  - Model Deployment & Inference

Once the model has been trained, it needs to be **deployed**.

With SageMaker, deployment is very easy and can be done with **one click**.

SageMaker also provides:

- **Automatic scaling**
- No need to manage servers

This is different from deploying your own model on your own servers.

This type of solution is called a **self-hosted solution**.

Here, **Auto-scaling** means automatically increasing or decreasing the compute resources according to the workload or traffic.

- **Self-hosted solution** → you deploy and manage the model on your own servers.
- **Managed solution** → the service handles much of the underlying infrastructure and management for you.

Because SageMaker is a managed solution, it provides **reduced overhead**.

---

# SageMaker Inference Types

SageMaker provides four main ways to deploy and run a model:

- **1. Real-time inference**
- **2. Serverless inference**
- **3. Asynchronous inference**
- **4. Batch transform**

The right choice depends on things such as:

- Latency requirements
- Payload size
- Number of predictions
- Processing time
- Infrastructure management

**Inference** means using a trained machine learning model to calculate an outcome or prediction for new input data.

---

## 1. Real-Time Inference

**Real-time inference** is used when you need **one prediction at a time** and want the answer immediately.

The application sends a **payload** to a real-time endpoint.

- **Payload** → The input data sent to the model for making a prediction.

- We configure resources such as **CPU or GPU** for the model to perform inference.
- **Inference** → Using a trained machine learning model to make a prediction for new input data.
- And we will have **Auto-scaling** → Automatically increasing or decreasing compute resources based on workload or traffic.

The answer is returned right away.

```text
Application
    ↓ - payload
Real-Time Endpoint
    ↓
ML Model
    ↓
Prediction
```

### Key Points

- **Latency:** Low (milliseconds to seconds)
- **Prediction:** One prediction at a time
- **Payload:** Small
- **Payload size:** Up to **25 MB** (one record)
- **Records:** One record
- **Maximum processing time:** **60 seconds**
- **Auto-scaling:** Available
- **Response:** Immediate

**Use case:** Real-time inference of small predictions. Fast, near-instant predictions for web/mobile apps

---

## 2. Serverless Inference

**Serverless inference** is similar to real-time inference architecture because the response is also given right away.

The main difference is that serverless inference requires **less configuration**.

RAM Selection
here, we only select how much memory we want for our models depending on the models we have.

 Auto-scaling is done out-of-the-box, we don't configure it.

With serverless inference:

- You select how much **memory** you want for the model. The required memory depends on the model.
- **Auto-scaling** is handled automatically. You don't need to configure auto-scaling yourself.
- We can have periods where you don't have any traffic. **no traffic**.
- You don't need to manage infrastructure during periods when there is no traffic.

### Cold Start

One downside of serverless inference is a **cold start**.

A cold start can happen when there has been no traffic for a long time. When a new request arrives:

1. The model/infrastructure needs to boot up.
2. The first request takes a little longer.
3. This adds extra **latency** to the first request.

### Key Points

- **Latency:** Low (milliseconds to seconds)
- **Prediction:** One prediction at a time
- **Payload:** Small
- **Payload size:** Up to **4 MB** (one record)
- **Records:** One record
- **Maximum processing time:** **60 seconds**
- **Infrastructure:** No infrastructure to manage
- **Auto-scaling:** Handled automatically
- **Cold start:** Possible
- **Response:** Immediate
- **Use Case:** Sporadic, short-term inference without infrastructure, can tolerate cold starts

**No infrastructure to manage → Serverless inference**

So, The real-time endpoint is a bit more configuration and The serverless endpoint is a bit less configuration but potentially more latency once you have a cold start.

---

## Asynchronous Inference

**Asynchronous inference** is useful when you have **very large payloads** and the processing can take longer.

The input payload can be up to **1 GB**.

Because processing can take a long time, you don't get the response immediately.

The payload is placed into a **staging Amazon S3 bucket**.

The process is:

1. The application puts the payload into a staging S3 bucket.
2. The application tells the asynchronous endpoint to put the job in a queue.
3. The model processes the job in its own time.
4. The result is placed into another Amazon S3 bucket.

```text
Application
    ↓ - payload
S3 Staging Bucket
    ↓
Asynchronous Endpoint
    ↓
Job Queue
    ↓
Model Processing
    ↓
S3 Result Bucket
```

The request and response for the payloads are stored in **Amazon S3**.

### Key Points

- **Latency:** **Near-real-time**. Medium to High. (You don't get the answer right away but you'll get it at some point)
- **Prediction:** One big prediction
- **Payload size:** Up to **1 GB** (one record)
- **Maximum processing time:** **1 hour**
- **Request/response:** Stored in Amazon S3
- **Processing:** Uses a job queue
- **Use case:** Large payloads and workloads requiring longer processing times

**Near-real-time → Asynchronous inference**

> Asynchronous inference is for **one large prediction**.

---

## Batch Transform

**Batch transform** is used when you want predictions for an **entire dataset**.

In other words, you want **multiple predictions**.

The application puts the dataset into a staging S3 bucket and tells the batch endpoint to process it.

The process is:

1. Application puts the dataset into a staging S3 bucket.
2. It tells the batch endpoint to put the job in a job queue.
3. Predictions are calculated for the dataset.
4. The results are placed into a result Amazon S3 bucket.

```text
Application
    ↓
S3 Staging Bucket
    ↓
Batch Endpoint
    ↓
Job Queue
    ↓
Process Dataset
    ↓
S3 Result Bucket
```

The request and response are stored in **Amazon S3**.

### Concurrent Processing

Batch transform processes **multiple data points** from a dataset.

Because there are many predictions to make, it can perform **concurrent processing**.

- **Concurrent processing** → Processing multiple data points at the same time.

This is why it is called a **batch**: many records are processed together.

The batch size can be **100 MB per mini-batch**, but you can have many mini-batches.

Therefore, batch transform can have very large overall invocations.

### Key Points

- **Latency:** High (minutes to hours)
- **Predictions:** Multiple
- **Input:** Entire dataset
- **Processing:** Concurrent processing
- **Payload size:** Up to **100 MB per invocation** (per mini-batch)
- **Maximum processing time:** **1 hour**
- **Mini-batches:** Many mini-batches can be used
- **Request/response:** Stored in Amazon S3
- **Processing:** Uses a job queue

**Multiple records / entire dataset → Batch Transform**

---

## SageMaker Studio

- End-to-End ML development from a unified interface
- Team collaboration
- Tune and debug ML models
- Deploy ML models
- Automated workflows

So, SageMaker is used to train the model, automatically tune the model, deploy the model in four different ways.

---
---

# SageMaker - Hands On

## SageMaker vs SageMaker AI

When you search for **SageMaker** in AWS, you may see two options:

- **AmAzon SageMaker**
- **Amazon SageMaker AI**

The SageMaker option is a **higher-level service** and is not the one used in this course for actually building machine learning models.

**SageMaker AI** is the service used to:

- Build machine learning models
- Train machine learning models
- Deploy machine learning models
- Perform these activities **at scale** (means being able to handle larger amounts of data, workloads, users, or machine learning operations)

---

## Setting Up SageMaker AI

Since we are new to SageMaker AI, we need to set it up for a **single user**.

As the setup progresses, it creates:

- A **SageMaker domain**
- A **Studio user profile**

A **SageMaker domain** provides the environment that allows users to access **SageMaker Studio** and its machine learning tools.

A **Studio user profile** represents a user inside the SageMaker domain and provides access to the SageMaker Studio environment.

---

## SageMaker Studio

Once SageMaker Studio is open, it provides a single interface where you can access the different SageMaker capabilities.

The things covered throughout the course are available from this interface.

You can access applications and features such as:

- **RStudio**
You can access **RStudio** as a separate application from SageMaker Studio.

- **Canvas**
Canvas provides a user interface for working with machine learning without necessarily needing to write all the code yourself.

- **MLFlow**
It can be used for managing and tracking machine learning experiments and models.

- **JupyterLab**
JupyterLab provides an interactive environment where you can work with code, notebooks, data, and machine learning workflows.


- **Models**

Within the **Models** section, you can view models that are available to use.

These can include **JumpStart base models**.

For example, you can launch models such as:

- **DeepSeek R1**
- **Meta Llama**

You can:

- View the model details
- Customize the model using a UI
- Customize the model using code
- Start with the available base model

A **base model** is a pre-existing model that you can use as a starting point instead of building a model completely from scratch.

- **Assets**
The **Assets** section allows you to work with machine learning-related resources.

You can access:

- **Datasets**
You can view your datasets and **upload** datasets to SageMaker Studio.

- **Evaluators**
You can manage evaluators from the interface.

- Compute - Instances can be used to run your ml models
here, You can also view which **instances** can be used to run your machine learning models.

An **instance** is a virtual computing resource in AWS that provides resources such as CPU, memory, or GPU for running workloads.

The type of instance you use depends on the requirements of your machine learning workload.

- **Experiments**
You can use the interface to work with and manage your experiments.

- **Jobs**
SageMaker Studio provides a place where you can view different types of jobs.

These include: Inference Optimization , Training, Model evaluation, Performance evaluation

### Inference Optimization

Inference optimization focuses on improving how efficiently a trained machine learning model performs predictions.

### Training

Training jobs are used to train machine learning models using your data.

### Model Evaluation

Model evaluation is used to evaluate how well a machine learning model performs.

### Performance Evaluation

Performance evaluation is used to evaluate the performance of the model and its predictions.

- **Pipelines**
There is a **visual editor** that can be used to maintain your SageMaker Pipelines.

A **pipeline** is a sequence of machine learning steps or processes that can be organized into a workflow.

- **Deployments**
Deployment means making a trained machine learning model available so that it can be used to make predictions.

- **Feature Store**
A Feature Store is used to store and manage **features** used by machine learning models.

A **feature** is an input variable used by a machine learning model to make predictions.

---

## SageMaker Domain and Studio Access

After the setup, we have a **SageMaker domain**.

This domain allows us to access the SageMaker Studio UI.

The domain provides the environment through which we can access the different SageMaker Studio capabilities.

Within SageMaker Studio, you can also select applications such as:

- Canvas
- RStudio
- Other available applications

When you click these options, they can redirect you to the relevant functionality within the SageMaker Studio UI.

---

So, These capabilities are accessible from the **SageMaker AI UI**. SageMaker Studio provides a central place to access many machine learning tools and workflows.

The main idea is:

```text
SageMaker AI
      ↓
SageMaker Domain
      ↓
SageMaker Studio
      ↓
┌──────────────────────────────────────┐
│ RStudio                              │
│ Canvas                               │
│ MLFlow                               │
│ JupyterLab                           │
│ Models                               │
│ Datasets                             │
│ Evaluators                           │
│ Instances                            │
│ Experiments                          │
│ Jobs                                 │
│ Pipelines                            │
│ Feature Store                        │
└──────────────────────────────────────┘
```

SageMaker Studio brings the different machine learning capabilities into **one UI**.

---
---

# Amazon SageMaker - Data Tools

To get started with SageMaker, we first need to **prepare our data**.

For this, we can use **SageMaker Data Wrangler**. Data Wrangler is now fully integrated in "SageMaker Canvas".

## SageMaker - Data Wrangler

Data Wrangler provides a **single interface** where you can work with your data.

**SageMaker Data Wrangler** is a tool used to prepare 

**1. tabular and image data** for machine learning.

- **Tabular data** → Data organized in rows and columns, such as data in a spreadsheet or database table.

**2. Data Preparation, Transformation, Feature engineering :**
- **Data preparation** → Getting data into a suitable form before using it for machine learning.
- **Data transformation** → Changing data into a more useful format.
- **Feature engineering** → Creating or changing features so they can be used effectively by a machine learning model.

**3. Data selection, cleansing, exploration, visualization, processing**

1. You can select the data that you want to work with.

2. You can **cleanse** your data before using it for machine learning.

Data cleansing means finding and dealing with problems in the data, such as:

- Missing data
- Incorrect formats
- Incorrect or unwanted values

3. You can explore your datasets to understand what is inside them.

This helps you understand:

- What type of data you have
- How the data is distributed
- Whether there are problems in the data
- What kind of data you are dealing with

4. Data Wrangler allows you to visualize your data using **graphs**.

Graphs can help you understand what is happening within your datasets.

Understanding your data is important because the type and quality of your data can have a **big impact on the machine learning model you choose**.

5. You can process and transform your data so that it is ready to be used by machine learning models.

So, Data Wrangler is a powerful data tool that helps make sure your data is **ready for machine learning**.


**4. SQL Support**

If you are a programmer who uses the **SQL language**, Data Wrangler also provides **SQL support**. This allows you to work with and manipulate data using SQL.

**5. Data Quality**

Data Wrangler also provides a **data quality tool**.

This helps you analyze the quality of your data.

For example, it can help you check:

- Whether rows & columns are in the correct format
- Whether some data is missing
- Whether there are other data quality problems

The goal is to make sure that the data is in a suitable condition before using it for machine learning.

---

## Importing Data

Data Wrangler allows you to import data from different places.

For example:

- **Amazon S3**

After importing data, you can preview it and configure how the data should be interpreted.

You can:

- Preview the data
- Extract data
- Configure column names
- Configure column types

**Column type** tells the system what kind of data a column contains, such as numerical or text data.

## Visualizing Data

Data Wrangler allows you to create graphs to understand your datasets.

Visualization helps you:

- Understand what is happening within your data
- Understand the type of data you are dealing with
- Identify patterns in the data
- Get a better idea of how the data may affect your machine learning model

This is important because understanding your data has a big impact on **which machine learning model you will choose**.

## Transforming Data

Data Wrangler also allows you to define **data transformations**.

You can define:

- The transformation you want to perform
- The function you want to apply to your data
- Data that you want to drop
- Data that you want to add

A **data transformation** changes the existing data into a form that is more useful for machine learning.

For example, you may:

- Remove unwanted columns
- Add new columns
- Change the format of existing values
- Apply a function to existing data

## Quick Model Analysis

Data Wrangler can also be used to perform a **quick model analysis**.

This gives you an initial idea of whether your machine learning model is likely to **perform well or not**.

It is a quick analysis rather than a complete machine learning model evaluation.

## Exporting the Data Flow

The **data flow** created in Data Wrangler can be exported.

This allows the same data preparation and transformation process to be:

- Recreated in a pipeline
- Automated

A **pipeline** is a sequence of steps that can run as a workflow.

**Automated** means the steps can be performed by the system without manually repeating them each time.

This is useful when the same data preparation process needs to be performed repeatedly.

So, whenever you need to **transform or prepare data for machine learning, Data Wrangler can do**.

```text
Data
  ↓
Data Wrangler
  ↓
Clean + Explore + Transform
  ↓
Feature Engineering
  ↓
Machine Learning Model
```

---

# What Are ML Features?

When you use Data Wrangler or any other tool to prepare data, you will want to create **machine learning features**.

**Features** are the inputs that are given to a machine learning model.

They are used:

- As input during **training**
- As input during **inference**

**Training** is the process of teaching a machine learning model using data.

**Inference** is when a trained model uses new input data to make a prediction.

## Example: Birth Date → Age

Suppose a dataset contains a person's **birth date**.

The birth date may not be useful enough in its original form for the machine learning model.

Through **feature engineering**, we can transform the birth date into **age**.

The **age** is a numerical value that may be more usable for the machine learning model.

This is an example of creating a more useful feature from existing data.

## Other Example: 

For a music dataset, features could include:

- **Song rating**
- **Listening duration**
- **Listener demographics**

These features can then be used as inputs to machine learning models.

**Listener demographics** means information about the characteristics of listeners, such as age group or other audience-related information.


## Importance of High-Quality Features

It is very important for a company to have **high-quality features** across its datasets.

The goal is not to create useful features for only one dataset.

Instead, companies want to create and maintain high-quality features **across their datasets** so that they can be reused.

This brings us to the **SageMaker Feature Store**.

---

# SageMaker - Feature Store

The idea behind Feature Store is that features can exist in **many datasets** and can be created or collected from a **variety of sources**.

The Feature Store provides an overview of the features that exist across a company.

You can also have information such as:  Feature descriptions, Details about the available features

This makes it easier to understand and find features that can be used for machine learning.

With SageMaker Feature Store, you can:

- Get an overview of the features available in your company
- Discover existing features
- Add descriptions and information about features
- **Define** the transformation of data into a feature directly
- Publish features from Data Wrangler into Feature Store
- Make features discoverable within SageMaker Studio

This helps improve:
**Collaboration** → Different people in the company can work with and reuse the same features.
**Discovery** → People can find existing features instead of creating the same feature again.

This makes it easier to reuse data and features across the company.
---

## Data Wrangler vs Feature Store

| Feature | Data Wrangler | Feature Store |
|---|---|---|
| Main purpose | Prepare and transform data | Store and manage machine learning features |
| Data preparation | Yes | Not the main purpose |
| Data transformation | Yes | Can define feature transformations |
| Feature engineering | Yes | Supports feature management |
| Data visualization | Yes | Not the main purpose |
| Data quality | Yes | Not the main purpose |
| Feature discovery | Not the main purpose | Yes |
| Feature reuse | Can publish features | Designed for reusable features |
| Collaboration | Supports data workflows | Helps teams discover and reuse features |

- **Need to prepare or transform data? → Data Wrangler**
- **Need to store, discover, and reuse machine learning features? → Feature Store**

### SageMaker Data Wrangler

- Used to prepare **tabular and image data** for machine learning.
- Supports:
  - Data preparation
  - Data transformation
  - Feature engineering
  - Data selection
  - Data cleansing
  - Data exploration
  - Data visualization
  - Data processing
- Supports **SQL**.
- Provides a **data quality tool**.
- Can import data from sources such as **Amazon S3**.
- Allows you to preview data and configure column names and types.
- Allows you to visualize and transform data.
- Can perform a quick model analysis.
- Data flows can be exported and recreated in automated pipelines.
- Data Wrangler is part of **SageMaker Studio**.

### SageMaker Feature Store

- Used to manage **machine learning features**.
- Features are inputs used by machine learning models during:
  - Training
  - Inference
- Features can come from many datasets and different sources.
- Provides an overview of features available across a company.
- Features can have descriptions and other information.
- Feature transformations can be defined within Feature Store.
- Features can be published directly from Data Wrangler.
- Features are discoverable within SageMaker Studio.
- Helps with **feature reuse, collaboration, and discovery**.

---
---

# Amazon SageMaker - Models and Humans

**SageMaker Clarify** provides tools to evaluate and understand machine learning and foundation models.

It can be used for:

- Evaluating foundation models
- Comparing models
- Model explainability
- Detecting bias

---

## 1. Evaluating Foundation Models

With SageMaker Clarify, we can evaluate how one **foundation model** performs compared with another.

For example:

| Evaluation | Model A | Model B |
|---|---:|---:|
| Brand voice | 25% | 75% |
| Relevance | 64% | 93% |

This gives us insights into how the models perform on different tasks.

Here, A **foundation model** is a pre-trained model that can be adapted or customized for different tasks.

### How the Evaluation Works

We provide specific **tasks** to the models, and SageMaker Clarify evaluates how the models perform on those tasks.

For example, we can evaluate human-related factors such as:

- **Friendliness**
- **Humor**
- Other human preferences or qualities

To evaluate these human factors, we need **human involvement**.

---

### Human Evaluation

For model evaluation, we can use:

- An **AWS-managed team**
- Our **own employees**

This allows humans to evaluate and compare the models from a human perspective.

We can also choose where the evaluation data comes from:

- Use **built-in datasets**
- Bring our **own datasets**
- Provide our **own questions**

SageMaker Clarify also provides:

- Built-in metrics
- Built-in algorithms

All of this is available as part of **SageMaker Studio**.

The important point is that **humans are involved in comparing foundation models on specific tasks**.

---

## 2. Model Explainability

Another important feature of SageMaker Clarify is **model explainability**.

Model explainability helps us understand:

- How a model is working
- Why a model is making a particular prediction
- Which features are influencing the prediction

1. SageMaker Clarify provides tools that explain how ML models make predictions.

2. This helps us understand the characteristics of a model as a whole **before deployment**.

3. It can also be useful for **debugging predictions after the model has been deployed**.

4. Helps increase the trust and understanding of the model.

### Example: Loan Rejection

We can ask:

> Why did the model predict a negative outcome such as loan rejection for a given applicant?

SageMaker Clarify can show the main features or reasons that why the applicant was rejected were - Maturity month, Loan amount, etc

This helps us understand **why the model made the prediction**.

> Why did the model make an incorrect prediction?

If the prediction is incorrect, we can investigate which features caused the model to make that incorrect prediction.

---

## 3. Bias Detection (human)

Another important capability of SageMaker Clarify is **bias detection**.

**Bias** means that the data or model may systematically favor one group over another.

For example, the data may contain very different numbers of people from different groups.

1. we want to understand where there may be **human bias** in: Our datasets, Our machine learning model

2. SageMaker Clarify can help detect this bias and measure it using **statistical metrics**.

3. We can specify the **input features** that we want to examine, and SageMaker Clarify can automatically detect potential bias.

### Example: Class Imbalance

One example of bias is **class imbalance**.

**Class imbalance** means that one group or class is substantially more represented in the dataset than another, disadvantaged group.

For example:

```text
Group A: 90%
Group B: 10%
```

Here, Group A is much more represented than Group B. This difference in representation can indicate a potential bias in the dataset.

Another example could be the spread between:

- Men and women
- Other groups being compared

For example, there may be substantially more women than men in a dataset, or vice versa.

SageMaker Clarify can automatically detect these types of potential biases, which is very useful.

---

## SageMaker Ground Truth

**SageMaker Ground Truth** is used for tasks involving **human feedback and human-labeled data**.

A key concept associated with Ground Truth is **RLHF**.

**RLHF** stands for **Reinforcement Learning from Human Feedback**.

SageMaker Ground Truth can be used for:

- Model review, customization, Model evaluation
- Aligning a model to human preferences
- Reinforcement learning where human feedback is included in the "reward" function

#### Human Feedback for ML

The idea is to include **human feedback in the reward function** for reinforcement learning.

A **reward function** provides feedback to a reinforcement learning system about how good or bad an action or result is.

By adding human feedback, we can help the machine learning system learn what humans prefer.

Human feedback can be used to:

- Create and Evaluate models from a human perspective
- Create data and Annotate data (create labels) from a human perspective

This is useful because automated processes do not always align perfectly with **human preferences**. or we need to fine tune the models with specific human preferences.

#### Example:

Suppose a model has learned to behave in a way that is Joyful, Happy, Funny. That may be appropriate for some applications.

However, suppose we are building an AI system that is supposed to be **very business-oriented**.

In that case, we may need one additional layer of human feedback.

Humans can provide their preference and guide the model toward being More professional, More business-oriented, Better aligned with the intended use

This is where human involvement becomes important.

```text
Existing Model
      ↓
Human Feedback
      ↓
Human Preferences
      ↓
Fine-tuning / Alignment
      ↓
Model Better Matches Human Needs
```

---

SageMaker Ground Truth can also be used to create **labels** for data.

Humans review the data and create the appropriate labels.

A **label** is the correct category, value, or description assigned to a piece of data so that it can be used for machine learning.

For example:
An image can be labeled **dog**, Another image can be labeled **ship**, Another image can be labeled **cat**

These labeled examples can then be used to create or improve machine learning datasets.

---

Who Can Perform the Human Review?

The reviewers used for these tasks can come from different sources:

- **Your own employees**
- **Third-party employees**
- Workers from **Amazon Mechanical Turk**

**Amazon Mechanical Turk** is a service that provides access to a large workforce of people who can perform human tasks, such as data labeling and review.

---

### SageMaker Ground Truth Plus : Label Data

**SageMaker Ground Truth Plus** is a capability within SageMaker Ground Truth to use this workforce to perform **data-labeling tasks**.

The idea is that instead of having your own employees perform all the labeling work, you can use this workforce to perform the tasks.

---

# SageMaker Clarify vs SageMaker Ground Truth

| Feature | SageMaker Clarify | SageMaker Ground Truth |
|---|---|---|
| Main purpose | Evaluate, explain, and detect bias | Human feedback and data labeling |
| Foundation model evaluation | Yes | Yes, for human-based review/evaluation |
| Model explainability | Yes | Not the main purpose |
| Bias detection | Yes | Not the main purpose |
| Human feedback | Used for model evaluation | Central to the service |
| Human preferences | Yes | Yes |
| Data labeling | Not the main purpose | Yes |
| RLHF | Not the main focus | Important concept |
| Human reviewers | AWS-managed team or own employees | Employees, third parties, Mechanical Turk |
| Ground Truth Plus | No | Yes |

---

## Summary

- **Clarify → Understand and evaluate**
  - Compare foundation models
  - Explain model predictions
  - Detect bias

  SageMaker Clarify
  → Compare + Explain + Detect Bias

- **Ground Truth → Humans provide the truth**
  - Human feedback
  - Human preferences
  - Data labeling
  - Model review and evaluation
  - RLHF

  SageMaker Ground Truth
  → Human Feedback + Human Preferences + Data Labeling + RLHF

| keyword | Think |
|---|---|
| Compare foundation models | SageMaker Clarify |
| Evaluate model on specific tasks | SageMaker Clarify |
| Friendliness / humor | SageMaker Clarify |
| Model explainability | SageMaker Clarify |
| Why did the model make this prediction? | SageMaker Clarify |
| Detect bias | SageMaker Clarify |
| Statistical metrics for bias | SageMaker Clarify |
| RLHF | SageMaker Ground Truth |
| Reinforcement Learning from Human Feedback | SageMaker Ground Truth |
| Human preferences | SageMaker Ground Truth |
| Human feedback in reward function | SageMaker Ground Truth |
| Data annotation / labeling | SageMaker Ground Truth |
| Employees / third-party workers / Mechanical Turk | SageMaker Ground Truth |
| Ground Truth Plus | SageMaker Ground Truth |

---

## Key Takeaways

### SageMaker Clarify

- Evaluates and compares **foundation models**.
- Models can be evaluated on specific tasks.
- Human factors such as **friendliness and humor** can be evaluated.
- Evaluation can use an AWS-managed team or your own employees.
- Built-in datasets and custom datasets can be used.
- You can provide your own questions.
- Built-in metrics and algorithms are available.
- Provides **model explainability**.
- Helps understand why a model made a particular prediction.
- Can help debug incorrect predictions.
- Helps increase trust and understanding of models.
- Can detect potential **bias** in datasets and models.
- Uses **statistical metrics** to measure bias.
- Can identify issues such as **class imbalance**.
- Available within **SageMaker Studio**.

### SageMaker Ground Truth

- Uses humans for **model review, customization, and evaluation**.
- Helps align models with **human preferences**.
- Important for **RLHF**.
- Human feedback can be included in the reward function.
- Can be used to create and annotate data from a human perspective.
- Helps when automated processes do not align well with human preferences.
- Human reviewers can be:
  - Your employees
  - Third-party employees
  - Amazon Mechanical Turk workers
- **SageMaker Ground Truth Plus** provides a workforce for data-labeling tasks.

---
---

# Amazon SageMaker - ML Governance

Once a machine learning model is deployed and is being used by users, it is important to have **good machine learning governance**.

AWS SageMaker provides several tools to help manage and govern machine learning models.

The main governance tools are:

## 1. SageMaker Model Cards

**SageMaker Model Cards** provide a way to gather and document the essential information about a machine learning model in one place.

You can document information such as:

- **Intended uses** of the model
- **Risk rating** of the model
- **How the model was trained**
- Other important training and model details

### Why Model Cards?

They provide a central place to document important information about a model, which supports better **governance, understanding, and management**.

---

## 2. SageMaker - Model Dashboard

**SageMaker Model Dashboard** is a centralized repository where you can view and manage information about all your machine learning models in SageMaker.

It allows you to:

- View all models in one place
- Search and explore models
- Get information and insights about models
- Track the **risk rating**
- Monitor **model quality**
- Monitor **data quality**
- Identify models that may require attention

The Model Dashboard can help you track:
- Which models are deployed for inference

**Inference:** Using a trained model to make predictions on new data.

The Model Dashboard can be accessed directly from the **SageMaker console**.

### Monitoring Threshold Violations

The dashboard can help identify models that violate thresholds set for:

- Data quality
- Model quality
- Bias
- Explainability

This allows you to identify problems quickly and take action on affected models.

---

## 3. SageMaker - Role Manager

**SageMaker Role Manager** is used to define **roles and permissions** for different personas within an organization.

For example, an organization may have:

- Data Scientists
- MLOps Engineers
- Data Engineers
- Other users or teams

You can define what each role is allowed to do within SageMaker.

### Why Role Manager?

It helps establish proper **access control and governance** in SageMaker.

---

# 4. SageMaker - Model Monitor

Once a model is deployed in production, you need to make sure that its quality remains acceptable over time.

**SageMaker Model Monitor** allows you to monitor a model at the **individual model level**.

You can monitor the model:

- **Continuously**, meaning all the time
- **On a schedule**, such as once a day, once a week, etc.

### Model Quality Deviation

If the model's quality deviates from the expected standard, Model Monitor can generate an **alert**.

The alert tells you that the model may need attention.

After receiving an alert, you can take actions such as:

- Fix the underlying data
- Retrain the model
- Recalibrate the model
- Improve the model so that its quality returns to the required standard

### Example: Loan Model

Suppose you created a **loan prediction model**.

Initially, the model correctly gives loans to people who have the required credit score.

However, after six months, the model starts giving loans to people who do not have the correct credit score.

This indicates that there may be **drift in the model**.

Model Monitor can be configured to detect such problems and alert you so that you can take action.

---

# 5. SageMaker - Model Registry

**SageMaker Model Registry** is a centralized repository for **tracking, managing, and versioning machine learning models**.

It allows you to:

- Keep models in a central catalog
- Track different model versions, Change or manage model versions
- View metadata associated with a model
- Manage model approval status 

### Model Approval

One important feature of the Model Registry is the ability to create an **approval status** for a model.

For example, a model can go through a governance process where an appropriate person or team reviews and approves the model before it is registered or used.

This provides **governance and stewardship** over models.

### Why Model Registry?

It is particularly useful when:

- Automating model deployments
- Managing multiple versions of models
- Sharing models within a company
- Applying governance and approval processes

> **Model Registry = Where are my models and which version is approved?**

---

# 6. SageMaker Pipelines

**SageMaker Pipelines** allows you to create a workflow that automates the process of building, training and deploying a ML model. This is especially useful for **MLOps**.

**MLOps** applies software development and operational practices to machine learning.

SageMaker Pipelines is similar in idea to **CI/CD (Continuous Integration / Continuous Delivery)** used in software development.

- **Continuous Integration (CI):** Frequently integrate and test changes.
- **Continuous Delivery (CD):** Automatically prepare and deliver changes for deployment.

For machine learning, the idea is to continuously and automatically move models through the ML workflow and deploy them into production.

## Why Use SageMaker Pipelines?

Because the process is automated, you can:

- Build hundreds of models automatically
- Train hundreds of models automatically
- Test models automatically
- Deploy models automatically

This provides several benefits:

- **Faster iteration**
- **Reduced errors**
- **Fewer manual steps**
- **Repeatable processes**
- Automated model deployment

## SageMaker Pipeline Step Types

A SageMaker Pipeline consists of different **steps**, where each step performs a specific task.

| Step Type | Purpose |
|---|---|
| **Processing** | Data processing and tasks such as feature engineering |
| **Training** | Train the machine learning model |
| **Tuning** | Hyperparameter tuning or optimization |
| **AutoML** | Automatically train a machine learning model |
| **Model** | Create or register a SageMaker model |
| **ClarifyCheck** | Perform checks using SageMaker Clarify |
| **QualityCheck** | Check data or model quality against a baseline |

## 1. Processing

The **Processing** step is used for data processing tasks. (eg. feature engineering)


## 2. Training

The **Training** step is used to train the machine learning model.

## 3. Tuning

The **Tuning** step is used for: Hyperparameter tuning (eg. Hyperparameter Optimization)

## 4. AutoML

The **AutoML** step is used to automatically train a machine learning model.

**AutoML:** Automated Machine Learning, where parts of the model-building process are automated.

## 5. Model

The **Model** step is used to:

- Create a SageMaker model or
- Register a SageMaker model

The model can be registered in the **SageMaker Model Registry**.

## 6. ClarifyCheck

The **ClarifyCheck** step performs stuff using **SageMaker Clarify**.

So you can look for drift checks against the baseline such as :

- Data bias
- Model bias
- Model explainability
 
`ClarifyCheck = Check bias, explainability and related issues`

## 7. QualityCheck

The **QualityCheck** step checks quality against a **baseline**.

It can be used for:

- Data quality
- Model quality

**Baseline:** A reference level or expected standard used to compare the current results.

`QualityCheck = Check data/model quality`

## For a full list check docs:
https://docs.aws.amazon.com/sagemaker/latest/dg/build-and-manage-steps.html#build-and-manage-steps-types

### Explanation

```text
Processing   → Process data
Training     → Train model
Tuning       → Optimize hyperparameters
AutoML       → Automatically train a model
Model        → Create/Register model
ClarifyCheck → Check bias/explainability/drift
QualityCheck → Check data/model quality
```

---

# SageMaker Governance Tools at a Glance

| SageMaker Tool | Main Purpose |
|---|---|
| **Model Cards** | Document important model information |
| **Model Dashboard** | Centralized view of all models and their insights |
| **Role Manager** | Define roles and permissions |
| **Model Monitor** | Monitor deployed models and detect quality deviations |
| **Model Registry** | Track, manage, version, and approve models |
| **Pipelines** | Automate ML workflows for MLOps |

---

# Summary

- **SageMaker Model Cards** document essential information about a model, such as intended use, risk rating, and training details.
- **SageMaker Model Dashboard** provides a centralized place to view, search, and explore models.
- The Model Dashboard can provide insights about **risk, model quality, data quality, bias, and explainability**.
- **SageMaker Role Manager** defines roles and permissions for different personas such as data scientists, MLOps engineers, and data engineers.
- **SageMaker Model Monitor** monitors deployed models continuously or on a schedule and can generate alerts when model quality deviates.
- When problems are detected, you may need to **fix data, retrain, or recalibrate the model**.
- **SageMaker Model Registry** is a centralized repository for tracking, managing, and versioning models.
- Model Registry also supports **approval status**, which is useful for governance and automated deployments.
- **SageMaker Pipelines** automates the ML workflow and is important for **MLOps**.
- Pipelines can automate building, training, testing, and deploying models.
- Important pipeline step types include:
  - Processing
  - Training
  - Tuning
  - AutoML
  - Model
  - ClarifyCheck
  - QualityCheck

---
---

# Amazon SageMaker - Consoles

**SageMaker JumpStart** is a machine learning hub to find
- Pre-trained **foundation models**
- **Computer vision models**
- **Natural Language Processing (NLP) models**
- Pre-built **machine learning solutions**

These models and solutions can be launched directly on SageMaker.

SageMaker JumpStart provides a large collection of models from providers such as:

- **Hugging Face**
- **Databricks**
- **Meta**
- **Stability AI**
- And others

The collection of models available through JumpStart is much larger than what you would find on **Amazon Bedrock**.

### Customizing JumpStart Models

Models accessed through SageMaker JumpStart can be:

- Fully customized for your own data & your specific use case

After customization, the model can be deployed directly on SageMaker.

You still have full control over the deployment options for the specific model.

---

## Machine Learning Solutions

JumpStart also provides **pre-built ML solutions** for common business use cases.

Examples include:

- Demand forecasting
- Credit rate prediction
- Fraud detection
- Computer vision
- Other common machine learning use cases

These solutions are a little higher-level than working directly with individual models.

Instead of starting completely from a model, you can start with a solution designed for a particular business problem.

### Two Options in SageMaker JumpStart

SageMaker JumpStart mainly provides two options:

| Option | Purpose |
|---|---|
| **Machine Learning Hub** | Browse and use pre-trained ML/foundation models |
| **Machine Learning Solutions** | Start with pre-built solutions for common business use cases |

### Option 1

```text
Browse Models - directly access a few pre-built solutions
     ↓
Experiment
     ↓
Customize with some of our data to
     ↓
Fine-tune or Train from Scratch
     ↓
Deploy Directly on SageMaker
```

### Option 2

```text
Browse Pre-built Solutions
     ↓
Select a Solution
     ↓
Customize
     ↓
Deploy
```

> **JumpStart = Ready-made models + Ready-made ML solutions**

---

# SageMaker Canvas

If you are **not a developer** and do not want to write code, you can use **SageMaker Canvas** to build machine learning models.

**SageMaker Canvas** is a **visual, no-code interface** for building machine learning models.

> **No-code SageMaker interface = SageMaker Canvas**

## How SageMaker Canvas Works

Suppose you have a dataset and want to predict a column called:

**`Median House Value`**

You can tell SageMaker Canvas that:

> "From my dataset, I want to predict the `Median House Value` column."

Canvas then walks you through the process of building a machine learning model to predict that column.

You do not need to write code for this process.

## Models Available in SageMaker Canvas

Canvas provides pre-packaged models that you can use.

You can use:

- Models from **Amazon Bedrock**
- Models from **SageMaker JumpStart**
- Build your own custom models powered by AutoML powered by SageMaker Autopilot

**AutoML (Automated Machine Learning)** automates parts of the machine learning model-building process.

## Canvas and SageMaker Studio

SageMaker Canvas is part of **SageMaker Studio**.

If data transformation is required behind the scenes, Canvas can leverage the **SageMaker Data Wrangler** tool.

```text
SageMaker Studio
       │
       ├── SageMaker Canvas
       │       ↓
       │    No-code SageMaker
       │
       └── Data Wrangler
               ↓
          Data Transformation
```

---

## SageMaker Canvas - Ready-to-Use Models

**SageMaker Canvas** also provides **ready-to-use models** for different use cases.

You can select the type of use case you need, and Canvas can use the appropriate AWS AI service behind the scenes.

### Examples

| Use Case | AWS Service |
|---|---|
| **Sentiment Analysis** | Amazon Comprehend |
| **Object Detection in Images** | Amazon Rekognition |

Canvas has direct integration with AWS AI services such as:

- **Amazon Rekognition**
- **Amazon Comprehend**
- **Amazon Textract**

This makes it easier to build a complete machine learning pipeline **without writing code** while leveraging different AWS AI services.

---

## MLFlow with SageMaker

**MLFlow** is an **open-source tool** that allows machine learning teams to manage the entire machine learning lifecycle.

It can be used for activities such as:

- Tracking machine learning runs
- Running experiments
- Managing the ML lifecycle

MLFlow is a separate open-source tool, but SageMaker provides integration with it.

### MLFlow in SageMaker Studio

MLFlow does not look like SageMaker Studio itself.

However, **MLFlow can be part of SageMaker Studio** if you choose to use it.

SageMaker allows you to launch an **MLFlow Tracking Server**.

### MLFlow Tracking Server

An **MLFlow Tracking Server** is a server that runs the MLFlow software.

It allows you to:

- Track ML runs
- Perform and track experiments

You can launch the MLFlow Tracking Server easily from SageMaker.

```text
SageMaker
    ↓
Launch MLFlow Tracking Server
    ↓
MLFlow
    ↓
Track Runs + Experiments
```

SageMaker makes it easier to use **open-source tools** that are deeply integrated with AWS services.
 
> **Amazon SageMaker provides the option to launch MLFlow on SageMaker.**

---

# SageMaker JumpStart vs Canvas vs MLFlow

| Tool | Main Purpose | Coding |
|---|---|---|
| **SageMaker JumpStart** | Pre-trained models and pre-built ML solutions | Can use code/customization |
| **SageMaker Canvas** | Build ML models using a visual interface | **No code** |
| **MLFlow** | Manage ML lifecycle, track runs and experiments | Open-source tool |

---

# Summary

- **SageMaker JumpStart** is a machine learning hub for quickly getting started with ML on SageMaker.
- JumpStart provides:
  - Pre-trained foundation models
  - Computer vision models
  - NLP models
  - Pre-built ML solutions
- JumpStart has models from providers such as **Hugging Face, Databricks, Meta, and Stability AI**.
- JumpStart models can be customized for your data and use case.
- You can **fine-tune** models or **train from scratch**.
- Models are deployed directly on SageMaker, while still providing control over deployment options.
- JumpStart also provides higher-level **ML solutions** for common business use cases.
- The two main JumpStart options are:
  - **Machine Learning Hub**
  - **Machine Learning Solutions**


- **SageMaker Canvas** is a visual **no-code** interface for building ML models.
- Canvas is useful for users who do not want to write code.
- Canvas is powered by **SageMaker Autopilot / AutoML**.
- Canvas can use models from **Bedrock, JumpStart, or custom models**.
- Canvas can leverage **Data Wrangler** for data transformation.
- Canvas provides ready-to-use models and integrates with:
  - **Rekognition**
  - **Comprehend**
  - **Textract**
- **MLFlow** is an open-source tool for managing the ML lifecycle, tracking runs, and experiments.
- SageMaker allows you to launch an **MLFlow Tracking Server**.
- The key idea is that SageMaker integrates open-source ML tools such as MLFlow into its environment.

- **SageMaker JumpStart → Pre-trained models + ML solutions**
- **JumpStart Machine Learning Hub → Browse and use models**
- **JumpStart Machine Learning Solutions → Pre-built solutions for business use cases**
- **SageMaker Canvas → No-code ML**
- **SageMaker Autopilot → AutoML behind Canvas**
- **Canvas + Rekognition → Object detection**
- **Canvas + Comprehend → Sentiment analysis**
- **Canvas + Textract → Document/text extraction use cases**
- **MLFlow → Open-source ML lifecycle management**
- **MLFlow Tracking Server → Track runs and experiments**

---
---

# SageMaker Summary

## SageMaker Services and Features

| SageMaker Service / Feature | What It Does | Main Use Case |
|---|---|---|
| **SageMaker** | End-to-end machine learning service | Build, train, and deploy ML models |
| **SageMaker Automatic Model Tuning** | Tunes hyperparameters | Improve model performance |
| **SageMaker Deployment & Inference** | Provides different ways to serve models | Real-time, serverless, batch, and asynchronous inference |
| **SageMaker Studio** | Unified interface for SageMaker | Perform end-to-end ML processes |
| **SageMaker Data Wrangler** | Explores and prepares datasets and creates features | Data preparation and feature engineering |
| **SageMaker Feature Store** | Centrally stores feature metadata | Easily access and reuse features across a company |
| **SageMaker Clarify** | Compares models, explains outputs, and detects bias | Model evaluation, explainability, and bias detection |
| **SageMaker Ground Truth** | Uses human feedback for model grading and data labeling | RLHF and human-based data labeling |
| **SageMaker Model Cards** | Creates model documentation | Model governance |
| **SageMaker Model Dashboard** | Shows models in one place | Centralized model visibility |
| **SageMaker Model Monitor** | Monitors models and provides alerts | Detect model quality issues |
| **SageMaker Model Registry** | Centralized repository to manage ML model versions | Model versioning and management |
| **SageMaker Pipelines** | CICD for ML | CI/CD and MLOps |
| **SageMaker Role Manager** | Manages roles and permissions | Access control |
| **SageMaker JumpStart** | Provides model hub and pre-built ML solutions | Quickly find, customize, and deploy models |
| **SageMaker Canvas** | No-code ML interface | Build ML pipelines/models without coding |
| **MLFlow on SageMaker** | Provides MLFlow tracking servers on AWS | Track ML runs and experiments |

```text
                 SAGEMAKER
                     │
       ┌─────────────┼─────────────┐
       ↓             ↓             ↓
    BUILD          MANAGE        DEPLOY
       │             │             │
   Studio        Model Cards    Inference
   Canvas        Dashboard      Options
   JumpStart     Monitor
                 Registry
                 Role Manager
       │
       ↓
      DATA
       │
   Data Wrangler
       ↓
  Feature Store
       │
       ↓
    MODELS
       │
   Auto Tuning
   Clarify
   Ground Truth
       │
       ↓
    AUTOMATE
       │
   Pipelines
       │
       ↓
     MLOps

MLFlow
→ Track ML runs and experiments
```

- **Tune hyperparameters? → Automatic Model Tuning**
- **Unified SageMaker interface? → SageMaker Studio**
- **Prepare/transform data? → Data Wrangler**
- **Store features centrally? → Feature Store**
- **Explain model predictions? → Clarify**
- **Detect bias? → Clarify**
- **Human feedback / RLHF? → Ground Truth**
- **Document a model? → Model Cards**
- **View all models centrally? → Model Dashboard**
- **Monitor deployed model? → Model Monitor**
- **Manage/version models? → Model Registry**
- **Automate ML workflow / CI/CD? → SageMaker Pipelines**
- **Manage permissions? → Role Manager**
- **Pre-trained models / pre-built solutions? → JumpStart**
- **No-code ML? → Canvas**
- **Track ML experiments/runs with open source? → MLFlow**

---
---

# SageMaker - Extra Featues

## 1. Network Isolation Mode

**Network Isolation Mode** is used when you want to make sure that SageMaker job containers have **no outbound internet access**.

### Why Use Network Isolation?

The main purpose is **maximum security**.

During a training job, your model may use sensitive data. You may want to make sure this data cannot be leaked outside the training environment to an attacker on the internet.

With Network Isolation Mode:

- SageMaker job containers cannot access the internet.
- They cannot access **Amazon S3**.
- They cannot access resources in your **VPC**.
- They cannot access anything outside the data and resources already available to the training job.

This creates a strongly **network-isolated training environment**.

> **Network Isolation Mode → Prevents outbound network/internet access from SageMaker job containers for better security.**

---

## 2. SageMaker DeepAR Forecasting Algorithm

**DeepAR** is a SageMaker forecasting algorithm.

### Main Use

DeepAR is used to **forecast time series data**.

**Time series data:** Data collected or recorded over time, such as daily sales, monthly demand, or hourly temperature.

DeepAR Leverages an **RNN (Recurrent Neural Network)** to perform the forecasting.

**DeepAR → Time series forecasting using RNN**
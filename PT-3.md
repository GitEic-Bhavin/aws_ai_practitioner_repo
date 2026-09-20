**Question 9:**

**Question:**
A healthcare company is building a machine learning model to predict patient outcomes based on various health indicators. The data science team is exploring different techniques to improve the model's accuracy by refining the input data, specifically using feature extraction and feature selection. Understanding the key differences between these two approaches will help the team optimize the model's performance.

What do you suggest to the company?


**Correct Answer:**
**Feature extraction reduces the number of features by transforming data into a new space, while feature selection reduces the number of features by selecting the most relevant ones from the existing features.**

![alt text](fe.png)


**Hint / Key Takeaway:**

* **Feature Extraction:** Creates a new set of features by transforming the original data (e.g., using techniques like Principal Component Analysis / PCA). It combines existing features into fewer, newly transformed features.
* **Feature Selection:** Keeps a subset of the original features based on their relevance/importance (e.g., using forward selection or regularization) without altering or transforming the original feature values.
* Both techniques aim to perform **dimensionality reduction** to prevent overfitting and improve model training performance.


# AWS Certified AI Practitioner - Practice Question 10

## Question
A financial services company is exploring the adoption of generative AI to automate report generation and enhance customer service through chatbots. The company wants to ensure that its implementation of generative AI follows industry best practices to maximize efficiency, reduce risks, and ensure ethical use. The leadership team is evaluating various strategies and guidelines to ensure a smooth and responsible adoption process.

Given this use case, which of the following represents a best practice in generative AI adoption?

## Options
- [ ] Using generative AI exclusively for creative applications and avoiding its use in business operations
- [x] **Implementing guardrails and enhancing transparency for generative AI applications**
- [ ] Prioritizing rapid deployment over the ethical considerations and potential biases in AI models
- [ ] Disregarding continuous monitoring and updating of AI models after deployment

## Correct Answer
**Implementing guardrails and enhancing transparency for generative AI applications**

## Key Takeaways & Hints
* **Transparency:** Always inform users when they interact with AI (e.g., self-identification by chatbots or clear labeling of AI-generated content).
* **Guardrails:** Apply guardrails to prevent data leakage, filter toxic content, and protect against security risks like prompt injection or hallucinations.
* **Responsible AI:** Maintain ongoing monitoring, bias mitigation, and ethical checks alongside operational deployment.

# AWS Certified AI Practitioner - Practice Question 11

## Question
A retail company is utilizing Amazon Bedrock to generate personalized product descriptions and recommendations. The data science team is experimenting with the Top K inference parameter, since it is crucial to understand how adjusting the Top K parameter impacts the responses for optimizing customer interactions.

What do you suggest to the team regarding the Top K parameter?

## Options
- [ ] Influences the likelihood of the model selecting lower-probability outputs, thereby impacting the creativity of the model’s output
- [x] **Influences the number of most-likely candidates that the model considers for the next token**
- [ ] Influences the percentage of most-likely candidates that the model considers for the next token
- [ ] Specifies the sequences of characters that stop the model from generating further tokens

## Correct Answer
**Influences the number of most-likely candidates that the model considers for the next token**

## Key Takeaways & Hints
* **Top K:** Sets the fixed count ($K$) of most-likely candidate tokens considered for generating the next token.
* **Top P vs Top K:** Top K sets a fixed count of top candidate tokens, whereas Top P considers a cumulative percentage threshold of probability.
* **Temperature:** Controls the overall randomness/creativity of the generated response.

# AWS Certified AI Practitioner - Practice Question 12

## Question
Which security discipline in the Generative AI Security Scoping Matrix focuses on identifying potential threats to generative AI solutions and recommending mitigations?

## Options
- [ ] Resilience
- [x] **Risk management**
- [ ] Governance and compliance
- [ ] Legal and privacy


## Correct Answer
**Risk management**

![alt text](scmx.png)



## Key Takeaways & Hints
* **Risk Management:** Focuses on threat modeling, risk assessment, and defining mitigations for generative AI systems.
* **Governance and Compliance:** Deals with organizational policies, oversight, and compliance reporting.
* **Legal and Privacy:** Focuses on privacy laws, data protection, and regulatory compliance.
* **Resilience:** Ensures high availability, fault tolerance, and disaster recovery.

# AWS Certified AI Practitioner - Practice Question 13

## Question
A retail company is exploring machine learning algorithms to improve its customer segmentation systems. The data science team is evaluating both K-Means and K-Nearest Neighbors (KNN) algorithms but needs to understand the key differences between them, since understanding these distinctions will help the team choose the right algorithm for their specific tasks.

Given this context, what do you recommend to the company?

## Options
- [ ] K-Means is primarily used for regression tasks, while KNN is used for reducing the dimensionality of data
- [x] **K-Means is an unsupervised learning algorithm used for clustering data points into groups, while KNN is a supervised learning algorithm used for classifying data points based on their proximity to labeled examples**
- [ ] K-Means requires labeled data to form clusters, whereas KNN does not use labeled data for making predictions
- [ ] K-Means is a supervised learning algorithm used for classification, while KNN is an unsupervised learning algorithm used for clustering


## Correct Answer
**K-Means is an unsupervised learning algorithm used for clustering data points into groups, while KNN is a supervised learning algorithm used for classifying data points based on their proximity to labeled examples**

## Key Takeaways & Hints
* **K-Means:** Unsupervised learning technique used to group unlabeled items into clusters based on feature similarity (ideal for customer segmentation).
* **KNN (K-Nearest Neighbors):** Supervised learning technique used for classification and regression tasks using labeled training examples based on proximity/distance metrics.

# AWS Certified AI Practitioner - Practice Question 14

## Question
A financial services company manages a machine learning model to assess loan eligibility for its customers. The company wants to migrate to AWS Cloud and is looking at understanding the capabilities of the various SageMaker services to operationalize and manage its Machine Learning workflow.

As an AI Practitioner, what would you recommend to the company as the best-fit use case for the SageMaker Clarify service?

## Options
- [ ] You can use SageMaker Clarify to prepare ML models with no coding involved, which offers a no-code interface for building, training, and deploying machine learning models without requiring any programming skills
- [ ] You can use SageMaker Clarify to monitor the quality of a model, which involves assessing and optimizing model performance in real-time during deployment to improve its accuracy and reliability
- [ ] You can use SageMaker Clarify to automate hyperparameter tuning, which is the process of automatically optimizing the hyperparameters of a model to achieve the best performance.
- [x] **You can use SageMaker Clarify to identify potential bias in data preparation, allowing you to detect and measure bias in datasets and models to ensure fairness and transparency in machine learning applications**


## Correct Answer
**You can use SageMaker Clarify to identify potential bias in data preparation, allowing you to detect and measure bias in datasets and models to ensure fairness and transparency in machine learning applications**


## Key Takeaways & Hints
* **SageMaker Clarify:** Detects bias across the ML lifecycle and provides feature attribution reports for model explainability.
* **SageMaker Model Monitor:** Used for real-time monitoring of model quality, data drift, and bias drift post-deployment.
* **SageMaker Canvas:** No-code interface for building ML models.
* **Hyperparameter Tuning:** Handled by SageMaker's built-in Hyperparameter Optimization (HPO).

# AWS Certified AI Practitioner - Practice Question 15

## Question
Is it possible to increase both the bias and variance of a machine learning model simultaneously?

## Options
- [ ] No, it is not possible to increase both bias and variance simultaneously, as they are inversely related
- [ ] No, increasing bias always decreases variance and vice versa, so they cannot be increased at the same time
- [ ] Yes, increasing both bias and variance simultaneously will improve the model's accuracy and generalization capabilities
- [x] **Yes, it is possible to increase both bias and variance, but this typically leads to a model that performs poorly due to both underfitting and overfitting**

## Correct Answer
**Yes, it is possible to increase both bias and variance, but this typically leads to a model that performs poorly due to both underfitting and overfitting**

## Key Takeaways & Hints
* **Bias-Variance Dynamics:** While adjusting simple parameter knobs often trades off bias for variance, certain negative actions (e.g., adding irrelevant noisy features while over-simplifying key structures) can increase both.
* **Underfitting & Overfitting:** High bias causes underfitting (inability to model basic relationships), whereas high variance causes overfitting (sensitivity to noise). Having both leads to poor generalization and weak performance across all datasets.


Here are concise strategies and pattern-recognition hints for the common scenario types tested on the **AWS Certified AI Practitioner (AIF-C01)** exam:

* **Keyword Association:**
* **"No-code" / "Point-and-click" / "Business Analysts"** $\rightarrow$ **Amazon SageMaker Canvas**
* **"Data preparation" / "Cleansing" / "Tabular data visualization"** $\rightarrow$ **Amazon SageMaker Data Wrangler**
* **"Bias detection" / "Explainability" / "Feature importance"** $\rightarrow$ **SageMaker Clarify**
* **"Centralized repository to share ML features"** $\rightarrow$ **SageMaker Feature Store**
* **"Multiple layers of defense" / "Validation + Access Controls + Monitoring"** $\rightarrow$ **Defense-in-depth**


* **Foundation Models & Generative AI:**
* **Fine-Tuning vs. RAG:** Fine-tuning **changes model weights** (using labeled data). RAG **does not change weights** (it retrieves dynamic knowledge at runtime).
* **Self-Supervised Learning:** How FMs pre-train on **unlabeled, unstructured data** by creating implicit labels.
* **Multi-Modal Embeddings vs. Generative FMs:** Use **multi-modal embeddings** for cost-effective search/retrieval across text and images; reserve **generative multi-modal FMs** for generating entirely new content.


* **Security & Vulnerabilities:**
* **Poisoning:** Malicious data injected into training/fine-tuning data to compromise model behavior.
* **Prompt Leaking:** The model accidentally exposing its private system instructions, context, or previous user history.
* **Hallucination vs. Toxicity:** Hallucination is **factually incorrect/invented content** presented as true; Toxicity is **offensive, hateful, or harmful text**.


* **Model Training Dynamics:**
* **Overfitting:** Performs exceptionally well on training data, but **poorly on unseen test data**.
* **Underfitting:** Performs **poorly on both** training data and unseen test data.
* **Deterministic Logic:** If a problem can be solved using fixed, standard mathematical formulas (like basic card probability), a **rule-based algorithm** is better, cheaper, and more accurate than ML/RL.
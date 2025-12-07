# gcp_professional_machine_learning_engineer_exam_notes

**Vertex AI (60-70%, heavy emphasis)**

Vertex AI AutoML: You can train models without coding, but learn when to use AutoML effectively versus building custom models.
Vertex AI Pipelines and Orchestration: These are essential for building real-world ML systems. Expect questions on how pipelines work, the different components, how to troubleshoot them, and streamlining and automating your ML workflows for efficient and scalable machine learning solutions on Google Cloud.
Vertex AI Experiments: Keep track of different models and experiments. Make sure you learn how to track, compare, and analyze different model versions and training runs.
Vertex AI Metadata: Helps you organize all your ML stuff (models, datasets, etc.). Know how to use it to track your work and see how everything connects.
Vertex AI Model Registry: Where you store your trained models. Know how to register them, deploy them, and manage different versions.
Vertex AI Endpoints: How you make your models available for others to use. Understand how to deploy models for online prediction and the different deployment options available.
Vertex AI Feature Store: A newer service that helps you organize, store, and serve machine learning features. It can be important for improving model accuracy and consistency.
Vertex AI Training: Go beyond AutoML and explore custom training options, including pre-built containers, custom containers, and distributed training strategies.
Vertex AI Prediction: This component handles serving predictions from your deployed models. Understand different prediction methods (online, batch) and scaling options.
Vertex AI Explainable AI: Helps you understand how your models make predictions. It’s increasingly important for model transparency and debugging.
Vertex AI Model Monitoring: Vertex AI has specific tools for monitoring model performance, drift, and fairness.

**ML fundamentals are essential (20-25%)**

Types of algorithms: Know the different types of ML algorithms (like linear models, clustering, regression, and classification) and when to use each one.
Evaluation: Understand how to interpret metrics like recall, precision, and accuracy.
Monitoring: Know how to keep an eye on your models after you deploy them and spot problems like model drift or bias.
Hardware: Understand when to use TPUs, GPUs, or regular CPUs for your ML tasks.
TensorFlow and TFRecords: Be comfortable with TensorFlow and know how to use TFRecords to feed data to your models efficiently.
Data splitting and cross-validation: Understand how to split your data for training, validation, and testing. Know different cross-validation techniques.
Bias and fairness in ML: Be aware of potential biases in data and models. Understand techniques for mitigating bias and ensuring fairness.
MLOps principles: This includes concepts like continuous integration, continuous delivery, and model versioning.
Security in ML: Understand security considerations for data, models, and infrastructure.

**Other GCP services (10-15%) and final review**

Cloud Natural Language API: This one is for working with text. Understand what it can do, when you’d use it, and how much it costs.
BigQuery ML: Allows you to build and deploy models directly within BigQuery. It can be useful for simpler models or when your data is already in BigQuery.
Cloud Storage: Fundamentals for storing and accessing data for your ML workloads.
Cloud Logging and Monitoring: Essential for monitoring your ML pipelines and deployed models.
Cloud Functions: Used for lightweight serverless deployments or triggering actions in your ML workflows.
Dataflow, Pub/Sub, Firebase: These are important for building data pipelines and connecting different parts of your ML system.


Professional Machine Learning Engineer Sample Questions
https://docs.google.com/forms/d/e/1FAIpQLSeYmkCANE81qSBqLW0g2X7RoskBX9yGYQu-m1TtsjMvHabGqg/viewform

**key decision points:**
Unstructured data storage: Cloud Storage.
Structured data storage/analysis: BigQuery.
Generic problem, no custom data: Pre-trained API.
Custom problem, have data, no code skills: AutoML.
Data in BigQuery, SQL-proficient team: BigQuery ML.
Need full control/custom framework: Custom Training on Vertex AI.
Orchestrate an ML-centric workflow: Vertex AI Pipelines.
Orchestrate a complex business workflow with ML and non-ML parts: Cloud Composer.
Guarantee training-serving consistency: TFX tf.Transform or Vertex AI Feature Store.
Automate hyperparameter tuning: Vertex AI Vizier.
Monitor deployed models for drift/skew: Vertex AI Model Monitoring.


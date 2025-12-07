# gcp_professional_machine_learning_engineer_exam_notes

**Vertex AI (60-70%, heavy emphasis)** <br/>

- **Vertex AI AutoML:** You can train models without coding, but learn when to use AutoML effectively versus building custom models. <br/>
- **Vertex AI Pipelines and Orchestration:** These are essential for building real-world ML systems. Expect questions on how pipelines work, the different components, how to troubleshoot them, and streamlining and automating your ML workflows for efficient and -scalable machine learning solutions on Google Cloud. <br/>
- **Vertex AI Experiments:** Keep track of different models and experiments. Make sure you learn how to track, compare, and analyze different model versions and training runs. <br/>
- Vertex AI Metadata: Helps you organize all your ML stuff (models, datasets, etc.). Know how to use it to track your work and see how everything connects. <br/>
- Vertex AI Model Registry: Where you store your trained models. Know how to register them, deploy them, and manage different versions. <br/>
- Vertex AI Endpoints: How you make your models available for others to use. Understand how to deploy models for online prediction and the different deployment options available. <br/>
- Vertex AI Feature Store: A newer service that helps you organize, store, and serve machine learning features. It can be important for improving model accuracy and consistency. <br/>
- Vertex AI Training: Go beyond AutoML and explore custom training options, including pre-built containers, custom containers, and distributed training strategies. <br/>
- Vertex AI Prediction: This component handles serving predictions from your deployed models. Understand different prediction methods (online, batch) and scaling options. <br/>
- Vertex AI Explainable AI: Helps you understand how your models make predictions. It’s increasingly important for model transparency and debugging.<br/>
- Vertex AI Model Monitoring: Vertex AI has specific tools for monitoring model performance, drift, and fairness. <br/>

**ML fundamentals are essential (20-25%)** <br/>

Types of algorithms: Know the different types of ML algorithms (like linear models, clustering, regression, and classification) and when to use each one. <br/>
Evaluation: Understand how to interpret metrics like recall, precision, and accuracy. <br/>
Monitoring: Know how to keep an eye on your models after you deploy them and spot problems like model drift or bias. <br/>
Hardware: Understand when to use TPUs, GPUs, or regular CPUs for your ML tasks. <br/>
TensorFlow and TFRecords: Be comfortable with TensorFlow and know how to use TFRecords to feed data to your models efficiently. <br/>
Data splitting and cross-validation: Understand how to split your data for training, validation, and testing. Know different cross-validation techniques.  <br/>
Bias and fairness in ML: Be aware of potential biases in data and models. Understand techniques for mitigating bias and ensuring fairness.<br/>
MLOps principles: This includes concepts like continuous integration, continuous delivery, and model versioning. <br/>
Security in ML: Understand security considerations for data, models, and infrastructure. <br/>

**Other GCP services (10-15%) and final review** <br/>

Cloud Natural Language API: This one is for working with text. Understand what it can do, when you’d use it, and how much it costs. <br/>
BigQuery ML: Allows you to build and deploy models directly within BigQuery. It can be useful for simpler models or when your data is already in BigQuery. <br/>
Cloud Storage: Fundamentals for storing and accessing data for your ML workloads. <br/>
Cloud Logging and Monitoring: Essential for monitoring your ML pipelines and deployed models. <br/>
Cloud Functions: Used for lightweight serverless deployments or triggering actions in your ML workflows. <br/>
Dataflow, Pub/Sub, Firebase: These are important for building data pipelines and connecting different parts of your ML system. <br/>


Professional Machine Learning Engineer Sample Questions <br/> 
https://docs.google.com/forms/d/e/1FAIpQLSeYmkCANE81qSBqLW0g2X7RoskBX9yGYQu-m1TtsjMvHabGqg/viewform <br/>

**key decision points:** <br/>
Unstructured data storage: Cloud Storage. <br/>
Structured data storage/analysis: BigQuery. <br/>
Generic problem, no custom data: Pre-trained API. <br/> 
Custom problem, have data, no code skills: AutoML. <br/>
Data in BigQuery, SQL-proficient team: BigQuery ML. <br/>
Need full control/custom framework: Custom Training on Vertex AI. <br/>
Orchestrate an ML-centric workflow: Vertex AI Pipelines. <br/>
Orchestrate a complex business workflow with ML and non-ML parts: Cloud Composer. <br/>
Guarantee training-serving consistency: TFX tf.Transform or Vertex AI Feature Store. <br/>
Automate hyperparameter tuning: Vertex AI Vizier. <br/>
Monitor deployed models for drift/skew: Vertex AI Model Monitoring. <br/>


In Google Cloud exams, hardware selection questions are often binary. 


<img width="909" height="619" alt="image" src="https://github.com/user-attachments/assets/6a424e56-89cf-49f7-85e2-f651315506e8" />


**GPUs**
- Models with a significant number of custom PyTorch/JAX operations that must run at least partially on CPUs
- Models with TensorFlow ops that are not available on Cloud TPU (see the list of available TensorFlow ops)
- Medium-to-large models with larger effective batch sizes

**TPUs**
- Models dominated by matrix computations
- Models with no custom PyTorch/JAX operations inside the main training loop
- Models that train for weeks or months
- Large models with large effective batch sizes
- Models with ultra-large embeddings common in advanced ranking and recommendation workloads

**Cloud TPUs are not suited to the following workloads:
**
- Linear algebra programs that require frequent branching or contain many element-wise algebra operations
- Workloads that require high-precision arithmetic
- Neural network workloads that contain custom operations in the main training loop

src: https://docs.cloud.google.com/tpu/docs/intro-to-tpu#when_to_use_tpus

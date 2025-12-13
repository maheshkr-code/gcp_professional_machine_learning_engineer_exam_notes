# How to reduce the model size

Post-training quantization is a conversion technique that can reduce model size while also improving CPU and hardware accelerator latency, with little degradation in model accuracy. You can quantize an already-trained float TensorFlow model when you convert it to LiteRT format using the LiteRT Converter.LiteRT currently supports optimization via quantization, pruning and clustering

# How can I reduce the inference latency? 

**Question: ** </br>
Without retraining the model, but aiming to reduce inference time by 50% even with a slight compromise in accuracy, which model optimization technique should you initially attempt?
Answer: Dynamic range quantization

**Reason: **  </br>
Dynamic range quantization is a post-training optimization technique that reduces model size and improves inference speed without retraining. It converts 32-bit floating-point weights to 8-bit integers, while activations are dynamically quantized during inference. This process typically yields up to 4× smaller model size and up to 2–4× faster inference, often with only a minor loss in accuracy.

It’s ideal when latency and resource efficiency matter more than marginal accuracy improvements — for example, mobile gaming or edge deployments.

Importantly, it can be applied after training using TensorFlow Lite’s tf.lite.TFLiteConverter with optimizations = [tf.lite.Optimize.DEFAULT], without access to the training dataset.

Docs references
[[[TensorFlow Lite Model Optimization — Dynamic Range Quantization](url)]](https://www.tensorflow.org/lite/performance/post_training_quant)

# Can I try Weight pruning to reduce the inference latency? No

Pruning removes less significant weights to create sparse models, improving size and sometimes speed. However, the pruned model often requires retraining or fine-tuning to recover lost accuracy.
Without retraining, pruning can cause significant degradation and typically doesn’t yield the same real-world inference speedup as quantization on edge hardware.

# Can I use Model distillation to reduce the model interencning latency? No 

Distillation transfers knowledge from a large “teacher” model -> smaller “student” model. It requires retraining a new student model using soft labels. If Retraining is allowed, then this can be an answer. 

# For post-training latency improvements without retraining, start with quantization - especially dynamic range quantization for CPU inference or full integer quantization for edge devices with hardware acceleration.




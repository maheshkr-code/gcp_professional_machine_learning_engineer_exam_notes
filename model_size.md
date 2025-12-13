# How to reduce the model size

Post-training quantization is a conversion technique that can reduce model size while also improving CPU and hardware accelerator latency, with little degradation in model accuracy. You can quantize an already-trained float TensorFlow model when you convert it to LiteRT format using the LiteRT Converter.LiteRT currently supports optimization via quantization, pruning and clustering

# How to reduce the inference latency

**Question: **
Without retraining the model, but aiming to reduce inference time by 50% even with a slight compromise in accuracy, which model optimization technique should you initially attempt?
Answer: Dynamic range quantization

**Reason: **
Dynamic range quantization is a post-training optimization technique that reduces model size and improves inference speed without retraining. It converts 32-bit floating-point weights to 8-bit integers, while activations are dynamically quantized during inference. This process typically yields up to 4× smaller model size and up to 2–4× faster inference, often with only a minor loss in accuracy.

It’s ideal when latency and resource efficiency matter more than marginal accuracy improvements — for example, mobile gaming or edge deployments.

Importantly, it can be applied after training using TensorFlow Lite’s tf.lite.TFLiteConverter with optimizations = [tf.lite.Optimize.DEFAULT], without access to the training dataset.

Docs references
[[TensorFlow Lite Model Optimization — Dynamic Range Quantization](url)](https://www.tensorflow.org/lite/performance/post_training_quant)


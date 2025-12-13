
**The Core Difference between parameter tuning vs hyperparameter tuning** </br>
Parameter Tuning (Model Training): This is the internal process where the model learns from the data. You do not set these manually; the algorithm calculates them.

Model Parameters (The "Learned" Variables) -- These are the internal variables that the model adjusts automatically during the training process to minimize error. </br> 
Google Cloud Context: When you run a standard Vertex AI Custom Training Job, the "output" is a model file (like model.pb) containing these tuned parameters. You generally don't "tune" these yourself; you train the model, and the model tunes its own parameters.

**Hyperparameter Tuning:** </br> 
This is the external process where you (the human) set configuration values before training begins to control how the model learns.
These are the settings you choose before you start training. They govern the training process itself </br> 
What they are: Learning rate, Batch size, Number of hidden layers, Number of epochs, or Drop-out rate. </br> 
Vertex AI runs multiple trials (training jobs) in parallel or sequence, testing different combinations to find which one results in the best model.
</br> 
<img width="953" height="418" alt="image" src="https://github.com/user-attachments/assets/98f09100-211b-4f00-a2df-5cf74e9dd1b1" />

# Neural Networks
A neural network that learns the XOR function — impossible for a single linear model — using only NumPy. Every component was implemented from scratch including forward pass, loss calculation, and backpropagation.
Key Concepts
•	Neuron formula: output = f(w·x + b)
•	Activation functions: ReLU = max(0,x) for hidden layers, Sigmoid = 1/(1+e⁻ˣ) for output
•	Training loop: forward pass → loss → backpropagation → weight update
•	Gradient descent: W = W - learning_rate × gradient

Result
Input [x1, x2]	Correct Answer	Prediction	Confidence
[0, 0]	0	0.0176	✓
[0, 1]	1	0.9921	✓
[1, 0]	1	0.9921	✓
[1, 1]	0	0.0066	✓



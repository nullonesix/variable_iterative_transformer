# variable_iterative_transformer

This is a variable iterative transformer.
If its maximum output probabilities for the given batch are not all > some threshold probability,
it iterates by using the output probabilities as the new input instead of evaluating the
criterion until it reaches the threshold. See unrolled diagram below:
one-hot token from training data -> transformer -> probabilities -> ... -> 
probabilities -> transformer -> probabilities meeting threshold -> output token sample
Code from the PyTorch language modelling tutorial is used as the baseline.

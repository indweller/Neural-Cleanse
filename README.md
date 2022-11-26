# Neural-Cleanse
My implementation of the [Neural Cleanse](https://people.cs.uchicago.edu/~ravenben/publications/pdf/backdoor-sp19.pdf) paper
for the trojan analysis track of the NeurIPS Trojan Detection Challenge 2022.

I reconstruct the trigger using clean input data and trojaned model. This is done as follows:
1. For a given output label, we treat it as the potential target label and optimize for a minimal 
trigger needed to misclassigfy clean examples of all the other label as the target label.
2. Perform this for all the possible output labels for the model.

Additionally, one may want to apply some sort of anomaly detection to detect the trigger that is significantly different from the other
triggers.

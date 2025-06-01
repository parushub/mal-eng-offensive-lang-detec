This project aims to detect offensive language in Malayalam-English code-mixed text,
particularly in social media contexts where language mixing and evolving trends are common.
Using the DravidianCodemix Malayalam dataset, which contains labeled comments, we
developed multiple classification approaches to improve detection accuracy despite significant
class imbalance.
Initially, BERT embeddings with class weights were applied to four classifiers—Random
Forest, Logistic Regression, KNN, and Naïve Bayes—using majority voting. However, due
to imbalance issues, we implemented a Multilayer Perceptron (MLP) trained with BERT
embeddings, class weights, and focal loss, achieving 87%.
These models are integrated into a simple frontend implementation for real-time comment
testing. The four-classifier approach retains majority voting, while the MLP model operates
independently, enhancing offensive language detection in multilingual social media text

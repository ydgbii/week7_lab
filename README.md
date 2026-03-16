# 
K-Nearest Neighbors (KNN) is a simple, instance-based (lazy) learning algorithm. Unlike eager learners that build a model during training, KNN defers all computation until prediction time: given a new point, it finds the k training examples closest to it (by some distance, usually Euclidean) and assigns the majority class among those neighbors. No explicit model is learned—the "model" is the entire training set.

Because KNN is distance-based, the choice of distance metric (Euclidean, Manhattan, Minkowski) and, crucially, the value of k strongly affect performance. Too small k leads to overfitting and noise sensitivity; too large k can underfit and blur class boundaries. Thus k selection (e.g., via elbow method or cross-validation) is essential.

In this lab we implement KNN from scratch using only NumPy on a simple 2D synthetic dataset, then solve the same problem with Scikit-learn and compare accuracy, parameters, and visualizations (decision boundaries, accuracy vs k). We also cover k selection methods and end with marked exercises on a 3-class dataset, sklearn comparison, and a real-world dataset.


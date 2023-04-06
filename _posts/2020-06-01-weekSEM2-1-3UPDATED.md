---
layout: post
title: Semester 2 | Weeks 1-3
---

In the previous semester, we achieved a working model using a single training example. Now, our next step is to expand our training data to include a larger portion of the dataset. Additionally, we'll divide the data into training, validation, and test sets. The training set, which is typically the largest, helps the model learn through multiple iterations, updating its internal parameters as it progresses. The validation set evaluates the model's performance and helps fine-tune its hyperparameters, which control the model's behavior. Lastly, the test set assesses the model's performance after training, providing a sample of how it generalizes to new, unseen data.

Dividing the data into these distinct sets ensures the model doesn't learn from the validation and test sets, preventing overfitting, which occurs when the model "memorizes" its training data. Overfitting is usually identified when validation error increases while training error decreases. Eventually, we'll use the validation data to fine-tune the model's hyperparameters.

When scaling our dataset, we encountered a problem with the matrix sizes returned from our dataloader. Our training loop came across a few examples of matrices that weren't the expected size. After troubleshooting our pipeline and re-examining our data, we discovered strings of nucleotide bases that weren't correctly converted into matrices by our one-hot encoder. Once we identified and fixed the issue, we allocated chromosomes 2, 3, and 5 for testing; chromosomes 1, 7, and 9 for validation; and the remaining numbered chromosomes for training. We then modified our loop to iterate through all examples in the training data and successfully processed the entire training set. Now that we have fully functional training, validation, and test sets, we can adjust the complexity of our model and training loops. 


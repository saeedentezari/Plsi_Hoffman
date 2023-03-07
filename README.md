# [Hofmann, 1999](https://www.iro.umontreal.ca/~nie/IFT6255/Hofmann-UAI99.pdf): Probabilistic Latent Semantic Analysis

A statistical technique of two-mode (term-document) and co-occurence of data, based on a mixture decomposition derived from a latent class model.
Number of latent topics is a hyperparameter of the model which should be tuned for each dataset. This model uses Expectation Maximization (EM)
to maximize likelihood on data, and to avoid overfitting, proposes a generalization of maximum likelihood model fitting called Tempered EM. It's a
modification of [Deerwester, 1990](http://wordvec.colorado.edu/papers/Deerwester_1990.pdf)
which is based on linear algebra and performs a Sigular Value Decomposition of co-occurence tables (of term-document).

You can obtain a similarity metric for documents and/or terms by this model. Anything similar to term-document structure can be considered by this model,
for example user-purchase, which each user (~ document) can have multiple purchases (~ terms), and then you can gain the similarity of users or purchases.

You can find my functional implementation of PLSI in the `plsimodel.ipynb` file. It's not OOP implementation, but it's easy to create a `PlsiModel` class then.

# Modern Approaches in Natural Language Processing

In the last few years, there have been several breakthroughs concerning the methodologies used in Natural Language Processing (NLP). These breakthroughs originate from both new modeling frameworks as well as from improvements in the availability of computational and lexical resources.

In this seminar, we are planning to review these frameworks starting with a methodology that can be seen as the beginning of modern NLP: Word Embeddings.

We will further include a chapter about the integration of embeddings into end-to-end trainable approaches, namely convolutional and recurrent neural networks. As Attention-based models and transfer learning approaches are the foundation of most of the recent state-of-the-art models, we will cover these two topics extensively in the second part of our our booklet.

Further parts will cover existing software implementations of transfer learning architectures and benchmark tasks/data sets for evaluating state-of-the-art models. In the concluding chapter, two use cases of the discussed methods will be presented.


## How this book came about

This book is the result of a student seminar for Master Statistics and Master Data Science at the LMU in the summer semester 2020.
Each student in the seminar wrote about a specific chapter of the book to pass the seminar.

## How to build the book

Step 0: Prerequisites

Make sure you have git and R up and running on your computer.

Step 1: Clone the repository to your machine

With RStudio: https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN

With command-line:
```
git clone git@github.com:slds-lmu/seminar_nlp_ss20.git
```

Step 2: Install dependencies

Start R in the project folder:

```
install.packages("devtools")
devtools::install_dev_deps()
```

Step 3: Render the book (R commands)

```{r}
# HTML
bookdown::render_book('./', 'bookdown::gitbook')
# PDF
bookdown::render_book('./', 'bookdown::pdf_book')
```



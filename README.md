# The-functioning-of-GPT-type-LLM-s
# Introduction

In this guide, I want you to understand in detailed how the GPT system works (**Generative Pre-trained Transformer**) system. 
# The Datasets

## What is a dataset and what is it used for ?

Un dataset est un **ensemble de données structurées**, comme par exemple :
A dataset is a structured set of data, such as 

- a set of penguins photo's 🐧,
    
- a set of all the works of Shakespeare  📖,
    
- or a list of all the meals of an individual during a year🥘.    

These data can be **labeled**, meaning that each piece of data is associated with a label. If we take the dataset example with all the meals of an individual over one year, each meal can be labeled by associating the day and the time of day the when the meal was taken.

Dataset are used in different fields like **machine learning** and **database creation**.

When there is a collection of texts in a dataset, we refer to it as a **corpus**.

## What role do datasets play in GPT model training ?

Datasets are the most important component of language models because they shape the **style**, the **quality of language** and the **knowledge of a model**.

## WebText

The model GPT 2 and later ones from OpenAI are trained on **WebText**.

Webtext is a dataset developed by OpenAI. It collects the content of every **outgoing link from Reddit** (a forum where users share, comment, and vote in thematic communities called subreddits) with at least of 3 karma points (likes).

Webtext is based on **45 million links**, including **8 million documents**, for a total of **40 GB of text**.

**WebText contains zero documents from Wikipedia.**

There are 2 main reasons for this :

- To diversify the language (Wikipedia has a neutral and highly structured style)

- To increase repetition in the data

WebText **isn't open-source **(public), but there are similar datasets open-source like [OpenWebText](https://github.com/jcpeterson/openwebtext) or even [The Pile](https://pile.eleuther.ai/).

## Datasets You Can Use

We often choose a dataset based on its size and type of language.

Tiny dataset: 

- **Tiny Shakespeare** : [https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt) (Tiny—they are recommended for tiny models.)
    
- **Wikipedia** : [https://huggingface.co/datasets/openskyml/wikipedia](https://huggingface.co/datasets/openskyml/wikipedia) (available in many language)
    
- **Open Artificial Knowledge** : [https://oakdataset.org/](https://oakdataset.org/) (Data is collected by LLM models like ChatGPT, Claude, and Gemini.i)
    

Heavier dataset:

- **OpenWebText** : [https://github.com/jcpeterson/openwebtext](https://github.com/jcpeterson/openwebtext) (38 GB open-source version of WebText)
    
- **The Pile** : [https://pile.eleuther.ai](https://pile.eleuther.ai/) (886 GB corpus used by models like GPT-Neo and LLaMA.)

# Tokenisation 

## Tokenization — what is it?

To understand a text, our GPT model needs to **perform mathematical operations on the words**. But on raw text, it's just impossible. For that, we need to **tokenize** our text. That is to say, that we will **transform and split it into text units** to adapt it to our model. We say that we split it into tokens.

In the example of a model like GPT, we begin by **taking a text corpus and splitting it into units**. Each unit is **added into a list of vocabulary with an ID** if it doesn’t already exist. 

Then our model is **ready** to tokenize. The text will be split into units, and each unit in the text is replaced by its associated number.

![Miro Image](https://miro.medium.com/v2/resize:fit:828/format:webp/1*gWP5Whykah1101EpYy17qQ.png)

*Source Image : https://teetracker.medium.com/llm-fine-tuning-step-tokenizing-caebb280cfc2

The main question, therefore, is how we will split our text. We will explore the different approaches available to us.


# CSE-576-NLP-Dev-engers
Logical Reasoning Dataset and Model Creations

## Introduction
The purpose of this project is to explore the logical reasoning capabilities of GPT3, the latest natural language processing model developed by OpenAI. GPT3 is a large-scale, deep-learning language model that has been trained on a vast corpus of natural language text. This model has been shown to have impressive performance on a variety of tasks, from text generation to question answering. By examining the performance of GPT3 on tasks involving logical reasoning, this project aims to gain insights into the capabilities of the model and how it can be applied to real-world problems. Logical reasoning is a fundamental cognitive ability, and it is an essential component of problem-solving, decision-making, and other higher-level thinking skills. The ability to reason logically is a key component of human intelligence and is critical for success in many areas. Thus, the ability to accurately assess GPT3’s logical reasoning capabilities is of great importance.

To evaluate the model’s logical reasoning capabilities, we will create a series of tasks designed to assess the model’s ability to make inferences, draw conclusions, and solve problems. Each task will be designed with the goal of assessing the model’s ability to reason logically. Additionally, we will assess the model’s performance on tasks involving natural language processing and text understanding. We will then compare the performance of GPT3 on these tasks to the performance of other language models. Once we have evaluated the performance of GPT3 on logical reasoning tasks, we will use the insights gained to train a BERT model for label prediction. BERT is a deep learning model developed by Google that is specifically designed for natural language understanding tasks. Training a BERT model for label prediction will allow us to further explore the capabilities of GPT3 and to determine if the model can be used to accurately predict labels based on natural language inputs.

Overall, this project will provide an in-depth exploration into the logical reasoning capabilities of GPT3 and will allow us to gain insights into how the model can be applied to real-world problems. By evaluating the performance of GPT3 on logical reasoning tasks and training a BERT model for label prediction, we will be able to better understand the potential of GPT3 and determine how it can be applied in a variety of areas.

## Methods
### Manual Data Generation

We created 5 samples for each of the logic. Upon cross-referencing and feedback from the professor, we updated and corrected some of them. This had to be stored in a simple JSON, structured with the Type, Subtype, Premise, Hypothesis, and Label fields. The simple followed JSON format is given below.

### Data Creation using GPT-3 (Davinci - 2)

Each group member used GPT-3 to generate more data samples, roughly 10 times the size of manual samples. This exercise was to leverage prompt engineering and GPT3’s learning capability. Since it can handle reading comprehension tasks, it will understand the pattern of the texts given to it.

This is the prompt we used for generating the data.
 
“Create 10 new reasoning examples similar to the samples below. 
Use different topics and also generate a few false labels. Do not repeat examples. Hypothesis and Premise cannot be the same.”

For the most part, GPT3 was very effective at generating additional examples, but occasionally it would repeat data points or create examples that are very similar to existing ones. When this occurred, we introduced a few tactics:
Variance Prompting: Adding “Do not repeat the topics” or “Do not repeat the premises” will encourage the model to generate new examples
Temperature adjustment: Raising the temperature parameter makes the outputs more random, potentially getting GPT3 out of a rut
Presence Penalty: Adding a presence penalty discourages GPT3 from generating words that already exist, increasing the variety

## Experimentation - Models Used

### GPT-3 (Davinci 2 and 3)

GPT-3 is an autoregressive generative language model developed by OpenAI, which incorporates only the decoder portion of the transformer model. There are a few versions of GPT-3, of varying speed and power, but in this project, we incorporated Davinci 2 and 3. Davinci is the most powerful line of GPT-3 models and they should be able to handle any task that the others can handle. Davinci 2 was used for data generation, as Davinci 3 was not out yet. We used Davinci 3 for the evaluation of GPT-3 because we wanted to see the best GPT-3 could offer us.

### BERT Base Uncased

Bert-base-uncased is a Google-developed pre-trained model that uses a deep bidirectional transformer pre-trained on a huge corpus of lowercased (uncased) text. This model can be utilized to rapidly generate a model for natural languages processing tasks like text classification, question answering, and language comprehension. It is trained on a variety of tasks and datasets to generate a strong and potent general-purpose model.

### BERT Large Uncased

The BERT Large Uncased model is an upgrade of the Bert base uncased model. It is a sophisticated, bidirectional transformer that has been trained on an even larger corpus of uncased text. It is aimed to capture more complicated word-sentence interactions in natural language processing tasks. It is trained on a variety of tasks and datasets, resulting in a model that is more powerful and robust than its predecessor.




## Links to Refer 
- https://calcworkshop.com/logic/rules-inference/
- https://tutorialforbeginner.com/inference-in-first-order-logic-in-ai


## Team Members
- [Akash Kant](https://github.com/akashkthkr)
- [Tejesh Andhavarapu](https://github.com/tejesh5 )
- [Raviram Mamidi](https://github.com/ravirammamidi)
- [Micah Secrest](https://github.com/micahsecrest )

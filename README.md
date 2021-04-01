# IIT-Indore_Bridgei2i

## Problem Statement Breakdown:
The problem statement was the fusion of three sub tasks:
**Task 1** Theme Classification
**Task 2** Aspect Based Sentiment Classification
**Task 3** Headline Generation

## Structure
The entire folder is arranged in the following manner:

### 1. main:
There are five notebook scripts located in the base directory. A short description about them is as follows:
1. **Task1&2.ipynb**: Used to preprocess the dataset, and train distilBERT classifier and implement ABSA code for mobile brand and its corresponding sentiment analysis.
2. **Task3.ipynb**: Used to obtain metrics for different Headline Generation models, via Fine-tuned saved models.
3. **Pegasus_FineTune.ipynb**: Used to fine tune Pegasus for summarization task on the given dataset.
4. **T5_FineTune.ipynb**: Used to fine tune T5 model for summarization task on the given dataset.
5. **Evaluation.ipynb**: Used for evaluation of the testing data. Contains code for all three tasks.

### 2. results
Consists of two output files: Output1 and Output2. A description about them is as follows:
1. **Output1.csv**: Contains TextID, Predicted Labels, and generated headlines.
2. **Output2.csv**: Contains TextID, Predicted Labels and Extracted Brands and their sentiments.

### 3. Development Data
Contains training data as provided under the problem statement.

### 4. Evaluation Datasets
Comprises of evaluation dataset as provided.

### 5. Requirements
The requirements folder comprises of five ``txt`` files, containing required libraries version for each of the five notebooks mentioned above.

### 6. writeups
It contains two files: ``Technical Report.pdf`` and ``Presentation.pdf``. Both the files contains technical documentation related to the business problem explanation, pipeline components, and presentation files.

## Usage
The notebook files *Task1&2.ipynb* and *Task3.ipynb* both individually contains data preprocessing functions. But the preprocessing may take a variable amount of time, depending upon the number of requests to the Google Translation API by a given IP Address, and may be impacted by unavailibility of service due to high amount of API requests (in the scenario of running the code multiple times). However, for stable runtimes of the translation process, the paid version of the API can be used. We have used the open source version of the same, in accordance to the rules of the competition. 

For Headline Generation (Task3 and Evaluation), first run the scripts ``Pegasus_FineTune.ipynb`` and ``T5_FineTune.ipynb`` present in the **main** folder to generate savedmodels for inference. For "Theme Classification" and "Aspect Based Sentiment Classification", directly run the *Task1&2.ipynb* file.

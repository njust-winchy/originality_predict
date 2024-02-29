# Automated Originality Assessment of academic Paper: A Collaborative Approach Integrating Human Expertise and Large Language Models
## Overview
**Dataset and source code for paper "Automated Originality Assessment of academic Paper: A Collaborative Approach Integrating Human Expertise and Large Language Models".**
This study proposes utilizing peer reviews and the methodology section of academic papers to assess the originality and decision-making of academic articles. The key contributions of this paper are as follows:
- We proposed a novel approach for predicting the originality of scholarly papers and decision-making.
- We explored a novel method to leverage the knowledge of both human and artificial intelligence in aiding deep learning models to achieve enhanced performance.
- We designed a text-guided fusion module to guide and integrate the knowledge of both human and artificial intelligence, enabling effective utilization of the knowledge.
- The thorough experiments show that our method is effective, and has achieved commendable results.

## Directory structure
<pre>
originality_predict                               Root directory
├── Code                                          Source code folder
│   ├── baseline_model                            Baseline model folder
│   │    ├── load_method.py                       Load data for Review and Method as input
│   │    ├── main.py                              Train the model for Review and Feedback as input
│   │    ├── method_main.py                       Train the model for Review and Method as input
│   │    ├── model.py                             Model structure
│   │    ├── predict.py                           Predict the result
│   │    ├── split_data.py                        Load data for Review and Feedback as input
│   │    ├── util.py                              Data process tool
│   ├── Bi_interaction.py                         Proposed model structure      
│   ├── p_predict.py                              Predict the result
│   └── proposed_main.py                          Train the proposed model 
│   └── read_data.py                              Load data for Review and Feedback
├── Dataset                                        Preprocessed Dataset
│
└── README.md
</pre>
## Dataset Discription
The dataset contains four contents: 
  - "novelty_sentence": Originality evaluation sentences by reviewers
  - "chat_review"： Feedback from ChatGPT
  - "nov_score":  Technical Novelty And Significance score
  - "decision":  Paper decsion
## Quick Start
    - <code>python ./Code/baseline_model./method_main.py</code>  Execute this command to train model with Review and Method as input.
    - <code>python ./Code/baseline_model./main.py</code>  Execute this command to train model with Review and Feedback as input.
    - <code>python ./Code/proposed_main.py</code>  Execute this command to train our proposed model.
## Main result
- Results of originality prediction.
|Models|	|Review & method|	|||Review & feedback|||
||	|F1|	|Accuracy|	|F1|	|Accuracy|
|BERT|	|0.70|	|0.71|	|0.72|	|0.72|
|RoBERTa|	|0.68|	|0.67|	|0.71|	|0.71|
|SciBERT|	|0.70|	|0.71|	|0.73|	|0.74|
|XLNet|	|0.62|	|0.62|	|0.69|	|0.71|
|AlBERT|	|0.52|	|0.54|	|0.64|	|0.64|
|Ours-BERT|	|-|	|-|	|0.81|	|0.82|
|Ours- RoBERTa|	|-|	|-|	|0.78|	|0.79|
|Ours- SciBERT|	|-|	|-|	|0.83|	|0.84|
|Ours- XLNet|	|-|	|-|	|0.78|	|0.79|
|Ours- AlBERT|	|-|	|-|	|0.76|	|0.77|

# Automated Originality Assessment of academic Paper: A Collaborative Approach Integrating Human Expertise and Large Language Models

## Overview

**Model overview**
![c67c171d9cee7be81fce78e3b5d73fa](https://github.com/njust-winchy/originality_predict/assets/108659065/587c1b33-469e-4d36-aa21-c460c7b68a5d)

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

<b> </b>
    - <code> python ./Code/baseline_model./method_main.py</code>  Execute this command to train model with Review and Method as input.<br>
    - <code> python ./Code/baseline_model./main.py</code>  Execute this command to train model with Review and Feedback as input.<br>
    - <code> python ./Code/proposed_main.py</code>  Execute this command to train our proposed model.<br>
## Main result

- <b>Results of originality prediction.</b><br>
<div align=center>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none'>
 <tr>
  <td width=184 rowspan=2 style='width:138.25pt;border:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><a
  name="_Hlk160115425"><span lang=EN-US style='font-size:12.0pt;font-family:
  "Times New Roman",serif'>Models</span></a></p>
  </td>
  <td width=184 colspan=2 style='width:138.25pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Review &amp;
  method</span></p>
  </td>
  <td width=184 colspan=2 style='width:138.3pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Review &amp;
  feedback</span></p>
  </td>
 </tr>
 <tr>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>F1</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Accuracy</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>F1</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Accuracy</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>BERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.70</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.72</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.72</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>RoBERTa</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.68</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.67</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>SciBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.70</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.73</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.74</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>XLNet</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.62</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.62</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.69</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>AlBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.52</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.54</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.64</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.64</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours-BERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.81</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.82</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- RoBERTa</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.78</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.79</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- SciBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><b><span
  lang=EN-US style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.83</span></b></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><b><span
  lang=EN-US style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.84</span></b></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- XLNet</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.78</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.79</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- AlBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.76</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.77</span></p>
  </td>
 </tr>
</table>

</div>

- <b>Results of decision prediction</b><br>

<div align=center>
<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none'>
 <tr>
  <td width=184 rowspan=2 style='width:138.25pt;border:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Models</span></p>
  </td>
  <td width=184 colspan=2 style='width:138.25pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Review &amp;
  method</span></p>
  </td>
  <td width=184 colspan=2 style='width:138.3pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Review &amp;
  feedback</span></p>
  </td>
 </tr>
 <tr>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>F1</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Accuracy</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>F1</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Accuracy</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>BERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.75</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.75</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.76</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.76</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>RoBERTa</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.73</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.74</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>SciBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.77</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.77</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.78</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.78</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>XLNet</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.72</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.72</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.73</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.73</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>AlBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.71</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.74</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.74</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours-BERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.78</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.78</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- RoBERTa</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.76</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.76</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- SciBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><b><span
  lang=EN-US style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.79</span></b></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><b><span
  lang=EN-US style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.79</span></b></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- XLNet</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.74</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.74</span></p>
  </td>
 </tr>
 <tr>
  <td width=184 style='width:138.25pt;border:solid windowtext 1.0pt;border-top:
  none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>Ours- AlBERT</span></p>
  </td>
  <td width=92 style='width:69.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>-</span></p>
  </td>
  <td width=92 style='width:69.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.76</span></p>
  </td>
  <td width=92 style='width:69.15pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
  style='font-size:12.0pt;font-family:"Times New Roman",serif'>0.76</span></p>
  </td>
 </tr>
</table>
</div>
## Case Study

![2a6640a5868e6464eebc35e0cfed68b](https://github.com/njust-winchy/originality_predict/assets/108659065/623ebff2-d4d2-402e-9d71-463742fce431)

## Dependency packages
System environment is set up according to the following configuration:
- transformers==4.16.2
- nltk==3.6.7
- matplotlib==3.5.1
- scikit-learn==1.1.3
- pytorch 2.0.1
- tqdm 4.65.0
- numpy 1.24.1
# Acknowledgement
We thank the openreview.net team for the commitment to promoting transparency and openness in scientific communication. Aspect identifying tool what we used from Yuan et al [1] (https://github.com/neulab/ReviewAdvisor).
# Reference
[1] Yuan, W., Liu, P., Neubig, G.: Can we automate scientific reviewing? Journal of Artificial Intelligence Research 75, 171–212 (2022) <br>

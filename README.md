# TextAnalytics_SharedTask

How to Ask Good Questions? Try to Leverage Paraphrases” (ACL 2020)
https://aclanthology.org/2020.acl-main.545.pdf


This paper focuses on the task of question generation (QG): generating a natural question given a context passage and an answer. 
The authors propose a multi-task learning approach where question generation is the main task and paraphrase generation is used as an auxiliary task to improve the fluency and
diversity of questions. 
They create paraphrase supervision using back-translation, and they also introduce a diversity-promoting loss to encourage varied question patterns.

## Proposed Models
i. Baseline
• Reimplement the model as described in the paper: QG + paraphrasing using multi-task training, with
back-translated paraphrases.
ii. Additional Extensions
• Try pretrained encoder-decoder models like T5 or BART for the same setup.
• Use PAWS as an alternative paraphrase dataset (optional).
Evaluation: BLEU and ROUGE for question generation quality. Distinct-n for diversity. Compare
multi-task vs single-task performance

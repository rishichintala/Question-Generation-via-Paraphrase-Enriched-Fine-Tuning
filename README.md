# Text Analytics Shared Task

How to Ask Good Questions? Try to Leverage Paraphrases” (ACL 2020)
https://aclanthology.org/2020.acl-main.545.pdf


# Reimplementing: How to Ask Good Questions? Try to Leverage Paraphrases

This project reproduces and extends the ACL 2020 paper **“How to Ask Good Questions? Try to Leverage Paraphrases”**, which proposed a hybrid approach to question generation (QG) using paraphrase-aware training.

## 🧠 Project Summary

I explored how paraphrase knowledge can improve the quality of automatically generated questions. The core idea is that by exposing models to diverse question formulations, we can generate more natural, human-like questions from simple input sentences.

I implemented by following a three-model strategy:

- **Baseline Model**: A BART model fine-tuned on SQuAD to generate questions based on sentence–answer pairs.
- **Hybrid Model (Hybrid-2)**: A BART model further fine-tuned with paraphrased questions and special highlighting tokens to guide answer focus.
- **GPT-4o Baseline**: A zero-shot approach using OpenAI’s GPT-4o to generate questions via API, allowing comparison between traditional training and modern LLM prompting.

## 💡 Key Insights

- The Hybrid-2 model generated more fluent and context-aware questions than the baseline.
- GPT-4o showed strong performance out-of-the-box, producing fluent and sometimes more creative questions.
- Some overlapping outputs across all models suggested shared linguistic patterns, possibly due to the limited training data.

## ⚠️ Limitations

Due to resource constraints, I used a smaller paraphrase dataset compared to the original paper. I also did not implement the Hybrid-1 model or conduct BLEU/ROUGE evaluations. The focus was on reproducing key ideas and comparing model behavior qualitatively.

## 📌 Outcome

This project highlights how paraphrased supervision and modern LLMs complement each other in the task of question generation. It bridges classical NLP training techniques with zero-shot generation from powerful LLMs like GPT-4o.



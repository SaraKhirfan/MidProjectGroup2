# 🧠 AI-Powered Code Assistant with Tokenization &amp; Evaluation Pipeline

**HTU, Midterm Project, Generative AI Track ICT Upskilling Program — 11 Dec 2025**

Group 2: Sondos Ibrahim, Sara Khirfan, [Sadeel Alhaleeq](https://github.com/sadeelalhaleeq03) , Tasneem Alassaf

This project demonstrates an AI-powered code assistant capable of explaining, debugging, improving, and testing code using modern LLM techniques. It also includes an evaluation pipeline, tokenization experiments, and a hallucination detection framework implemented in a Google Colab notebook.

---

## 📌 Project Overview

The Code Assistant is a multi-feature system designed to support developers by providing:

- Code explanation (3 detail levels)
- Bug detection & root cause analysis
- Code optimization suggestions (performance, readability, security)
- Automatic unit test generation
- Code translation between programming languages

Additionally, the project evaluates:

- Tokenization efficiency
- Automated vs. human evaluation metrics
- Hallucination detection & mitigation
- Prompt optimization for reliability and cost reduction

---

## 🎯 Project Objectives

- Analyze tokenization and its impact on model efficiency and cost  
- Compare automated vs. human evaluations of model-generated summaries  
- Build a multi-feature code assistant optimized for clarity and control  
- Reduce hallucinations using structured prompting and context grounding  

---

## ⚙️ Features

### ✅ 1. Code Explanation
- Basic, medium, and high-detail explanations  
- Designed for readability and learning  

### ✅ 2. Debugging & Root Cause Analysis
- Identifies issues in user code  
- Suggests corrections and improvements  

### ✅ 3. Code Enhancement
- Improves structure, readability, efficiency, and security  
- Offers alternative implementations when needed  

### ✅ 4. Automatic Unit Test Generation
- Generates comprehensive tests with normal and edge cases  
- Covers 10–15 test cases per function  

### ✅ 5. Code Translation
- Converts code between languages (Python ⇆ JavaScript, C++, Java, etc.)  

### ✅ 6. Token Counting & Cost Awareness
- Tracks token usage for efficiency and budget optimization  

---

## 📊 Part B: Experiments & Evaluation

### B.1 Tokenization Experiment

Tokenizers tested on the same Python sample:

| Tokenizer        | Token Count |
|------------------|-------------|
| WordPiece        | 77          |
| SentencePiece    | 84          |
| BPE              | 97          |

**Finding:** WordPiece was **26% more efficient** for Python code — an unexpected result.

---

### B.2 Evaluation Pipeline

- Used **ROUGE-1** and **BLEU** for automated scoring  
- Designed a **human evaluation rubric** (clarity, correctness, coherence)  
- Compared **basic vs detailed prompts**  

#### 📈 Automated Results

- ROUGE-1: Basic = 0.641, Detailed = 0.615  
- BLEU: Basic = 23.35, Detailed = 29.01  

> Automated metrics failed to capture the true quality difference.

#### 👨‍🏫 Human Evaluation

- Basic Prompt: **14 / 15**  
- Detailed Prompt: **15 / 15 (Perfect)**  

---

### B.3 Optimization Reflection

- Tokenizer choice affects cost (**26% difference**)  
- Detailed prompts give better results despite similar ROUGE scores  
- Sequence length requires balancing cost vs. completeness  

---

## 🛑 Part C: Hallucination Detection & Fixing

This section evaluates how LLMs hallucinate and how to eliminate the issue.

### 🔥 1. Weak Prompt (Baseline)

- Asked about non-existent library **"FastML"**
- Model produced 1500+ words of fabricated features and comparisons  
- **Severe hallucination**

### 🧊 2. Improved Prompt

- Added rules: verify existence, avoid speculation  
- Model correctly answered:  
  > “FastML is not a recognized library.”  
- Suggested real alternatives  
- **Reduced hallucination to zero**

### 🛡️ 3. Context Grounding (RAG Simulation)

- Provided limited context  
- Forced model to answer **ONLY from context**  
- Output:  
  > “Not found in provided documentation.”

#### 🎯 Key Insight:
**Prompt structure and context grounding eliminate hallucinations far better than disclaimers.**

---

## 🏗️ System Implementation (Colab Notebook)

The Colab notebook includes:

- Modular prompt templates  
- Tokenization toolset  
- Evaluation functions (BLEU / ROUGE)  
- Model inference logic  
- Error handling  
- Hallucination detection workflows  
- Visualization for tokenization & evaluation results  

 ---
## 🏁 Conclusion

This project demonstrates a practical, optimized, and reliable code assistant powered by modern LLMs.
Through structured prompting, evaluation analysis, and hallucination detection, the system achieves:
-✅ High accuracy

-✅ High clarity

-✅ Low hallucination

-✅ Low cost

-✅ Developer-friendly behavior

It serves as a useful tool for software developers, students, and researchers working with code and AI models.



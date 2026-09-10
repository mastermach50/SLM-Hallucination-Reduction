1. [T1: TOOL-INTEGRATED VERIFICATION FOR TEST-TIME COMPUTE SCALING IN SMALL LANGUAGE MODELS](https://proceedings.iclr.cc/paper_files/paper/2026/file/776a5f2c7d6dd4b0d83145fc044e2726-Paper-Conference.pdf)

Explains how tool use can improve the accuracy of SLMs in verification tasks.
Tools such as a code interpreter to evaluate math and code so as to not hallucinate.

2. [Chain-of-Verification Reduces Hallucination in Large Language Models](https://aclanthology.org/2024.findings-acl.212.pdf)

Not exactly related to the project topic, but it demonstrates a recursive factchecking of responses to get more accurate one. In our case we will be doing a similar loop but with checks done using a RAG like lookup instead of another LLM

3. [CRITIC: LARGE LANGUAGE MODELS CAN SELF-CORRECT WITH TOOL-INTERACTIVE CRITIQUING](https://proceedings.iclr.cc/paper_files/paper/2024/file/fef126561bbf9d4467dbb8d27334b8fe-Paper-Conference.pdf)

Somewhat similar to the project, uses external tools as verifier instead of an LLM. Meets the requirement of low compute verification but does not use a DB of facts.

4. [NeMo Guardrails: A Toolkit for Controllable and Safe LLM Applications with Programmable Rails](https://arxiv.org/pdf/2310.10501)

Might be good, talks about triggering guardrails by matching LLM output with a DB of bad outputs. The matching part is relevant to us.

5. [Detecting hallucinations in large language models using semantic entropy](https://www.nature.com/articles/s41586-024-07421-0)

Can be used in a training like phase where we populate the DB for a specific task. This requires that we identify hallucinations is some other way than what we are trying to achieve.

6. [SEMANTIC ENERGY: DETECTING LLM HALLUCINATION BEYOND ENTROPY](https://arxiv.org/pdf/2508.14496) 
Improvement over paper 5, but similar idea. Can be used for generating the DB.

7. [TinyAgent: Function Calling at the Edge](https://arxiv.org/pdf/2409.00608)

A paper about using small language models as ai agents

8. 
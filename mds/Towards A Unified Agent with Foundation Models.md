# Towards A Unified Agent with Foundation Models

[Back](../README.md)

- Main question: Can we leverage the capabilities of
  Vision Language Models (VLM) to design efficient & general RL agents?
- They design a framework that puts language at the core of an RL robotic agent,
  - particularly in the context of learning from scratch.
- They show that LLMs and VLMs can tackle fundamental problems in RL such as:
    1. Efficiently exploring sparse-reward environments
    2. Re-using collected data to bootstrap the learning of new tasks
    3. Scheduling learned skills to solve novel tasks
    4. Learning from observation of expert agents.

- Section 4: A Framework for Language Centric Agents
  - **Bridging Vision and Language using VLMs**. To describe the visual inputs 
  taken from the RGB cameras in language they use CLIP
  - They use a *LM for reasoning what sub-goals are there*.
    - They use [FLAN-T5](https://huggingface.co/docs/transformers/model_doc/flan-t5) (or
    [T5](https://huggingface.co/docs/transformers/model_doc/t5)) of Google.
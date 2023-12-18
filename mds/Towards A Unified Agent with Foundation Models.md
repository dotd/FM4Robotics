# Towards A Unified Agent with Foundation Models
[Back](../README.md)

[My Paper](../pdfs/Towards%20a%20Unified%20Agent%20With%20Foundation%20Models%20-%20ICLR%202023%20-%20Di%20Palo%20et%20al.%202023.pdf)
; [Web Paper](https://arxiv.org/abs/2307.09668)



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
  - They **Grounding Instructions into Actions**
    - Takes an sub-goal embedding and the state (e.g., robot position, objects, etc.) at t, 
     and outputs an action for the robot to execute as timestep t + 1
  - **Collect & Infer Learning Paradigm** [link](https://openreview.net/forum?id=qscEfLT5VJK#:~:text=This%20position%20paper,knowledge%20inference%20respectively.)
    (the C&I separates the *data collection* and *inference processes* in RL).
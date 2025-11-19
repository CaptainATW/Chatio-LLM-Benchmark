<p align="center">
  <h1>Chatio LLM Benchmark</h1>
  <b>A benchmark for real-world helpfulness.</b><br><br>
  <a href="https://chatio.dev"><b>View the Live Leaderboard at chatio.dev</b></a>
</p>

<p align="center">
  <img src="assets/Model%20Radar.svg" alt="Model Card Visualization">
</p>

---

### Overview

Chatio is an evaluation suite designed to measure how genuinely useful Large Language Models (LLMs) are in everyday scenarios. While traditional benchmarks often focus on math olympiad problems or obscure coding challenges, Chatio evaluates the core skills required for a high-quality AI assistant: empathy, nuance, instruction following, and clear communication.

This repository contains the documentation and system card for the benchmark. To prevent test-set contamination and overfitting, the dataset itself remains closed-source.




### Why Chatio?

Legacy leaderboards often reward models for memorizing facts or solving puzzles that average users rarely encounter. However, high scores on these tests often fail to translate into a better user experience.

Chatio bridges this gap by evaluating models on **5 pillars of assistant utility**:

1.  **Emotional Support:** Evaluating tone adaptation and empathy in sensitive scenarios.
2.  **Creative Writing:** Assessing flow, originality, and stylistic adherence.
3.  **Instruction Following:** Rigorous testing of negative constraints and formatting rules.
4.  **Reading Comprehension:** Zero-hallucination information retrieval from text.
5.  **General Helpfulness:** Real-world "how-to" explanations and logic.

### Methodology

Our evaluation pipeline (v1.0) uses a mixed-method approach to balance scale with human nuance.

*   **Dataset:** ~500 synthetically generated prompts (created July 2025), manually reviewed for quality. The dataset is kept private to ensure no model has trained on the test data.
*   **Human Review:** A team of volunteers conducts blind, pairwise comparisons for subjective categories like Empathy and Helpfulness.
*   **Ensemble LLM-as-a-Judge:** For Creative Writing, we use an ensemble of **Claude 4.5 Sonnet** and **GPT-5.1** to mitigate individual model bias.
*   **Hardcoded Evaluation:** Instruction Following and Comprehension are scored via deterministic Python scripts (regex, JSON parsing).

For a deep dive into our scoring rubrics and decontamination protocols, please read the [System Card](https://chatio.dev/system-card).

### Results

We have currently evaluated the top 30 leading models.

Results are visualized on our website using a 5-point radar chart that reveals a model's specific personality—showing, for example, where a model might be excellent at coding but poor at emotional support.

<p align="center">
  <img src="assets/Model%20Card.svg" alt="Model Card Visualization">
</p>

[**Explore the Results on chatio.dev**](https://chatio.dev)

### Disclaimer

The Chatio Benchmark is intended for comparative evaluation and capability mapping. It is not a safety certification for high-stakes deployment.

------

*Created by Alex Tyh Wang.*
*© 2025 All rights reserved.*
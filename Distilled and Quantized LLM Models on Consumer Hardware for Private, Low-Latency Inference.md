Title: Distilled and Quantized LLM Models on Consumer Hardware for Private, Low-Latency Inference



------------------------------------------------------------------------------------

Reviewer Blind Comments to Author:



Aspects to consider

What is the paper about? What did you understand?

The paper evaluates distilled and quantized open-source Large Language Models (LLMs) running locally on consumer hardware, with a focus on code generation, reasoning, and mathematical problem-solving tasks. The authors benchmark several models: including DeepSeek R1 Distill Llama 70B, DeepSeek R1 Distill Qwen 32B, and QwQ-32B—across datasets such as AIME 2024, GPQA, LiveCodeBench, and MATH-500. The goal is to identify models that offer a balance between performance, inference speed, and privacy by enabling fully local deployment using tools like Ollama.

What do you think about the paper in general? Justify

The paper is well written, well structured, and addresses a timely topic: the practical viability of running open LLMs locally for privacy-sensitive applications. The motivation is clear, the benchmark selection is appropriate, and the results are presented in a straightforward way. The discussion successfully connects performance findings with practical deployment considerations. However, the methodology lacks detail in several areas (e.g., exact hardware specs, batch sizes, prompt formatting), the statistical robustness of the evaluation is not addressed, and the radar plots could include numerical scales for easier interpretation.

List. What would you change/correct? Justify

1. Add missing experimental details
The evaluation lacks transparency regarding prompt templates, hardware configuration specifics (beyond “high-end desktop”), quantization settings, and inference parameters. These details are essential for reproducibility.

2. Clarify the role of quantization in the experiments
Although quantization is named in the title and abstract, the experimental section does not clearly state which models were quantized, the methods used, or how precision levels affected performance.

3. Discuss variance and reliability of results
Benchmarks such as LiveCodeBench typically require multiple sampling runs (pass@k) or temperature variation. The paper reports only single values without uncertainty ranges.

4. Improve the comparative discussion
The paper references Matotek’s work but could benefit from a more explicit comparison: Did the tested 32B distilled models surpass the 7B–9B models in all tasks? Where do they still fail?

5. Enhance the radar plots
Current figures lack axis labels, scale values, and legends are visually separated from the charts. This makes interpretation harder and reduces the impact of the visualization.


List. Minor changes (spelling/math correction/reference errors)

1. Some references are missing authors (“and others.” repeated excessively).

2. The citation “[cite:1]” is a placeholder and does not resolve to any reference.

3. Several section headers do not follow consistent formatting.

4. Table 1 could be improved for better readability.


Conclusion. Justify your review in one paragraph
The paper makes a relevant and timely contribution by benchmarking locally deployable distilled LLMs on consumer hardware for privacy-sensitive applications. The results demonstrate that mid-sized distilled models (e.g., QwQ-32B) can approach the performance of the larger 70B models while remaining feasible to run locally. Although the motivation and discussion are strong, the work would benefit from adding methodological details, clarifying quantization settings, expanding the analysis of limitations, and improving result visualizations. Despite these issues, the paper provides valuable insights and is suitable for publication after minor revisions.


------------------------------------------------------------------------------------


Reviewer Confidential Comments to Editor:


Judgement:


1) Type of contribution:

[ ] Commentary or review
[X] New proposal of methodology
[ ] Major improvement of a known method
[ ] Minor improvement of a known method
[ ] New application area
[ ] Major development of a known application
[ ] Minor development of a known application
[ ] None of the above, but acceptable
[ ] None of the above, unacceptable


2) Potential impact:

[ ] High reference value for wide readership
[X] High reference value for limited readership
[ ] Marginal reference value for wide readership
[ ] Marginal reference value for limited readership
[ ] No reference value


3) Overall quality:

[ ] Excellent
[X] Good
[ ] Average
[ ] Fair
[ ] Poor


4) Originality:

[ ] Excellent
[X] Good
[ ] Average
[ ] Fair
[ ] Poor
[ ] Cannot determine


5) Technical correctness:

[ ] Correct
[X] Probably correct, convincing
[ ] Probably incorrect or unconvincing
[ ] Incorrect
[ ] Cannot determine


6) Experimental evaluation:

[ ] No such need
[ ] Thorough and convincing
[X] Limited but convincing
[ ] Unconvincing
[ ] Cannot determine


7) Clarity of presentation:

[ ] Excellent
[X] Good
[ ] Average
[ ] Fair
[ ] Poor


8) Adequacy of references to literature:

[ ] Adequate
[X] Mostly adequate, with some omissions
[ ] Inadequate references


9) Linguistic quality:

[ ] Excellent
[X] Good
[ ] Average
[ ] Fair
[ ] Poor
[ ] Cannot judge


10) Quality of illustrations:

[ ] Excellent
[ ] Good
[X] Average
[ ] Fair
[ ] Poor



Recommendations as to publication (please mark one category):

[ ] Excellent
[X] Accept
[ ] Marginal Accept
[ ] Marginal Reject
[ ] Reject





Confidential (NOT to be forwarded to the authors):



Confidence of review:

[ ] Highly confident
[X] Confident
[ ] Somewhat confident
[ ] May need additional review in some areas (explain)



Additional remarks for editors only:
Comments that are not sent to the authors but that help the editor to decide. IMPORTANT!
The paper addresses an increasingly relevant problem (local LLM deployment for privacy), and the benchmark selection matches the intended use case well. The conclusions are reasonable given the results. Some methodological improvements would strengthen the work, but the core contribution is solid and publication-ready after minor revisions.

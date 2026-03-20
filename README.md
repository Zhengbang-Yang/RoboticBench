# RoboticBench

## Prompt used in our paper

### Data Extraction and Standardization
Converting PDF files to Latex document: PDF2Latex.txt

Data Standardization: ExtractLatex.txt

Data Standardization agent extracts (i) the formal problem definition(s) $\mathcal{T}$, (ii) the algorithm definition $\mathcal{A}$, (iii) the ground-truth approximation ratio $\alpha$ and its corresponding proof, and (iv) the key lemmas invoked by the ground truth proof $\mathcal{C}$.

### User input to generate answer
User input contains user instruction and task information from standardized data.

Basic user instruction without CoT instruction: basic_instruction.txt

User instruction with CoT template: reasoning_instruction.txt

For the following part shared by both type of instruction, the {x} refers to how many parts contained task information. The parts contained in task information depends on the experiment setting.
```
The task information contains {x} parts, all written in LaTeX format:
1. **Problem Definition**: Describes the path planning problem you are analyzing.
2. **Preliminaries**: Provides in-context knowledge, definitions, and background information.
3. **Algorithm**: The algorithm for which you need to derive the approximation ratio.
4. **Approximation Ratio**: The approximation ratio concluded from the ground truth proof.
```

### Evaluation pipeline
Prompt for evaluation: evaluation.txt

Prompt for error analysis: evaluation.txt

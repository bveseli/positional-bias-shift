# Positional Biases Shift as Inputs Approach Context Window Limits

Large Language Models (LLMs) often struggle to use information across long inputs. Prior work has identified positional biases like the Lost in the Middle (LiM) effect—better performance when key information appears at the beginning (primacy) or end (recency) rather than in the middle—but long-context studies have not consistently replicated these effects. We address this by analyzing input length relative to each model’s context window and find that LiM is strongest when inputs occupy up to 50% of that window. Beyond that point, primacy weakens while recency remains relatively stable, effectively eliminating LiM and revealing a distance-based bias where performance is better when relevant information is closer to the end. Our results also suggest that successful retrieval is a prerequisite for reasoning, and that positional biases in reasoning are largely inherited from retrieval, with implications for long-context tasks, benchmark design, and evaluation.


<p align="center">
  <img src="figures/teaser_gemma_retrieval_final-2-1.png" width="500" alt="positional biases vs. relative length">
</p>

- **Key findings**
  - Analysis of positional biases using **relative input length** (proportion of a model’s context window) rather than absolute lengths across models.
  - Positional biases are consistent across models when analyzed relative to a model's context window size. 
  - LiM is strongest in input lengths up to 50% of a models context window size.
  - With growing input size, primacy bias increasingly collapses, while the recency bias remains stable. This results in a more distance-based bias, i.e. accuracy higher when evidence is nearer the end.
  - Positional biases in reasoning, specifically the LiM effect, appear to be largely inherited from retrieval.

## Citation
@inproceedings{veseli2025positional,
  title={Positional Biases Shift as Inputs Approach Context Window Limits},
  author={Veseli, Blerta and Chibane, Julian and Toneva, Mariya and Koller, Alexander},
  booktitle={Proceedings of the Conference on Language Modeling (COLM)},
  year={2025}
}

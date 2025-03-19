# Automatic Prompt Optimization

OPRO stands for Optimization by PROmpting (arXiv:2309.03409 [cs.LG]). It is a methodology which uses LLMs as optimizers in an iterative process.

How OPRO works for prompt optimization:
1.	Meta-Prompt Construction: Create a prompt containing:
-	Previously tested prompts with their performance scores
-	Task description and evaluation criteria
-	Example inputs and outputs for the classification task
2.	Solution Generation: The LLM generates multiple candidate prompts
3.	Evaluation: Each prompt is tested on a validation set to measure performance
4.	Feedback Loop: The best-performing prompts and their scores are incorporated into the meta-prompt for the next iteration
5.	Iteration: Steps 2-4 are repeated, with each cycle potentially producing better prompts

The provided notebook walks through a simple implementation which leverages Amazon Bedrock hosted models.
The implementation is applied to a text classification task, with ground truth data provided in a CSV file.

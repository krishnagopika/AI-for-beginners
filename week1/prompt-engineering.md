# Prompt Engineering


### Prompt and Completion

A prompt is the input text you provide to a model, and the completion is the model's output. The goal of prompt engineering is to design prompts that guide the model to produce the desired output.


#### Prompt Structure

```
`system message`: [System-level instructions to set context or behavior for the model]
`context`: [Optional; provides additional relevant background or constraints for more accurate responses]
`user input`: [The user's query or task; what the model is supposed to respond to]
`output_format`: [Optional; specifies the desired format of the output, such as list, paragraph, or specific style]
```

**Using Delimiters**

- Use clear delimiters to break down different parts of the prompt. These help ensure that each section is clearly understood by the model.
- Code block delimiter (```), triple quotes ("""), angle brackets (<>) or tags (<tag></tag>) can be used for different sections.

**Parameters**

- **n (number of choices)**: Specifies how many distinct response options the model should generate.
Example: n=3 generates 3 outputs.

- **max_tokens**: Limits the number of tokens the model can use in its response.
Example: max_tokens=150 restricts the output to 150 tokens.

- **stop**: Defines the stopping point for text generation.
Example: "stop": ["\n"] stops at a newline.

- **temperature**: Controls the randomness of the model’s responses.
Example: temperature=0.7 allows for creative responses.

- **top_p**: Uses nucleus sampling, considering tokens with cumulative probability greater than top_p.

- **top_k**: Limits the number of candidate tokens the model considers for the next word.


### Prompt Engineering Techniques

#### zero-shot and few-shot

**Zero-shot**: Model generates responses without prior examples.

**Few-shot**: Provides a few examples to guide the model’s responses.

#### chain of thought

A structured approach where the model is prompted to break down the reasoning process step-by-step.

#### ReAct

Combines reasoning and actions where the model alternates between logical reasoning and taking actions like querying external data.

#### usecase

Sentiment Analysis, Keyword Extraction and Summarization of product reviews

```

```

#### hallucinations

- LLM generating factually incorrect or nonsensical information.
- misalignmnet of text generation objectve and user's objective of desired responses.

[A Survey on Hallucination in Large Language Models](https://arxiv.org/pdf/2311.05232.pdf)

**NLP hallucination types:**

- intrinsic: input info is manupulated
- extrinsic: info not in input is added

**Sources of hallucinations**
- Imprefect representation learning
- Erroneous decoding
- Exposure bias
- parametric knowledge bias

**LLM Hallucinations Types:**

1. Factuality Hallucination
    - Factual Inconsistency
    - Factual Fabrication
2. Faithfulness Hallucination
   - Instruction Inconsistency
   - Context Inconsistency
   - logical Inconsistency

#### security considerations

- PPI (Personally Identifiable Information): Sensitive data, such as names, addresses, or contact details, that can be used to identify individuals.

- Data Privacy: Ensuring that user data used in LLM interactions is not stored or exposed inappropriately.

- Jailbreaking: Bypassing or disabling the model's built-in safeguards to generate unintended or harmful outputs.

- Prompt Injection: Manipulating the input prompt to trick the model into producing unwanted or harmful responses.

- Bias and Fairness: Safeguarding against biased responses or content that may perpetuate harmful stereotypes.

- Content Moderation: Implementing checks to prevent harmful, illegal, or unethical content generation.

references:


1. [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
2. Sahar Abdelnabi et al. Are you still on track!? Catching LLM Task Drift with Activations [https://arxiv.org/abs/2406.00799](https://arxiv.org/abs/2406.00799)
3. Azure AI announces Prompt Shields for Jailbreak and Indirect prompt injection attacks
4. Keegan Hines et al. Defending Against Indirect Prompt Injection Attacks With Spotlighting
5. Eric Wallace et al. The Instruction Hierarchy: Training LLMs to Prioritize Privileged Instructions

 


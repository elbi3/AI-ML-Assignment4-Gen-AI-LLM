# Generative AI with Pre-trained LLMs: Book Review Prompt

Author: El Brewster

Model Used: `google/flan-t5-base` (T5-based sequence-to-sequence model)

Task: Generate a book review for a sci-fi novel where two spaceships go from enemies to lovers, targeting approximately 136 words in length.

## Overview

This project demonstrates text generation using a pre-trained open-source LLM (`google/flan-t5-base`) in PyTorch. The goal was to generate coherent book reviews while experimenting with different generation parameters to understand their effect on output quality, length, and creativity.

Three main parameters were tested:
- Temperature: Controls randomness/creativity in output.
- Max New Tokens: Controls the length of the generated text.
- Top-P (nucleus sampling): Controls diversity of word selection at each step.

A final run was performed using selected parameters based on these experiments.


## Parameter Experiments

| Parameter Type | Parameter Value | Output Snippet | Brief Observation |
|----------------|----------------|----------------|-----------------|
| **Temperature** | 0.2 | "This is a great sci-fi novel, and a great sci-fi movie. The plot is a bit stale, but the characters are well developed and the story..." | Safe, repetitive, very predictable style. |
|                | 0.7 | "This sci-fi thriller features two surviving aliens and their love interest, the narrator, who reveals that they are lovers..." | Balanced creativity, more narrative flow, still coherent. |
|                | 1.0 | "If you're a lover of sci-fi novels, or want to see a sci-fi movie of the day, this is the one..." | Highly creative but occasionally unfocused; more surprising phrasing. |
| **Max New Tokens** | 100 | "This is one of the best sci-fi novels I've read. It's a lot of fun and it's also one of the best sci-fi novels I've read in a while..." | Short output, concise, some repetition. |
|                  | 150 | "Despite the crassness of the story and the lack of a plot, this is a surprisingly good sci-fi thriller..." | Moderate length, coherent story. |
|                  | 200 | "I love this series and I thought it was an excellent sci-fi adventure. I was hoping to see a sequel, but this one is not..." | Longer output, more detail and narrative development. |
| **Top-P** | 0.5 | "This is a great sci-fi thriller. The plot is a bit stale, but the characters are well developed and the story is well told..." | Conservative word selection, safe, repetitive. |
|           | 0.7 | "This is a very good sci-fi novel. It isn't a perfect movie, but it is very good..." | Balanced, slightly more variety and flow. |
|           | 0.9 | "This is a very entertaining sci-fi novel. There is nothing wrong with that. The plot is very clever and witty..." | High diversity, richer vocabulary, creative phrasing. |

## Final Run

Chosen Parameters: `{'temperature': 0.9, 'top_p': 0.9, 'max_new_tokens': 200}`

### Generated Book Review (≈136 words):

"A story of two savage aliens who try to avenge each other and then find each other. They start the journey toward a new world, and ultimately the end. This is a classic sci-fi thriller. A series of eerie, flashy, atmospheric scenes are the highlight of the story, with the characters being hailed as the stars of this masterpiece. The pacing is surprisingly fast and the characters portrayed as heroes are also pretty good. The plot is well written and the characters are well developed. The world is a place of terror. The aliens don't look like any aliens. The aliens are just like all humans, and the humans need to live. This book gives us a very unique story with a unique and complex way of life. A must read for sci-fi fans."

Analysis:
- Word count: 134
- Token count: 182

Notes
- This project demonstrates controlled experimentation with LLM parameters.
- Observations show how temperature, max tokens, and top-p influence the creativity,    length, and coherence of generated text.

The final selection balances creativity with coherence for a readable, engaging sci-fi book review.

## 🧰 Tools and Libraries
- Python 3.11.14
- transformers 4.57.1
- torch 2.9.1
- sentencepiece 0.2.1
- pandas 2.3.3
- jupytrlab 4.4.7
- ipywidgets 8.1.7
- ipykernel 6.31.0

### Further Reading
[Hugging Face Transformers Documentation on T5](https://huggingface.co/docs/transformers/v4.27.0/en/model_doc/t5)
[Tokenizer](https://huggingface.co/docs/transformers/main_classes/tokenizer)

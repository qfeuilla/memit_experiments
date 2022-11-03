# Improvments

- All in classes
- Using Easy Transformer lib for hooks (will allow to use more transformers, and bigger LLMs)
- Code fully commented
- Code almost fully typed (except return type)

# Notes of some blocking points i had

## For causal tracing

- The prompt is repeated n times, and the first element of the batch is never corrupted.

- The corruption is happening on the embedding

- Everything is corrupted and the layer are restore independently one by one by broadcasting the first element of the batch to the other one

- the only thing that is noised out is the subject, not all the text

# Random Ideas

- Tool to edit a list of concept to/toward a specific embedding (instead of another object as a str). Could be nice for gender debiasing for example

- hashmap of patches to reuse the ones already created

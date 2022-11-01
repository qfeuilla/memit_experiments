# Improvments

- All in classes
- Using Easy Transformer lib for hooks (will allow to use more transformers, and bigger LLMs)
- Code fully commented

# Notes of some blocking points i had

## For causal tracing

- The prompt is repeated n times, and the first element of the batch is never corrupted.

- The corruption is happening on the embedding

- Everything is corrupted and the layer are restore independently one by one by broadcasting the first element of the batch to the other one

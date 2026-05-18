# Runpod serverless runner for ollama

## How to use

If you are using this fork, push to `master` first and let GitHub Actions build your image to:

`ghcr.io/<your-github-username>/runpod-worker-ollama:latest`

Then start a Runpod serverless worker with that container image. Set `OLLAMA_MODEL_NAME` to a model from ollama.com or to an Ollama-compatible Hugging Face path such as `hf.co/HauhauCS/Gemma-4-E4B-Uncensored-HauhauCS-Aggressive:Gemma-4-E4B-Uncensored-HauhauCS-Aggressive-Q4_K_M.gguf` to automatically download the model.
A mounted volume will be automatically used.

[![RunPod](https://api.runpod.io/badge/SvenBrnn/runpod-worker-ollama)](https://www.runpod.io/console/hub/SvenBrnn/runpod-worker-ollama)

## Environment variables

| Variable Name       | Description                              | Default Value       |
|---------------------|------------------------------------------|---------------------|
| `OLLAMA_MODEL_NAME` | The name of the model to download        | NULL                |

## Test requests for runpod.io console

See the [test_inputs](./test_inputs) directory for example test requests. 


## Streaming

Streaming for openai requests are fully working.

## Preload model into the docker image

See the [embed_model](./embed_model/) directory for instructions.

## Licence

This project is licensed under the Creative Commons Attribution 4.0 International License. You are free to use, share, and adapt the material for any purpose, even commercially, under the following terms:

- **Attribution**: You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- **Reference**: You must reference the original repository at [https://github.com/svenbrnn/runpod-worker-ollama](https://github.com/svenbrnn/runpod-worker-ollama).

For more details, see the [license](https://creativecommons.org/licenses/by/4.0/).

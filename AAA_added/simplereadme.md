Run this command from repo folder to run with GPU acceleration:
```
docker run --rm -it \
  --gpus all \
  -p 127.0.0.1:9931:9931 \
  -v "$HOME/1337fede/llama.cpp/AAA_added/models/gemma-4-e4b:/root/.cache/huggingface" \
  ghcr.io/ggml-org/llama.cpp:server-cuda \
  -hf ggml-org/gemma-4-e4b-it-GGUF:Q4_0 \
  --host 0.0.0.0 \
  --port 9931 \
  --n-gpu-layers 99
```
wait until you see:
```
model loaded
listening on http://0.0.0.0:9931
```
and reach that website to chat with llama
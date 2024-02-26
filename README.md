# LLM Configs
A collection of my local LLM configs for efficient testing of models. I found LLM configuration to be quite a convoluted process and some were simply too large for an individual researcher (even with a 4070ti) to attempt to use efficiently. API calls were convenient, but limited in terms of research capabilities and certain models charged for API usage. I've tested the direct download from Meta as well but that proved to be difficult to fine tune and work with and was too slow. Hugging Face provides excellent support for downloading models as well as trying different quantization configurations on them. It's recommanded to use linux (wsl on windows) to run LLMs because many of the required packages are currently only supported on linux

Current Models Configured:
- Code LLama Instruct (7B)
- Gemma (7B)

If a login error is thrown, get a key from huggingface's website and save it to huggingface_token.txt.

To scan current models in the huggingface cached library:
```
huggingface-cli scan-cache
```

To delete models from the huggingface cached library:
```
huggingface-cli delete-cache
```

To install bitsandbytes for quantization:
```
pip install transformers accelerate bitsandbytes
```

Note to self: Use /usr/bin/python3.10 for runtime kernel

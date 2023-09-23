# Light Fairseq

This repo contains Hugging Face transformers-style conversions of some Fairseq model checkpoints

## 1. Checkpoints

GPT-like SMoE and dense model checkpoints from [arXiv:2112.10684](https://arxiv.org/abs/2112.10684)

- [x] en_dense_lm_125m
- [x] en_moe_lm_15b



## 2. Example usage:

```python
from lightfs.models import FSGPTForCausalLM

# load `en_dense_lm_125m` from 🤗Huggingface model hub
model = FSGPTForCausalLM.from_pretrained("Phando/fairseq-dense-125m")
```

```python
import torch

from lightfs.models import FSGPTMoEForCausalLM

# load `en_moe_lm_15b` from 🤗Huggingface model hub, with 🤗Accelerate MP and bf16
model = FSGPTMoEForCausalLM.from_pretrained("Phando/fairseq-moe-15b",
                                            device_map="auto", torch_dtype=torch.bfloat16)
```

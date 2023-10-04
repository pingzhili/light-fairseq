# Light Fairseq

Re-implement Fairseq models in the Huggingface-style

## 1. Checkpoints

### 1.1. GPT Dense&SMoE in [arXiv:2112.10684](https://arxiv.org/abs/2112.10684)

- [x] en_dense_lm_125m
- [x] en_moe_lm_15b



## 2. Example usage:

```python
from lightfs import FSGPTForCausalLM

# load `en_dense_lm_125m` from 🤗Huggingface model hub
model = FSGPTForCausalLM.from_pretrained("Phando/fairseq-dense-125m")
```

```python
from lightfs import FSGPTMoEForCausalLM

# load `en_moe_lm_15b` from 🤗Huggingface model hub, with 🤗Accelerate MP and bf16
model = FSGPTMoEForCausalLM.from_pretrained("Phando/fairseq-moe-15b",
                                            device_map="auto", torch_dtype=torch.bfloat16)
```

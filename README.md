# light-fairseq

Re-implement Fairseq models in the Huggingface-style

## 1. Checkpoints

### 1.1. GPT From arXiv:2112.10684

- [x] en_dense_lm_125m
- [ ] moe_15b

Example usage:

```python
from lightfs.models import FSGPTForCausalLM

model = FSGPTForCausalLM.from_pretrained("Phando/fairseq-dense-125m")
```
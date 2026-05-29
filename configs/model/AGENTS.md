# configs/model

Model configuration lives here.

```
configs/model/
├── README.md              # Human guide for model config requirements
├── Qwen/                  # Qwen-family HuggingFace-compatible configs
├── meta-llama/            # Llama-family HuggingFace-compatible configs
├── mistralai/             # Mixtral-family HuggingFace-compatible configs
└── microsoft/             # Phi-family HuggingFace-compatible configs
```

Each JSON file is the simulator and profiler's shape source of truth. Keep
paths aligned with HuggingFace ids (`<org>/<model>.json`). Derived profiling
configs may reduce `num_hidden_layers` or `layer_types`, but must keep the
canonical model id in the filename so profile output still maps back to the
real model.

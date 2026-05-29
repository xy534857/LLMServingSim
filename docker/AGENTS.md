# AGENTS.md

Container build recipes live here.

```
docker/
└── h100-dev/
    └── Dockerfile   # vLLM-based H100 development image for profiler and bench work
```

Keep images reproducible: install system and Python dependencies here, but do not copy local source trees, kubeconfigs, GitHub tokens, Hugging Face tokens, SSH keys, or benchmark outputs into images. Code is mounted, cloned, or streamed into pods at runtime.

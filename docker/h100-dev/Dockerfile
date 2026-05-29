FROM vllm/vllm-openai:v0.19.0

ENV DEBIAN_FRONTEND=noninteractive

# LLMServingSim needs the ASTRA-Sim build toolchain plus Python data packages.
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        ca-certificates \
        cmake \
        git \
        graphviz \
        protobuf-compiler \
    && rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install --no-cache-dir \
        msgspec \
        networkx \
        numpy \
        pandas \
        pydot \
        pyinstrument \
        "protobuf==6.*" \
        pyyaml \
        rich \
    && ln -sf "$(command -v python3)" /usr/local/bin/python

WORKDIR /workspace
CMD ["sleep", "infinity"]

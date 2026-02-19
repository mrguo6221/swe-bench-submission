# Qwen3-Coder-Next + mini-swe-agent

## SWE-bench Verified Results

- **Resolved**: 342 / 500 (**68.4%**)
- **Pass@1**: Single attempt per instance

## System Overview

### Model
- **Model**: Qwen3-Coder-Next (80B parameters)
- **Quantization**: FP8 (via vLLM)
- **Inference**: 2x NVIDIA RTX 4090 48GB GPUs with tensor parallelism
- **Context**: 256,000 tokens
- **Temperature**: 1.0

### Agent Framework
- **Framework**: mini-swe-agent (bash-only)
- **Tools**: Bash shell only (no specialized code editing tools)
- **Max steps**: 250 per task instance
- **Strategy**: Direct problem-solving without chain-of-thought prompting (NoCoT)

### Infrastructure
- **Deployment**: Self-hosted on-premise cluster
- **Load balancing**: 4-group vLLM instances with round-robin
- **Evaluation**: SWE-bench docker-based harness with 46 parallel workers

## Submission

Full predictions, trajectories, and metadata are available in the [SWE-bench experiments repository](https://github.com/SWE-bench/experiments).

## Authors

- Junqing Duan, Beijing Jiaotong University (段俊卿, 北京交通大学)
- Liang Sun, Beijing Jiaotong University (孙亮, 北京交通大学)
- Jinan Jigang Digital Innovation Technology Co., Ltd. (济南济钢数创科技有限公司)

**Contact**: 23126422@bjtu.edu.cn

Joint work between Beijing Jiaotong University and Jigang Digital Innovation, focused on evaluating open-source large language models for automated software engineering tasks.

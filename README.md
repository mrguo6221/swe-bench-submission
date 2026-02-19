# Qwen3-Coder-Next + mini-swe-agent

## SWE-bench Verified Results

- **Resolved**: 342 / 500 (**68.4%**)
- **Pass@1**: Single attempt per instance

## System Overview

### Model
- **Model**: Qwen3-Coder-Next (80B parameters)
- **Quantization**: FP8 (via vLLM)
- **Inference**: 4x NVIDIA A800 80GB GPUs with tensor parallelism
- **Throughput**: ~120 tokens/s
- **Context**: 32,768 tokens
- **Temperature**: 1.0

### Agent Framework
- **Framework**: mini-swe-agent (bash-only)
- **Tools**: Bash shell only (no specialized code editing tools)
- **Max steps**: 250 per task instance
- **Strategy**: Direct problem-solving without chain-of-thought prompting (NoCoT)

### Infrastructure
- **Deployment**: Self-hosted on-premise cluster
- **Load balancing**: 4-container vLLM instances with round-robin
- **Evaluation**: SWE-bench docker-based harness with 46 parallel workers

## Submission

Full predictions, trajectories, and metadata are available in the [SWE-bench experiments repository](https://github.com/SWE-bench/experiments).

## Organization

**济南济钢数创科技有限公司** (Jinan Jigang Digital Innovation Technology Co., Ltd.)

A subsidiary of Jigang Group, focused on digital innovation and AI infrastructure deployment.

<div align="center">

**Making inference faster, and checking that it stays correct.**

NVIDIA Blackwell / DGX Spark · Ascend · Open Source

[Contributions](#-open-source--pull-requests) · [Project](#-building) · [All pull requests](https://github.com/pulls?q=is%3Apr+author%3Azhachar14h-cell)

</div>

<br>

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>⚡ Current Focus</h3>
      <p><strong>LLM inference</strong><br>Serving paths, backend selection and deployment.</p>
      <p><strong>GPU / NPU kernels</strong><br>MoE, low-precision compute and linear attention.</p>
      <p><strong>Numerical correctness</strong><br>Reference checks, regression tests and reproducible benchmarks.</p>
    </td>
    <td width="50%" valign="top">
      <h3>🌱 Open Source</h3>
      <p><strong><a href="https://github.com/QwenLM/FlashQLA/pull/33">FlashQLA contributor</a></strong><br>Merged support for NVIDIA GB10 / SM121 using the SM120 kernels.</p>
      <p><strong>Further pull requests</strong><br>FlashInfer · SGLang · Atlas · DeepInfer · Strata</p>
      <p>Inference optimizations, hardware compatibility and validation.</p>
    </td>
  </tr>
</table>

### 🛠 Working With

`Python` · `Rust` · `CUDA` · `TileLang` · `PyTorch` · `Ascend / CANN`

### 🔎 Open Source & Pull Requests

| Project | Selected work | Links |
| :--- | :--- | :--- |
| **[FlashQLA](https://github.com/QwenLM/FlashQLA)** | NVIDIA GB10 / SM121 support | [#33 · Merged](https://github.com/QwenLM/FlashQLA/pull/33) |
| **[FlashInfer](https://github.com/flashinfer-ai/flashinfer)** | Build fingerprints to invalidate stale NVCC JIT caches | [#4490](https://github.com/flashinfer-ai/flashinfer/pull/4490) |
| **[SGLang](https://github.com/sgl-project/sglang)** | FlashInfer CUTLASS backend selection for mixed MoE on SM120 | [#35617](https://github.com/sgl-project/sglang/pull/35617) |
| **[Atlas](https://github.com/Avarok-Cybersecurity/atlas)** | NVFP4 MoE prefill: compact row lists and K32 down projection | [#584](https://github.com/Avarok-Cybersecurity/atlas/pull/584) |
| **[DeepInfer](https://github.com/deepseek-ai/DeepInfer)** | Ascend NUMA discovery and ViT variable-length attention tests | [#129](https://github.com/deepseek-ai/DeepInfer/pull/129) · [#139](https://github.com/deepseek-ai/DeepInfer/pull/139) |
| **[Strata](https://github.com/Niko1221/Strata)** | Ascend MoE validation and compensated S2 rounding | [#3582](https://github.com/Niko1221/Strata/pull/3582) |

<sub>Links point to upstream pull requests, where review status, measurements and validation scope are recorded.</sub>

### 🚀 Building

**[Uniform DGX Spark — Claude Code Plugin](https://github.com/zhachar14h-cell/uniform-dgxspark-claude-plugin)**

A Claude Code client for a running Uniform DGX Spark platform: deploy models, follow progress, inspect logs and monitor machine metrics from a coding session.

`TypeScript` · `Claude Code` · `DGX Spark` · `Model Deployment`

---

<div align="center">
  <sub>From kernel behavior to serving behavior — measure, verify, improve.</sub>
</div>

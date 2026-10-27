<div align="center">

**Making inference faster, and checking that it stays correct.**

NVIDIA Blackwell / DGX Spark · Ascend · Open Source

[Contributions](#-open-source--pull-requests) · [Project](#-building) · [All pull requests](https://github.com/pulls?q=is%3Apr+author%3Azhachar14h-cell)

</div>

<br>

<table>
  <tr>
    <td width="50%" valign="top">
      <p><a name="-current-focus"></a><strong>⚡ Current Focus</strong>&nbsp; <a href="#-current-focus" title="Link to Current Focus">🔗</a></p>
      <p><strong>LLM inference</strong><br>Serving paths, backend selection and deployment.</p>
      <p><strong>GPU / NPU kernels</strong><br>MoE, low-precision compute and linear attention.</p>
      <p><strong>Numerical correctness</strong><br>Reference checks, regression tests and reproducible benchmarks.</p>
    </td>
    <td width="50%" valign="top">
      <p><a name="-open-source"></a><strong>🌱 Open Source</strong>&nbsp; <a href="#-open-source" title="Link to Open Source">🔗</a></p>
      <p><strong><a href="https://github.com/QwenLM/FlashQLA/pull/33">FlashQLA contributor</a></strong><br>Merged support for NVIDIA GB10 / SM121 using the SM120 kernels.</p>
      <p><strong>Further pull requests</strong><br>FlashInfer · SGLang · Atlas · DeepInfer · Strata</p>
      <p>Inference optimizations, hardware compatibility and validation.</p>
    </td>
  </tr>
</table>

### 🛠 Working With

`Python` · `Rust` · `CUDA` · `TileLang` · `PyTorch` · `Ascend / CANN`

### 🔎 Open Source & Pull Requests

| Project | Selected work | Pull requests |
| :--- | :--- | :--- |
| **[FlashQLA](https://github.com/QwenLM/FlashQLA)** | SM120 / SM121 Gated Delta Rule kernels and CP | [PR #21](https://github.com/QwenLM/FlashQLA/pull/21) (cooperate merged)<br>[PR #34](https://github.com/QwenLM/FlashQLA/pull/34) (cooperate merged)<br>[PR #33](https://github.com/QwenLM/FlashQLA/pull/33) (merged) |
| **[Atlas](https://github.com/Avarok-Cybersecurity/atlas)** | Completions API, Gated DeltaNet and MoE prefill | [PR #582](https://github.com/Avarok-Cybersecurity/atlas/pull/582) (merged via [#1203](https://github.com/Avarok-Cybersecurity/atlas/pull/1203))<br>[PR #583](https://github.com/Avarok-Cybersecurity/atlas/pull/583)<br>[PR #584](https://github.com/Avarok-Cybersecurity/atlas/pull/584)  |
| **[SGLang](https://github.com/sgl-project/sglang)** | SM120 / SM121 NVFP4 MoE and backend selection | [#35422](https://github.com/sgl-project/sglang/pull/35422) · [#35617](https://github.com/sgl-project/sglang/pull/35617) |
| **[DeepInfer](https://github.com/deepseek-ai/DeepInfer)** | Evaluation fixes and Ascend NPU validation | [#31](https://github.com/deepseek-ai/DeepInfer/pull/31) · [#33](https://github.com/deepseek-ai/DeepInfer/pull/33) · [#129](https://github.com/deepseek-ai/DeepInfer/pull/129) · [#139](https://github.com/deepseek-ai/DeepInfer/pull/139) |
| **[FlashInfer](https://github.com/flashinfer-ai/flashinfer)** | NVCC JIT cache invalidation | [#4490](https://github.com/flashinfer-ai/flashinfer/pull/4490) |
| **[Strata](https://github.com/Niko1221/Strata)** | Ascend MoE numerical validation | [#3582](https://github.com/Niko1221/Strata/pull/3582) |

### 🚀 Building

**[Uniform DGX Spark — Claude Code Plugin](https://github.com/zhachar14h-cell/uniform-dgxspark-claude-plugin)**

A Claude Code client for a running Uniform DGX Spark platform: deploy models, follow progress, inspect logs and monitor machine metrics from a coding session.

`TypeScript` · `Claude Code` · `DGX Spark` · `Model Deployment`

---

<div align="center">
  <sub>From kernel behavior to serving behavior — measure, verify, improve.</sub>
</div>

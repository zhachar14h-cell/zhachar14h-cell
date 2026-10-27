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

#### [FlashQLA](https://github.com/QwenLM/FlashQLA) · Qwen's linear attention kernels · 700+ ⭐

[PR #21](https://github.com/QwenLM/FlashQLA/pull/21) · [PR #34](https://github.com/QwenLM/FlashQLA/pull/34) — merged collaborations  
[PR #33](https://github.com/QwenLM/FlashQLA/pull/33) — merged

- **SM120 forward and backward:** contributed in collaboration to Gated Delta Rule forward inference, fused backward and intra-card CP, adapting kernels to the approximately 100 KB shared-memory limit.
- **SM121 / DGX Spark:** routed GB10 to the SM120 kernels. For a T=8192 variable-length workload, kernel latency went from **7.19 ms to 1.62 ms (4.45×)**. [#33](https://github.com/QwenLM/FlashQLA/pull/33)

#### [Atlas](https://github.com/Avarok-Cybersecurity/atlas) · Inference engine and optimization · 700+ ⭐

[PR #582](https://github.com/Avarok-Cybersecurity/atlas/pull/582) · [PR #583](https://github.com/Avarok-Cybersecurity/atlas/pull/583) · [PR #584](https://github.com/Avarok-Cybersecurity/atlas/pull/584)

- **Completions API:** addressed ignored `min_tokens` in blocking, streaming and speculative decoding paths. The original #582 was closed; its commits landed via [#1203](https://github.com/Avarok-Cybersecurity/atlas/pull/1203).
- **SSM / Gated DeltaNet:** proposed an opt-in native FlashQLA prefill path. A reviewer measured median cold TTFT falling from **944.81 ms to 710.39 ms (~25%)** on GB10 with Qwen3.6-35B-A3B-NVFP4. [Measurement](https://github.com/Avarok-Cybersecurity/atlas/pull/583#issuecomment-5338149513)
- **MoE prefill:** proposed compact expert row lists and K32 down projection; the reported GB10 stage-1 TTFT fell from **601.62 ms to 467.73 ms (~22%)**. [#584](https://github.com/Avarok-Cybersecurity/atlas/pull/584)

<sub>As of 2026-10-27, #583 is closed without merging and #584 is open. Measurements apply to the configurations and workloads described in the linked reports.</sub>

#### [SGLang](https://github.com/sgl-project/sglang) · SM120 / SM121 inference · 37k+ ⭐

[PR #35422](https://github.com/sgl-project/sglang/pull/35422) — closed · [PR #35617](https://github.com/sgl-project/sglang/pull/35617) — open

- **NVFP4 MoE:** proposed an opt-in FlashInfer CUTLASS path for small-batch decode on GB10, targeting dispatch overhead and supporting both Gate/Up weight layouts.
- **Mixed-precision backend selection:** proposed selecting the existing FlashInfer CUTLASS runner automatically for ModelOpt mixed MoE on SM120. #35617 supersedes #35422.

#### [DeepInfer](https://github.com/deepseek-ai/DeepInfer) · Evaluation and Ascend NPU · 20k+ ⭐

[PR #31](https://github.com/deepseek-ai/DeepInfer/pull/31) · [PR #33](https://github.com/deepseek-ai/DeepInfer/pull/33) · [PR #129](https://github.com/deepseek-ai/DeepInfer/pull/129) · [PR #139](https://github.com/deepseek-ai/DeepInfer/pull/139)

- **Evaluation:** proposed fixes for AIME answer extraction before sentence-ending periods and for sample-index validation in coverage reporting.
- **Ascend 910B3:** proposed a PCI sysfs fallback for NUMA discovery in containers, plus **34 numerical tests** for ViT variable-length attention covering precision, tensor layouts and sequence isolation.

<sub>These four DeepInfer pull requests were open on 2026-10-27.</sub>

#### Other contributions

- **[FlashInfer #4490](https://github.com/flashinfer-ai/flashinfer/pull/4490):** build fingerprints for stale NVCC JIT cache invalidation.
- **[Strata #3582](https://github.com/Niko1221/Strata/pull/3582):** Ascend MoE numerical validation and compensated S2 rounding.

### 🚀 Building

**[Uniform DGX Spark — Claude Code Plugin](https://github.com/zhachar14h-cell/uniform-dgxspark-claude-plugin)**

A Claude Code client for a running Uniform DGX Spark platform: deploy models, follow progress, inspect logs and monitor machine metrics from a coding session.

`TypeScript` · `Claude Code` · `DGX Spark` · `Model Deployment`

---

<div align="center">
  <sub>From kernel behavior to serving behavior — measure, verify, improve.</sub>
</div>

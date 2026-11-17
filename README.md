# ComfyUI Model Notes

> 个人 AI 模型链接索引与 ComfyUI 放置位置备忘
> 适配 **NVIDIA GeForce RTX 3050 4GB Laptop GPU** 与 **NVIDIA GeForce RTX 5070 12GB**

<h3 align="center">
  <a href="https://d1irgger.github.io/ai-repo-collection/">🌐 打开在线展示页面 →</a>
</h3>

<p align="center">
  <a href="https://d1irgger.github.io/ai-repo-collection/">
    <img src="https://img.shields.io/badge/GitHub_Pages-Online_Showcase-0071e3?style=for-the-badge&logo=githubpages&logoColor=white" alt="Online Showcase">
  </a>
</p>

<p align="center">
  <sub>网页为主展示入口；下方文本已折叠，展开后可自由选中复制。</sub>
</p>

---

## 说明

- **在线展示**：https://d1irgger.github.io/ai-repo-collection/
- **适配设备**：
  - 4GB 显存：NVIDIA GeForce RTX 3050 4GB Laptop GPU
  - 12GB 显存：NVIDIA GeForce RTX 5070
- 本 README 保留全部原始文本，按板块折叠，方便检索与复制。
- 本仓库只记录模型来源链接与放置位置，**不包含模型权重文件**。

---

<details>
<summary><b>📸 效果图</b>（2 张，点击展开）</summary>

<br>

<p align="center">
  <img src="assets/lustify/result-01.png" width="320" alt="LUSTIFY 效果图"><br>
  <sub><b>LUSTIFY! [NSFW checkpoint]</b> · 配 Krea-2 工作流</sub>
</p>

<p align="center">
  <img src="assets/moss/result-02.png" width="320" alt="MOSS 效果图"><br>
  <sub><b>Moss Image - Better Nudes</b> · 配 MOSS-Image</sub>
</p>

</details>

<details>
<summary><b>📋 模型总表</b>（点击展开）</summary>

<br>

| 模型名 | 类型 | 放置路径 | 链接 | 备注 |
|---|---|---|---|---|
| LUSTIFY! [NSFW checkpoint] | Checkpoint | `models/checkpoints/` | https://civitai.red/models/573152/lustify-nsfw-checkpoint | 配 Krea-2 工作流，含 text encoder / VAE |
| Moss Image - Better Nudes | Checkpoint | `models/checkpoints/` | https://civitai.red/models/3008073/moss-image-better-nudes | 配 MOSS-Image，含 diffusion model / text encoder / VAE |

</details>

<details>
<summary><b>🧩 LUSTIFY! [NSFW checkpoint]</b>（点击展开）</summary>

<br>

- **主模型**：https://civitai.red/models/573152/lustify-nsfw-checkpoint
- **放置路径**：`ComfyUI/models/checkpoints/`
- **对应工作流**：https://civitai.red/models/2503119/lustify-workflows-krea-2-sdxl?modelVersionId=3123550
- **版本备注**：自制 11（含义待确认）
- **配套来源**：Krea-2 https://huggingface.co/Comfy-Org/Krea-2/tree/main

**配套文件**

| 文件 | 来源目录 | 放置路径 |
|---|---|---|
| qwen3vl_4b_fp8_scaled.safetensors | `Krea-2/text_encoders` | `ComfyUI/models/text_encoders/` |
| qwen_image_vae.safetensors | `Krea-2/vae` | `ComfyUI/models/vae/` |
| 按实际下载文件名 | `Krea-2/diffusion_models` | `ComfyUI/models/diffusion_models/` |

> NSFW checkpoint；工作流为 Krea-2 / SDXL 相关，`diffusion_models` 下的文件按实际下载名放置。

<details>
<summary>工作流参考图（2 张）</summary>

<br>

<p>
  <img src="assets/lustify/workflow-01.png" width="49%" alt="LUSTIFY 工作流 1">
  <img src="assets/lustify/workflow-02.png" width="49%" alt="LUSTIFY 工作流 2">
</p>

</details>

</details>

<details>
<summary><b>🧩 Moss Image - Better Nudes</b>（点击展开）</summary>

<br>

- **主模型**：https://civitai.red/models/3008073/moss-image-better-nudes
- **放置路径**：`ComfyUI/models/checkpoints/`
- **配套来源**：MOSS-Image https://huggingface.co/Comfy-Org/MOSS-Image/tree/main

**配套文件**

| 文件 | 来源目录 | 放置路径 |
|---|---|---|
| moss_image_base_bf16.safetensors | `MOSS-Image/diffusion_models` | `ComfyUI/models/diffusion_models/` |
| qwen3.5_9b_bf16.safetensors | `MOSS-Image/text_encoders` | `ComfyUI/models/text_encoders/` |
| flux2-vae.safetensors | `MOSS-Image/vae` | `ComfyUI/models/vae/` |

> NSFW；MOSS-Image 仓库内文件已按类型标注，直接对照上表放置即可。

<details>
<summary>工作流参考图（2 张）</summary>

<br>

<p>
  <img src="assets/moss/workflow-03.png" width="49%" alt="MOSS 工作流 1">
  <img src="assets/moss/workflow-04.png" width="49%" alt="MOSS 工作流 2">
</p>

</details>

</details>

<details>
<summary><b>🗂️ ComfyUI 路径映射</b>（点击展开）</summary>

<br>

| 模型类型 | 放置路径 | 说明 |
|---|---|---|
| Checkpoint | `ComfyUI/models/checkpoints/` | 完整主模型 |
| Diffusion Model / UNet | `ComfyUI/models/diffusion_models/` | 单独 diffusion model |
| Text Encoder | `ComfyUI/models/text_encoders/` | qwen3vl、qwen3.5 等 |
| LoRA | `ComfyUI/models/loras/` | 需与基座匹配 |
| VAE | `ComfyUI/models/vae/` | 单独 VAE，如 qwen_image_vae、flux2-vae |
| ControlNet | `ComfyUI/models/controlnet/` | 控制网模型 |
| Embeddings | `ComfyUI/models/embeddings/` | 文本反推 |
| CLIP Vision | `ComfyUI/models/clip_vision/` | IP-Adapter 等用 |
| Upscale | `ComfyUI/models/upscale_models/` | 放大模型 |
| 工作流 | `ComfyUI/user/default/workflows/` | 也可直接存 JSON 备注 |

</details>

---

<p align="center">
  <sub>ComfyUI Model Notes · 个人参考记录 · 不含模型权重文件</sub>
</p>

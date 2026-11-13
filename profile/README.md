<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/budgetany_dark.svg">
    <img src="assets/budgetany_light.svg" height="92" alt="BudgetAny">
  </picture>
</p>

<p align="center">
  🌐 <a href="https://budgetany.github.io/"><b>Web page</b></a> &nbsp;|&nbsp;
  📄 <a href="https://arxiv.org/abs/2610.12307">Paper</a> &nbsp;|&nbsp;
  🤗 <a href="https://huggingface.co/BudgetAny">Hugging Face</a>
</p>

**Generative models that run at any compute budget.** BudgetAny collects open-source implementations of
compute-adaptive ("budget") tokenization. A generative model is fine-tuned so that one checkpoint runs on a variable
number of tokens, chosen at inference: detailed content keeps fine tokens, simple content is merged into coarse ones,
and compute and memory fall with the token count.

> **Unofficial, open-source implementation.** The method comes from
> [BudgetPix: Compute-Adaptive Tokenization for Pixel-Space Image Diffusion](https://arxiv.org/abs/2610.12307)
> (Kara et al., 2026). The code and models here are a community reimplementation and extension of it, not an
> official release, and BudgetAny is not a company, a lab or a formal organisation: the name only groups the
> repositories.

## Categories

| | Category | Task | Code | Page | Paper |
|:---:|---|---|---|---|---|
| <img src="assets/budgetpix_mark.svg" width="64" height="64" alt="BudgetPix"> | **BudgetPix** | pixel-space image generation | [BudgetPix](https://github.com/BudgetAny/BudgetPix) | [budgetpix](https://budgetany.github.io/budgetpix/) | [arXiv:2610.12307](https://arxiv.org/abs/2610.12307) |
| <img src="assets/budget3d_mark.svg" width="64" height="64" alt="Budget3D"> | **Budget3D** | image-to-3D generation (3D Gaussian splats) | [Budget3D](https://github.com/BudgetAny/Budget3D) | [budget3d](https://budgetany.github.io/budget3d/) | tech report coming soon |
| <img src="assets/budgetlatent_mark.svg" width="64" height="64" alt="BudgetLatent"> | **BudgetLatent** | latent-space image generation | coming soon | [budgetlatent](https://budgetany.github.io/budgetlatent/) | tech report coming soon |

## Models

### <img src="assets/budgetpix_mark.svg" width="32" height="32" alt=""> BudgetPix

| Model repository | Base model | Task | License of the weights |
|---|---|---|---|
| [BudgetAny/BudgetPix-JiT](https://huggingface.co/BudgetAny/BudgetPix-JiT) | [JiT](https://github.com/LTH14/JiT) B/16, B/32, L/16, L/32 | class-conditional ImageNet, 256 and 512 px | MIT |
| [BudgetAny/BudgetPix-pMF](https://huggingface.co/BudgetAny/BudgetPix-pMF) | [pixel MeanFlow](https://github.com/Lyy-iiis/pMF) L/16 | one-step class-conditional ImageNet, 256 px | MIT |
| [BudgetAny/BudgetPix-MiniT2I](https://huggingface.co/BudgetAny/BudgetPix-MiniT2I) | [MiniT2I](https://huggingface.co/MiniT2I/MiniT2I) B/16, L/16 | text-to-image, 512 px | MIT |
| [BudgetAny/BudgetPix-PixelDiT](https://huggingface.co/BudgetAny/BudgetPix-PixelDiT) | [PixelDiT-T2I 1.3B](https://huggingface.co/nvidia/PixelDiT-1300M-1024px) | text-to-image, 1024 px | NVIDIA License (NSCLv1), non-commercial |

### <img src="assets/budget3d_mark.svg" width="32" height="32" alt=""> Budget3D

| Model repository | Base model | Task | License of the weights |
|---|---|---|---|
| [BudgetAny/Budget3D-Idol](https://huggingface.co/BudgetAny/Budget3D-Idol) | [speridlabs/idol](https://huggingface.co/speridlabs/idol) | image-to-3D, 50 steps | Apache-2.0 |
| [BudgetAny/Budget3D-Idol-Turbo](https://huggingface.co/BudgetAny/Budget3D-Idol-Turbo) | [speridlabs/idol-turbo](https://huggingface.co/speridlabs/idol-turbo) | image-to-3D, 5 steps | Apache-2.0 |

### <img src="assets/budgetlatent_mark.svg" width="32" height="32" alt=""> BudgetLatent

Coming soon.

## Citation

If you use these models or the code, please cite the BudgetPix paper, and BudgetAny:

```bibtex
@article{kara2026budgetpix,
  title={BudgetPix: Compute-Adaptive Tokenization for Pixel-Space Image Diffusion},
  author={Ozgur Kara and Yujia Chen and Daniel Watson and David Forsyth and James Matthew Rehg and Wen-Sheng Chu and Du Tran},
  journal={arXiv preprint arXiv:2610.12307},
  year={2026}
}

@misc{budgetany2026,
  title={BudgetAny: Generative Models at Any Compute Budget},
  author={Ozgur Kara},
  year={2026},
  howpublished={\url{https://budgetany.github.io}}
}
```

Built on [JiT](https://github.com/LTH14/JiT), [pixel MeanFlow](https://github.com/Lyy-iiis/pMF),
[MiniT2I](https://github.com/Hope7Happiness/minit2i-torch), [PixelDiT](https://github.com/NVlabs/PixelDiT),
[Idol and Idol-turbo](https://huggingface.co/speridlabs), [FLUX.2](https://github.com/black-forest-labs/flux2),
[DINOv3](https://github.com/facebookresearch/dinov3) and [APT](https://github.com/rccchoudhury/apt).

<p align="center">
  <img src="assets/logo.png"  height=360>
</p>


### <div align="center"> UltraHR-100K: Enhancing UHR Image Synthesis with A Large-Scale High-Quality Dataset <div> 
<div align="center">
  <a href="https://nju-pcalab.github.io/projects//UltraHR-100K"><img src="https://img.shields.io/static/v1?label=UltraHR-100K&message=Project&color=purple"></a> &ensp;
  <a href="https://arxiv.org/abs/2510.20661"><img src="https://img.shields.io/static/v1?label=Paper&message=Arxiv&color=red&logo=arxiv"></a> &ensp;
  <a href="https://huggingface.co/datasets/zhihefang/UltraHR-100K"><img src="https://img.shields.io/static/v1?label=Dataset&message=HuggingFace&color=yellow"></a> &ensp;
</div>


## UltraHR-100K
ltra-high-resolution (UHR) text-to-image (T2I) generation has seen notable progress. However, two key challenges remain : 1) the absence of a large-scale high-quality UHR T2I dataset, and (2) the neglect of tailored training strategies for fine-grained detail synthesis in UHR scenarios. To tackle the first challenge, we introduce \textbf{UltraHR-100K}, a high-quality dataset of 100K UHR images with rich captions, offering diverse content and strong visual fidelity. Each image exceeds 3K resolution and is rigorously curated based on detail richness, content complexity, and aesthetic quality. To tackle the second challenge, we propose a frequency-aware post-training method that enhances fine-detail generation in T2I diffusion models. Specifically, we design (i) \textit{Detail-Oriented Timestep Sampling (DOTS)} to focus learning on detail-critical denoising steps, and (ii) \textit{Soft-Weighting Frequency Regularization (SWFR)}, which leverages Discrete Fourier Transform (DFT) to softly constrain frequency components, encouraging high-frequency detail preservation. Extensive experiments on our proposed UltraHR-eval4K benchmarks demonstrate that our approach significantly improves the fine-grained detail quality and overall fidelity of UHR image generation. 

## News 🚀🚀🚀
- **[2025.09.18]** 🏆 UltraHR-100K is accepted by **NeurIPS 2025**!!!


## Preparation
### Environment
```bash
conda create -n openvid python=3.10
conda activate openvid
pip install torch torchvision
pip install packaging ninja
pip install flash-attn --no-build-isolation
pip install -v --disable-pip-version-check --no-cache-dir --no-build-isolation --config-settings "--build-option=--cpp_ext" --config-settings "--build-option=--cuda_ext" git+https://github.com/NVIDIA/apex.git
pip install -U xformers --index-url https://download.pytorch.org/whl/cu121
```

### Dataset
Download [UltraHR-100K](https://huggingface.co/datasets/zhihefang/UltraHR-100K) dataset.

`
## Benchmark
Download [UltraHR-100K](https://huggingface.co/datasets/zhihefang/UltraHR-100K) dataset.


## Citation
```bibtex
@article{sun2022shufflemixer,
  title={UltraHR-100K: Enhancing UHR Image Synthesis with A Large-Scale High-Quality Dataset},
  author={Chen Zhao, En Ci, Yunzhe Xu, Tiehan Fan, Shanyan Guan, Yanhao Ge, Jian Yang, Ying Tai},
  journal={Advances in Neural Information Processing Systems},
  year={2025}
}
```

---
license: apache-2.0
base_model: Qwen/Qwen3.5-4B-Instruct
tags:
- openvino
- nncf
- int4
- optimum
- text-generation-inference
pipeline_tag: text-generation
library_name: optimum
language:
- en
- zh
---

# Aura-1-Thinking (With A OpenVINO INT4 Optimized Version)
This repository contains the cutting-edge **Aura-1-Thinking** reasoning model available in two production-ready formats: a standard **Non-OpenVINO base layer** for native PyTorch environments, and a highly optimized layout compiled into Intel's **OpenVINO™ Intermediate Representation (IR)** format. For the OpenVINO engine, the model weights have been downscaled to high-efficiency asymmetric **INT4** precision using the Neural Network Compression Framework (NNCF).

This engine is tailor-made to deliver high-speed, localized token streaming on consumer-grade hardware, including standard **Dual-Core CPUs (2 vCPU)** and setups with **16GB RAM** or less.

---

## 📊 Performance Footprint Comparison

| Optimization Layer | Resource Footprint (RAM/VRAM) | Minimum Target Hardware | Run Status |
| :--- | :--- | :--- | :--- |
| **Baseline Raw (FP16)** | `~8.5 GB - 10.0 GB` | Dedicated Tensor Core GPU | High Overhead |
| **Aura OpenVINO (INT4)**| **`~2.2 GB - 2.8 GB`** | **Basic Laptop CPU (2vCPU)** | **Ultra-Fast Stream** |

---

## ⚡ Model On HuggingFace

View The Project On HuggingFace by Visiting https://huggingface.co/arthpandeyofficial/Aura-1-Thinking

# Hi, I'm Zixin Jia 👋

**Physics at Peking University · hardware, systems and sensor fusion · project lead of [Swift IARS](https://github.com/zixinzenith/swift-iars) (2024 startup project)**

I like problems where the physics and the code have to agree — inertial navigation, GPU kernels, computer architecture, and the messy real-time systems that sit in between. I'm currently applying for CS/ECE master's programs.

---

## Featured project — Swift IARS

**[Swift IARS — Integrated Augmented Reality System](https://github.com/zixinzenith/swift-iars)**

A helmet-clip AR head-up display that replaces the four-to-five separate instruments skydivers, wingsuit pilots and firefighters strap to themselves with one fused, stabilised display. A 2024 startup project — I led it and did the embedded/algorithm work, with a teammate on industrial design and a team flight campaign. The algorithm core is open-sourced now: an implementation of the 2024 design written in 2026 with AI coding assistance, and the repo says so.

<p align="center">
  <img src="https://raw.githubusercontent.com/zixinzenith/swift-iars/main/docs/assets/hero_freefall_hud.jpg" width="85%" alt="Swift IARS HUD during freefall" />
</p>

Four algorithms are designed to keep the display readable at 50 m/s:

| | Block | What it does |
|---|---|---|
| I | [Redundancy design & fault-tolerant fusion](https://github.com/zixinzenith/swift-iars/blob/main/iars/redundancy/fusion.py) | four altitude sources, consensus voting, fault isolation, bias tracking |
| II | [Head-motion stabilisation](https://github.com/zixinzenith/swift-iars/blob/main/iars/stabilization/head_motion.py) | separates voluntary head turns from airflow buffeting (−26 dB) |
| III | [Binocular display alignment](https://github.com/zixinzenith/swift-iars/blob/main/iars/stereo/alignment.py) | recovers and corrects per-eye waveguide misalignment |
| IV | [Multi-sensor SLAM / INS fusion](https://github.com/zixinzenith/swift-iars/blob/main/iars/slam/eskf.py) | 15-state error-state Kalman filter over IMU + baro + GNSS + stereo vision |

`Python` · `error-state Kalman filter` · `sensor fusion` · `real-time embedded` · `MIT licensed`

---

## GPU kernels, compilers and systems

| Repository | Focus |
|---|---|
| [triton-lab](https://github.com/zixinzenith/triton-lab) | Triton kernels — blocked matmul (~80% of tensor roofline), fused epilogues, softmax, layernorm, GQA attention — with benchmarks and profiling notes |
| [cuda-lab](https://github.com/zixinzenith/cuda-lab) | stand-alone CUDA exercises: tiled matmul, coalesced transpose, shared-memory reductions, streams, cuBLAS |
| [llvm-lab](https://github.com/zixinzenith/llvm-lab) | notes and experiments while learning LLVM IR and `clang -emit-llvm` |
| [QuantKernelBench](https://github.com/zixinzenith/QuantKernelBench) | a benchmark of 40 quantized GPU operators (INT4 packing, dequant-GEMV, GEMM, KV-cache, fused ops) with bit-exact / error-bound oracles and an agent loop for studying LLM kernel generation |
| [AI-infra-training-camp](https://github.com/zixinzenith/AI-infra-training-camp) | AI-infrastructure coursework and decode-path experiments |

---

## Toolbox

`Python` `C/C++` `CUDA` `Triton` `LLVM` `NumPy` `Git` · embedded firmware, IMU/GNSS sensor stacks, Kalman filtering, computer architecture

---

## Links

- 📌 Featured work: [Swift IARS algorithm core](https://github.com/zixinzenith/swift-iars)
- ✉️ zixinzenith@gmail.com

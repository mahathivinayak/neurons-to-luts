# FPGA-Based Hardware-Aware Equalizer

Capstone Project | Learning-to-Implementation Journey

## Overview

This repository documents my capstone project and structured learning journey, starting from fundamental concepts and culminating in the design and FPGA implementation of a hardware-optimized digital equalizer.

The project emphasizes hardware-aware design techniques such as parallelism, fixed-point arithmetic, and bit-width optimization to achieve a low-latency and resource-efficient FPGA implementation, inspired by modern machine learning acceleration workflows.

## Project Objective

The primary objectives of this capstone project are:

* Design a multi-band digital equalizer
* Implement the design on an FPGA platform
* Apply hardware optimization techniques including:

  * Parallel processing
  * Fixed-point arithmetic
  * Bit-width and word-length optimization
* Evaluate performance in terms of:

  * Latency
  * Throughput
  * Resource utilization
  * Signal quality

## Motivation

Conventional software-based equalizers often suffer from high latency, limited parallelism, and inefficient power usage in real-time systems.

FPGAs provide true hardware parallelism, deterministic timing behavior, and efficient execution of DSP-intensive workloads.

Furthermore, techniques used in machine learning inference acceleration—such as quantization, MAC parallelism, and pipelining—closely align with FPGA-based DSP design, motivating a hardware-aware approach.

## Learning Context

This project was undertaken with no prior background in machine learning.

Machine learning concepts are included only where they provide architectural insight, specifically to:

* Understand MAC-based parallel computation
* Study precision and quantization trade-offs
* Draw parallels between CNN-style convolution and FIR filtering

The repository reflects a progression from conceptual understanding to hardware realization.

## Project Flow

The project follows an end-to-end workflow consisting of four main stages.

## Data Generation (MATLAB)

* Generate PAM4 and PAM8 signals
* Simulate channel impairments
* Export datasets for further processing

## Model Training (PyTorch)

* Import generated datasets
* Define a simple CNN or signal-processing model
* Train using forward and backward propagation
* Save trained weights for hardware deployment

## FPGA Implementation

* Convert trained model or algorithm to HLS-compatible C or C++
* Apply quantization and bit-width optimization
* Introduce parallelism and pipelining
* Synthesize RTL using Vivado HLS or Zynq
* Deploy the design on FPGA hardware

## Performance Analysis

* Measure Bit Error Rate before and after equalization
* Analyze latency, throughput, and FPGA resource utilization
* Generate plots and visualizations

Final outcome: improved signal quality and efficient real-time equalization on FPGA.

## Repository Structure

```text
fpga-equalizer/
│
├── 00-foundations/
├── 01-ml-core-concepts/
├── 02-cnn-and-convolution/
├── 03-hardware-aware-ml/
├── 04-equalizer-design/
├── 05-fpga-implementation/
├── 06-results-and-analysis/
├── 07-final-project/
│
├── diagrams/
├── references/
├── .gitignore
├── LICENSE
└── README.md
```

## Functional Requirements

* Accept digitized input signal samples
* Apply frequency-selective gain across multiple bands
* Operate in real time
* Produce equalized output samples continuously

## Non-Functional Requirements

* Low latency
* High throughput
* Deterministic timing
* Efficient FPGA resource utilization
* Scalability with respect to:

  * Number of bands
  * Bit-width
  * Sampling frequency

## Literature Survey

The literature survey focuses on FPGA-based equalizer architectures, fixed-point DSP implementations, hardware-aware machine learning inference, and precision and quantization trade-offs.

Detailed summaries and comparisons are provided in the references directory.

## Tools and Technologies

* MATLAB
* PyTorch
* Vivado HLS and Zynq
* Fixed-point arithmetic and DSP techniques

## System Flow
<img width="323" height="720" alt="image" src="https://github.com/user-attachments/assets/3fab45d4-9369-43de-8a03-73380b1ee461" />


## Future Work

* Adaptive equalization techniques
* Support for higher-order modulation schemes
* Power consumption analysis
* Comparison with GPU-based inference pipelines

## License

This project is licensed under the Apache License 2.0.
If you use or build upon this work, please provide appropriate attribution.
```

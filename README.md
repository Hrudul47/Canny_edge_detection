# FPGA-Based Canny Edge Detection (Simulation Only)

## 📌 Overview

This project presents the implementation and verification of the **Canny Edge Detection** algorithm using Verilog HDL. The design is validated through simulation and demonstrates the complete edge detection pipeline commonly used in image processing applications.

The system processes grayscale images with a resolution of **128 × 128 pixels (16,384 pixels total)** and generates refined edge maps with improved noise suppression and edge localization.

---

## 🔹 Canny Edge Detection (Simulation Implementation)

### ⚙️ Description

The Canny Edge Detection algorithm is implemented in Verilog HDL and verified using simulation. Due to its computational complexity and resource requirements, the design is not deployed on FPGA hardware in this project.

The implementation follows the standard Canny edge detection pipeline to produce accurate and noise-free edge outputs.

---

## 🧩 Pipeline Stages

1. **Gaussian Blur**

   * Reduces image noise and smooths the input image.

2. **Gradient Computation**

   * Computes edge gradients using Sobel operators.

3. **Non-Maximum Suppression (NMS)**

   * Eliminates non-edge pixels to produce thin edges.

4. **Double Thresholding**

   * Classifies pixels as strong, weak, or non-edges.

5. **Hysteresis**

   * Tracks connected edge pixels and removes isolated responses.

---

## 📁 Project Structure

```text
canny_top.v
gaussian_blur.v
nms.v
double_threshold.v
hysteresis.v
line_buffer.v
window3x3.v
canny_tb.v
input.mem
output.mem
```

---

## ▶️ Simulation Procedure

1. Open Xilinx Vivado Simulator (xsim).
2. Create a simulation project.
3. Add all Canny-related Verilog source files.
4. Set `canny_tb.v` as the top-level testbench.
5. Place the input image data in `input.mem`.
6. Run behavioral simulation.
7. Observe generated edge outputs and waveform results.
8. Verify the generated output stored in memory files.

---

## 📊 Results

| Parameter        | Value     |
| ---------------- | --------- |
| Image Resolution | 128 × 128 |
| Total Pixels     | 16,384    |
| Edge Pixels      | 2,689     |
| Edge Density     | 16.41%    |

### Observation

The Canny algorithm produces thin, accurate, and noise-free edges. Compared with traditional gradient-based methods, it provides superior edge localization and reduced false edge detection.

---

## ⚡ Hardware Platform

Although the current work is simulation-based, the target platform for future hardware implementation is:

* **Board:** Nexys A7
* **FPGA:** Xilinx Artix-7 (XC7A100T)
* **Development Tool:** Xilinx Vivado

---

## 🚀 Applications

* Computer Vision
* Embedded Image Processing
* Robotics
* Industrial Inspection
* Autonomous Systems
* Medical Imaging
* Surveillance and Security Systems

---

## 📌 Notes

* The design is verified through simulation only.
* Input and output image data are handled using `.mem` files.
* The project demonstrates the complete Canny edge detection pipeline in Verilog HDL.
* Future work includes FPGA deployment and real-time image processing support.

---

## 📜 License

This project is intended for academic and research purposes.

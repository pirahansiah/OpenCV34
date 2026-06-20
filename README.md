# OpenCV 3.4 — Build from Source (Visual Studio 2015, No CUDA)

[![OpenCV](https://img.shields.io/badge/OpenCV-3.4-blue?logo=opencv&logoColor=white)](https://opencv.org/)
[![Visual Studio](https://img.shields.io/badge/Visual%20Studio-2015-purple?logo=visualstudio&logoColor=white)](https://visualstudio.microsoft.com/)
[![License](https://img.shields.io/badge/License-Apache%202.0-green.svg)](LICENSE)

Pre-configured build of **OpenCV 3.4.x** for Windows using Visual Studio 2015 without CUDA support.

## Overview

This repository provides a ready-to-use OpenCV 3.4 build configuration targeting systems without NVIDIA GPU acceleration. Ideal for CPU-only desktop and embedded deployments.

## Build Instructions

### Prerequisites

- **Visual Studio 2015** (v140 toolset)
- **CMake** 3.x+
- **Python** 2.7 or 3.x (optional, for Python bindings)

### Steps

```bash
# Clone
git clone https://github.com/pirahansiah/OpenCV34.git
cd OpenCV34

# Configure (no CUDA)
cmake -G "Visual Studio 14 2015 Win64" \
  -D WITH_CUDA=OFF \
  -D BUILD_opencv_python2=ON \
  -D BUILD_opencv_python3=ON \
  ..

# Build
cmake --build . --config Release
```

## Build Configuration

| Option | Value |
|--------|-------|
| OpenCV Version | 3.4.x |
| Compiler | MSVC 14.0 (VS 2015) |
| CUDA | Disabled |
| Python | 2.7 / 3.x bindings |
| Target | Windows x64 |

## 2025–2026: When to Use OpenCV 3.4 vs. Modern Alternatives

| Use Case | Recommendation |
|----------|---------------|
| Legacy Windows XP/7 targets | OpenCV 3.4 ✅ |
| New projects (2025+) | OpenCV 4.x / 5.x with CUDA or oneAPI |
| Edge AI (Jetson, NPU) | OpenCV 4.10 + TensorRT 10 / OpenVINO 2025 |
| Real-time video analytics | OpenCV 4.10 + GStreamer 1.24 / MediaPipe |
| ONNX Runtime inference | OpenCV 4.10 DNN module + ONNX Runtime 1.20+ |

### Modern OpenCV Ecosystem (2025–2026)

- **OpenCV 4.10+**: Improved DNN backend (TensorRT, OpenVINO, CoreML), better Android/iOS support
- **OpenCV 5.0 (preview)**: C++20 modules, improved Python bindings, Vulkan compute backend
- **OpenCV.js**: WebAssembly builds for browser-based CV
- **G-API**: Graph-based API for heterogeneous pipeline acceleration

## Related Projects

- [opencv](https://github.com/pirahansiah/opencv) — General OpenCV examples
- [opencv4](https://github.com/pirahansiah/opencv4) — OpenCV 4.x builds
- [opencv5vs2022](https://github.com/pirahansiah/opencv5vs2022) — OpenCV 5.x for VS 2022

## Author

**Farshid Pirahansiah**
- Website: [pirahansiah.com](https://www.pirahansiah.com)
- GitHub: [github.com/pirahansiah](https://github.com/pirahansiah)
- LinkedIn: [linkedin.com/in/pirahansiah](https://www.linkedin.com/in/pirahansiah)

## License

Apache License 2.0 — See [LICENSE](LICENSE) for details.

## Maxim Eremenko

Research Scientist at ORNL / Theiss Research — physics, high-performance computing, and scientific software.

📍 Oak Ridge, TN · 📫 [erjomenko@gmail.com](mailto:erjomenko@gmail.com) · 💻 [github.com/MaximEremenko](https://github.com/MaximEremenko) · 🎓 [Google Scholar](https://scholar.google.com/citations?user=kJCFRkUAAAAJ) · 🆔 [ORCID](https://orcid.org/0000-0002-2875-968X) · 💼 [LinkedIn](https://www.linkedin.com/in/maksim-eremenko-417270109/)

Browser-based tools for diffuse-scattering and local-structure analysis of disordered crystalline materials. Everything runs fully client-side — no installation, no server, no uploads — and the applications share a unified HDF5 data contract, interoperating with RMCProfile, DISCUS, Yell, Meerkat, and Scatty.

### 🔬 Featured research tools

All Apache-2.0; output from one tool loads directly in the others.

| Tool | What it does | Technical highlights |
| --- | --- | --- |
| [3DSCalc](https://github.com/MaximEremenko/3DSCalc) | Forward calculator: computes the 3-D diffuse intensity I(*hkl*) in reciprocal space directly from atomistic configurations (RMCProfile `.rmc6f`, LAMMPS data files, unified structure HDF5) and visualizes it as interactive 3-D isosurfaces, slice planes, and 2-D maps | Type-3 NUFFT on a user-defined *hkl* grid with three engines — WebGPU, CPU FFT, and direct CPU summation for verification; neutron, X-ray, and electron scattering tables; average-lattice subtraction and 3-D smoothing; exports to `.dat`, unified HDF5, ParaView `.vtk`, `.cube`, CSV/SVG, and standalone Plotly HTML |
| [3DSView](https://github.com/MaximEremenko/3DSView) | Interactive slicer for pre-computed 3-D diffuse volumes: axis, arbitrary-normal-plane, and slab-average slicing with linked 2-D heatmap, 3-D plane, and 3-D isosurface views | Reads RMCProfile 3DS text, unified HDF5, DISCUS/Yell HDF5, and generic NeXus; Q/HKL-aware axes with unit-cell override and delta-PDF (3D-PDF) support; large text files are streamed, parsed in parallel Web Workers, and cached in IndexedDB for near-instant reloads |
| [DiffuseConvert](https://github.com/MaximEremenko/diffuse-convert) | Converts 3-D single-crystal diffuse data between the formats used by RMCProfile, DISCUS, Yell, Meerkat, and Scatty — any format to any other, input auto-detected | Unified HDF5, Yell 1.0 HDF5, RMCProfile `.dat`, and Scatty `.vtk`; parent-cell handling from `.rmc6f` or unified structure files; fully self-contained (vendored WebAssembly h5wasm, runs from `file://`); validated against real output files from each producer, with round-trip conversions exact at double precision |

<!-- Optional sentence; edit or delete as distribution plans settle: -->
Some of these tools may in the future also be distributed under the ORNL "neutrons" GitHub organization.

### 🗂️ Selected projects

- **[Utilities](https://github.com/MaximEremenko/Utilities)** — browser utilities for RMC-based workflows: Select Subvolume, PCA KDE, PCA SDE, and Background Remover, with a [GitHub Pages docs site](https://maximeremenko.github.io/Utilities/).
- **[MOSAIC](https://github.com/MaximEremenko/MOSAIC)** — a Python framework linking selected diffuse-scattering features to site-resolved chemical-order and displacement fields via a linear, phase-preserving workflow (scattering amplitudes, reciprocal-space masking, inverse Fourier transforms), with optional GPU acceleration and Dask-based parallel execution.
- **[WebGPU-NUFFT](https://github.com/MaximEremenko/WebGPU-NUFFT)** and **[WebGPU-FFT](https://github.com/MaximEremenko/WebGPU-FFT)** — MIT-licensed JavaScript/WGSL libraries for GPU non-uniform and uniform FFTs in the browser; WebGPU-FFT uses a plan-based execution model with FFT/DCT/convolution support, and WebGPU-NUFFT powers the calculator's WebGPU path (served via jsDelivr).
- **wgpuFFT** — a Rust WebGPU FFT/NUFFT library (type-1/2/3 NUFFTs, rank-generic N-dimensional plans, native f64 and portable double-float precision, WebAssembly/browser support) — the Rust counterpart of the WebGPU-FFT/NUFFT line, publication in preparation.
- **[UnifiedStructureFileFormat](https://github.com/MaximEremenko/UnifiedStructureFileFormat)** and **[UnifiedIntensityFileFormat](https://github.com/MaximEremenko/UnifiedIntensityFileFormat)** — proposals for unified HDF5 file formats for atomistic structures and 3-D diffuse / 3D-PDF data: the shared data contract the tools above read and write.
- **[BBest](https://github.com/MaximEremenko/BBest)** — an updated version of the BBEST R package for Bayesian background estimation, removing incoherent scattering from neutron total-scattering data (original method by Gagin & Levin).

More in the [repositories tab](https://github.com/MaximEremenko?tab=repositories).

**Stack:** C/C++ · CUDA · Python (PyTorch, TensorFlow, Dask) · Rust · JavaScript + WebGPU/WGSL · WebAssembly · R · MPI / HPC clusters · HDF5.

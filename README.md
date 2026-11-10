## Maxim Eremenko

Research Scientist at ORNL / Theiss Research — physics, high-performance computing, and scientific software.

📍 Oak Ridge, TN · 📫 [erjomenko@gmail.com](mailto:erjomenko@gmail.com) · 💻 [github.com/MaximEremenko](https://github.com/MaximEremenko) · 🎓 [Google Scholar](https://scholar.google.com/citations?user=kJCFRkUAAAAJ) · 🆔 [ORCID](https://orcid.org/0000-0002-2875-968X) · 💼 [LinkedIn](https://www.linkedin.com/in/maksim-eremenko-417270109/)

### 🔬 Featured research tools

Browser-based tools for diffuse-scattering and local-structure analysis of disordered crystalline materials. Everything runs fully client-side — no installation, no server, no uploads — and the applications share a unified HDF5 data contract, interoperating with RMCProfile, DISCUS, Yell, Meerkat, and Scatty.

All Apache-2.0 and open source; output from one tool loads directly in the others. If you use them in published work, please [cite them](#-how-to-cite).

| Tool | What it does | Technical highlights |
| --- | --- | --- |
| **3DSCalculator**<br>[Live app](https://maximeremenko.github.io/3DSCalculator/) · [Source](https://github.com/MaximEremenko/3DSCalculator) | Forward calculator: computes the 3-D diffuse intensity I(*hkl*) in reciprocal space directly from atomistic configurations (RMCProfile `.rmc6f`, LAMMPS data files, unified structure HDF5) and visualizes it as interactive 3-D isosurfaces, slice planes, and 2-D maps | NUFFT engines on a user-defined *hkl* grid — [wgpuNUFFT](https://github.com/MaximEremenko/wgpuNUFFT) type-1 on WebGPU (default), a type-3 WebGPU path, CPU FFT and CPU f64 NUFFT, and exact direct summation for verification; neutron, X-ray, and electron scattering tables; average-lattice subtraction and 3-D smoothing; exports to `.dat`, unified HDF5, ParaView `.vtk`, `.cube`, CSV/SVG, and standalone Plotly HTML |
| **3DSView**<br>[Live app](https://maximeremenko.github.io/3DSView/) · [Source](https://github.com/MaximEremenko/3DSView) | Interactive slicer for pre-computed 3-D diffuse volumes: axis, arbitrary-normal-plane, and slab-average slicing with linked 2-D heatmap, 3-D plane, and 3-D isosurface views | Reads RMCProfile 3DS text, unified HDF5, DISCUS/Yell HDF5, and generic NeXus; Q/HKL-aware axes with unit-cell override and delta-PDF (3D-PDF) support; large text files are streamed, parsed in parallel Web Workers, and cached in IndexedDB for near-instant reloads |
| **3DSConvert**<br>[Live app](https://maximeremenko.github.io/3DSConvert/) · [Source](https://github.com/MaximEremenko/3DSConvert) | Converts 3-D single-crystal diffuse data between the formats used by RMCProfile, DISCUS, Yell, Meerkat, and Scatty — any format to any other, input auto-detected | Unified HDF5, Yell 1.0 HDF5, RMCProfile `.dat`, and Scatty `.vtk`; parent-cell handling from `.rmc6f` or unified structure files; fully self-contained (vendored WebAssembly h5wasm, runs from `file://`); validated against real output files from each producer, with round-trip conversions exact at double precision |

Also in the browser: **RMCProfile Coordination Monitor** — coordination numbers computed locally and tracked across an RMCProfile refinement ([live app](https://maximeremenko.github.io/neighbor_analysis/) · [source](https://github.com/MaximEremenko/neighbor_analysis)); **RMC6f utilities** — diffuse-scattering and structural-analysis tools for RMC6f configurations ([live app](https://maximeremenko.github.io/Utilities/) · [source](https://github.com/MaximEremenko/Utilities)).

### 🗂️ Selected projects

- **[3DSCalculator](https://github.com/MaximEremenko/3DSCalculator)** — forward calculator of 3-D diffuse scattering I(*hkl*) from atomistic models, in the browser (WebGPU / CPU engines).
- **[3DSView](https://github.com/MaximEremenko/3DSView)** — interactive slicer and viewer for pre-computed 3-D diffuse-scattering volumes.
- **[MOSAIC](https://github.com/MaximEremenko/MOSAIC)** — a Python framework linking selected diffuse-scattering features to site-resolved chemical-order and displacement fields via a linear, phase-preserving workflow (scattering amplitudes, reciprocal-space masking, inverse Fourier transforms), with optional GPU acceleration and Dask-based parallel execution. Method paper: [doi:10.48550/arXiv.2607.10440](https://doi.org/10.48550/arXiv.2607.10440).
- **[wgpuNUFFT](https://github.com/MaximEremenko/wgpuNUFFT)** — Rust nonuniform FFTs on the GPU through `wgpu` (Vulkan, DX12, Metal) and in the browser through WebGPU: type-1/2/3 transforms in one to eight dimensions, `f32`, native `f64`, and portable double-float precision, bitwise-repeatable results, and Python, C, Fortran, MATLAB, and Julia interfaces. It powers 3DSCalculator's default WebGPU engine.
- **[wgpuFFT](https://github.com/MaximEremenko/wgpuFFT)** — the Rust GPU FFT library underneath wgpuNUFFT: mixed-radix, Rader, and Bluestein FFTs of any length and shape in `f32`, `f64`, and double-float, natively and in the browser — the Rust counterpart of WebGPU-FFT.
- **[WebGPU-NUFFT](https://github.com/MaximEremenko/WebGPU-NUFFT)** and **[WebGPU-FFT](https://github.com/MaximEremenko/WebGPU-FFT)** — MIT-licensed JavaScript/WGSL libraries for GPU non-uniform and uniform FFTs in the browser; WebGPU-FFT uses a plan-based execution model with FFT/DCT/convolution support, and WebGPU-NUFFT powers the calculator's type-3 WebGPU path (served via jsDelivr).

More in the [repositories tab](https://github.com/MaximEremenko?tab=repositories).

### 📄 Selected publications

Full list on [Google Scholar](https://scholar.google.com/citations?user=kJCFRkUAAAAJ&view_op=list_works&sortby=pubdate) and [ORCID](https://orcid.org/0000-0002-2875-968X).

- **M. Eremenko**, V. Krayzman, A. Gagin, I. Levin (2017). Advancing reverse Monte Carlo structure refinements to the nanoscale. *J. Appl. Cryst.* **50**, 1561–1570. [doi:10.1107/S1600576717013140](https://doi.org/10.1107/S1600576717013140)
- **M. Eremenko**, V. Krayzman, A. Bosak, H. Y. Playford, K. W. Chapman, J. C. Woicik, B. Ravel, I. Levin (2019). Local atomic order and hierarchical polar nanoregions in a classical relaxor ferroelectric. *Nat. Commun.* **10**, 2728. [doi:10.1038/s41467-019-10665-4](https://doi.org/10.1038/s41467-019-10665-4)
- **M. Eremenko**, V. Krayzman, S. Gorfman, A. Bosak, H. Y. Playford, P. A. Chater, *et al.* (2025). Emergent topological polarization textures in relaxor ferroelectrics. *Nat. Commun.* **16**, 7531. [doi:10.1038/s41467-025-62658-1](https://doi.org/10.1038/s41467-025-62658-1)
- S. Gorfman, **M. Eremenko**, V. Krayzman, A. Bosak, P. Y. Zavalij, I. Levin (2026). Measurements and scaling of X-ray total scattering from single crystals. *J. Appl. Cryst.* **59**, 1224–1237. [doi:10.1107/S1600576726006187](https://doi.org/10.1107/S1600576726006187)
- **M. Eremenko**, V. Krayzman, M. G. Tucker, I. Levin (2026). Connecting diffuse scattering to atomic-site-resolved occupancy and displacement fields through Fourier filtering. *arXiv:2607.10440*. [doi:10.48550/arXiv.2607.10440](https://doi.org/10.48550/arXiv.2607.10440) — the method behind [MOSAIC](https://github.com/MaximEremenko/MOSAIC)

### 📝 How to cite

If these tools or methods help your research, please cite them — it is what keeps them maintained.

- **MOSAIC** — M. Eremenko, V. Krayzman, M. G. Tucker, I. Levin, *arXiv:2607.10440* (2026), [doi:10.48550/arXiv.2607.10440](https://doi.org/10.48550/arXiv.2607.10440). Software metadata: [CITATION.cff](https://github.com/MaximEremenko/MOSAIC/blob/main/CITATION.cff).
- **3DSCalculator, 3DSView, 3DSConvert, wgpuNUFFT, wgpuFFT, and the other tools** — cite the software by name and repository URL, for example: M. Eremenko, *3DSCalculator* (software), https://github.com/MaximEremenko/3DSCalculator.
- **Reverse Monte Carlo methods** — M. Eremenko *et al.*, *J. Appl. Cryst.* **50**, 1561–1570 (2017), [doi:10.1107/S1600576717013140](https://doi.org/10.1107/S1600576717013140).

**Stack:** C/C++ · CUDA · Python (PyTorch, TensorFlow, Dask) · Rust · JavaScript + WebGPU/WGSL · WebAssembly · R · MPI / HPC clusters · HDF5.

# CENG443-Final-Project-NM-Sparse-Kernels

Triton re-implementation of the CUDA C++ kernels from the target paper. This repo will host iterative notebook experiments while we port and validate kernels.

## Prerequisites
- Python 3.10+ (Triton requires >= 3.8; 3.10/3.11 recommended)
- CUDA-capable GPU and matching NVIDIA drivers for running Triton kernels (CPU-only is fine for reading/editing but Triton execution will be skipped)

## Quickstart
1. Create a virtual environment at the project root:
   - macOS/Linux: `python3 -m venv .venv`
   - Windows (PowerShell): `python -m venv .venv`
2. Activate it:
   - macOS/Linux: `source .venv/bin/activate`
   - Windows: `.\.venv\Scripts\activate`
3. Upgrade pip (optional but recommended): `pip install --upgrade pip`
4. Install deps: `pip install -r requirements.txt`

## Notebook workflow
- Open `notebooks/triton_kernel_starter.ipynb` in JupyterLab/VS Code.
- If CUDA is unavailable locally, the Triton cells will be skipped—focus on editing kernel logic and push to a GPU-enabled machine for validation.

## Repository layout
- `notebooks/` – experimental notebooks; start from `triton_kernel_starter.ipynb`
- `requirements.txt` – runtime and notebook dependencies
- `.gitignore` – ignores local/temporary artifacts (venv, pyc, notebook checkpoints)

## Contributing (team notes)
- Keep notebook outputs trimmed before commits to keep diffs reviewable.
- Document kernel assumptions and any deviations from the original CUDA implementation directly in markdown cells.
- Prefer small, reviewable PRs and add short test/validation notes in descriptions.
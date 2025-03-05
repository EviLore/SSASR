# SSASR - Self-Supervised Attention for Super-Resolution

## Project Overview
This project implements a novel approach to image super-resolution by augmenting the Residual Channel Attention Network (RCAN) with a self-supervised attention mechanism. The proposed method enhances the performance of the base RCAN model by applying learned attention weights to intermediate features, resulting in improved super-resolution quality.

## Key Features
- **Attention-Augmented RCAN**: Extends the RCAN architecture with a multi-head attention mechanism
- **Self-Supervised Learning**: Attention weights are learned without additional supervision
- **Multi-Scale Feature Processing**: Uses three attention heads with different receptive fields
- **Statistically Significant Improvements**: Achieves consistent PSNR gains over the base RCAN model

## Results
The attention-augmented model demonstrates consistent improvements over the base RCAN model:
- Average PSNR improvement of 0.07 dB on the Set14 benchmark
- Statistically significant results (p-value < 0.0001)
- Visual improvements in detail preservation and artifact reduction

## Architecture
The attention mechanism consists of:
- Feature extraction layers that process intermediate RCAN features
- Three attention heads with different receptive fields (3×3, 5×5, and 7×7 convolutions)
- Learnable scaling factors for each attention head
- A base attention parameter that ensures stability

## Implementation Details
- Built on top of the official RCAN implementation
- Freezes the base RCAN weights during training
- Uses PyTorch for model implementation and training
- Evaluated on standard super-resolution benchmarks (Set5, Set14)

## Requirements
- PyTorch
- NumPy
- Matplotlib
- PIL/Pillow
- tqdm
- scipy

## Usage
The main implementation and experiments are contained in the Jupyter notebook. The notebook includes:
- Model implementation
- Dataset preparation
- Training procedures
- Evaluation metrics
- Visualization of results

## Future Work
- Explore different attention mechanisms
- Extend to other super-resolution architectures
- Investigate performance on different upscaling factors
- Apply to video super-resolution

## Author
Tyler Malka

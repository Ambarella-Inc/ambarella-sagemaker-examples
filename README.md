# Ambarella SageMaker Examples

This repository contains end-to-end examples for training and deploying computer vision models on [Ambarella](https://www.ambarella.com/) edge AI platforms using [AWS SageMaker](https://aws.amazon.com/sagemaker/). Each example walks through the full workflow from preparing a dataset and launching a SageMaker training job with Ambarella's Model Preparation Service (AmbaMPS), to running inference both in the cloud via SageMaker endpoints. The examples are organized by algorithm, with each folder corresponding to a supported model architecture.

## Repository Structure

```
ambarella-sagemaker-examples/
├── YOLOX/                  # Megvii YOLOX object detection
├── <algorithm>/            # Future algorithms follow the same layout
└── README.md
```

Each algorithm folder contains:

- **Jupyter notebook** (`demo-<model>-<dataset>-sagemaker.ipynb`) covering:
  - Data preparation
  - SageMaker training via the `ModelTrainer` API
  - Inference via SageMaker real-time endpoints
- **Helper file(s)** (`helpers.py` or similar) with model-specific pre/postprocessing and visualization utilities.

## Available Algorithms

| Algorithm | Source Repo | Task |
|-----------|-------------|------|
| [YOLOX](YOLOX/) | [Megvii-BaseDetection/YOLOX](https://github.com/Megvii-BaseDetection/YOLOX) | Object Detection |

## Prerequisites

1. **AWS CLI** -- Install and run `aws configure` to set up your credentials.
2. **SageMaker Python SDK** -- `pip install sagemaker` ([docs](https://github.com/aws/sagemaker-python-sdk)).
3. **AWS Marketplace subscription** -- Subscribe to the relevant Ambarella algorithm from its product listing page. ([Marketplace](https://aws.amazon.com/marketplace/))
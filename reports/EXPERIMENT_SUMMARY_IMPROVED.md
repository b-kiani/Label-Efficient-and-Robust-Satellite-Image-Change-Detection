# Improved ObjChange-MambaDiff Experiment Summary
Generated: 2026-06-21 18:06:37
Root: `D:\Datasets\Satillate`
Quick run: `False`

## Main benchmark
- **DSIFN-CD** best model: `PretrainedResNetSiamese` with F1=0.9125, IoU=0.8439, threshold=0.55
- **LEVIR-CD** best model: `ObjChangeMambaDiffLiteV2` with F1=0.7760, IoU=0.6588, threshold=0.55
- **S2Looking** best model: `PretrainedResNetSiamese` with F1=0.4409, IoU=0.2933, threshold=0.70
- **xView2** best model: `ObjChangeMambaDiffLiteV2` with F1=0.6281, IoU=0.4713, threshold=0.50

## Label efficiency
- **DSIFN-CD ObjChangeMambaDiffLiteV2 F1 by fraction**: 0.01: 0.654, 0.05: 0.708, 0.1: 0.736, 0.25: 0.758, 0.5: 0.794, 1: 0.815
- **LEVIR-CD ObjChangeMambaDiffLiteV2 F1 by fraction**: 0.01: 0.095, 0.05: 0.525, 0.1: 0.569, 0.25: 0.640, 0.5: 0.726, 1: 0.763
- **S2Looking ObjChangeMambaDiffLiteV2 F1 by fraction**: 0.01: 0.204, 0.05: 0.227, 0.1: 0.233, 0.25: 0.287, 0.5: 0.317, 1: 0.380

## Cross-dataset generalisation
- `ObjChangeMambaDiffLiteV2` trained on **LEVIR-CD** tested on **S2Looking**: F1=0.0195, IoU=0.0105
- `PretrainedResNetSiamese` trained on **LEVIR-CD** tested on **S2Looking**: F1=0.0064, IoU=0.0034
- `SiameseUNet` trained on **LEVIR-CD** tested on **S2Looking**: F1=0.0068, IoU=0.0036
- `ObjChangeMambaDiffLiteV2` trained on **S2Looking** tested on **LEVIR-CD**: F1=0.2401, IoU=0.1420
- `PretrainedResNetSiamese` trained on **S2Looking** tested on **LEVIR-CD**: F1=0.0000, IoU=0.0000
- `SiameseUNet` trained on **S2Looking** tested on **LEVIR-CD**: F1=0.2478, IoU=0.1485

## Ablation
- `ObjChangeMambaDiffLiteV2`: F1=0.7631, IoU=0.6417
- `Obj_no_mamba`: F1=0.7542, IoU=0.6268
- `Obj_no_object`: F1=0.7472, IoU=0.6193
- `Obj_no_object_no_mamba`: F1=0.7463, IoU=0.6186
- `PretrainedResNetSiamese`: F1=0.7262, IoU=0.5940
- `SiameseUNet`: F1=0.7232, IoU=0.5892

## Data quality notes
- No extreme mask-distribution warning was triggered by the quick sanity check.

# Data Preparation

We provide some tips for XRNerf data preparation in this file.

<!-- TOC -->

- [Data Preparation](#data-preparation)
  - [Getting Data](#getting-data)
      - [Dataset Organization](#dataset-organization)
      - [Dataset Download](#dataset-download)

<!-- TOC -->

## Getting Data

#### Dataset Organization
It is recommended to symlink the dataset root to $PROJECT/data. If your folder structure is different, you may need to change the corresponding paths in config files.

```
xrnerf
├── xrnerf
├── docs
├── configs
├── test
├── extensions
├── data
│   ├── nerf_llff_data
│   ├── nerf_synthetic
│   ├── multiscale
│   ├── ...
```

#### Dataset Download
1. Download ```nerf_llff_data``` and ```nerf_llff_data``` from [here](https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1), and put it under ```xrnerf/data```
2. Credit to NSVF authors for providing [their datasets](https://github.com/facebookresearch/NSVF), read introductions [here](https://github.com/creiser/kilonerf#download-nsvf-datasets)
3. For mip-nerf training, you can generate the multiscale dataset used in the paper by running the following command, ```python tools/convert_blender_data.py --blenderdir /data/nerf_synthetic --outdir data/multiscale```
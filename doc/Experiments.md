## Summary 2022/06/06
* Naive N-mono performs similar error to one-mono.
* for N-mono, obs can only be observed on cam0.

## TODO
- [ ] look into obervations handling in VIO (for non-overlaping cameras)
- [ ] figure out spatial tracking/matching for non-parallel stereo

### Euroc Stereo (FrameToFrameOpticalFlow)
* error 0.0720209
```bash
./basalt_vio --dataset-path ../data/euroc_data/MH_01_easy/ --cam-calib ../data/euroc_ds_calib.json --dataset-type euroc --config-path ../data/euroc_config.json --marg-data euroc_marg_data --show-gui 1
```

### Euroc Mono Cam0 (FrameToFrameOpticalFlow)
* error 0.112339
```bash
./basalt_vio --dataset-path ../data/euroc_data/MH_01_easy/ --cam-calib ../data/euroc_ds_calib_mono.json --dataset-type euroc_mono --config-path ../data/euroc_config.json --marg-data euroc_marg_data --show-gui 1
```

### Euroc Mono Cam0 (FrameToFrameMonoOpticalFlow)
* error 0.112374
```bash
./basalt_vio --dataset-path ../data/euroc_data/MH_01_easy/ --cam-calib ../data/euroc_ds_calib_mono.json --dataset-type euroc_mono --config-path ../data/euroc_config_mono.json --marg-data euroc_marg_data --show-gui 1
```

### Euroc two Mono Cam0 + Cam1 (FrameToFrameMonoOpticalFlow)
* error 0.112452
```bash
./basalt_vio --dataset-path ../data/euroc_data/MH_01_easy/ --cam-calib ../data/euroc_ds_calib.json --dataset-type euroc --config-path ../data/euroc_config_mono.json --marg-data euroc_marg_data --show-gui 1
```
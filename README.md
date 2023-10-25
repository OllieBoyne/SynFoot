# SynFoot

Synthetic foot datasets used for foot prediction tasks.

Data was produced using our [BlenderSynth](https://ollieboyne.github.io/BlenderSynth) package.

As used in our paper [FOUND](https://ollieboyne.github.io/FOUND).

## Install

[Installation instructions coming soon]

v1: [Download link coming soon]

As used in [FOUND](https://github.com/OllieBoyne/FOUND) - 50K, RGB, Normal, Masks

## Data format

We provide folders with different data types. As new versions of the dataset are released, they may have different formats available.

| Data type | Description                                                        |
|-----------|--------------------------------------------------------------------|
| `rgb`     | RGB images                                                         |
| `mask`    | Binary mask of foot                                                |
| `normals` | Predicted normals [(more info)](#normal-format)                    |
| `labels`  | JSON files with additional information [(more info)](#json-format) |

### Normal format

Our normals are formatted in a *camera* relative reference frame, with RGB corresponding to XYZ, normalized in 0-255,
such that (0, 1, 0) -> (128, 255, 128).

In our format, (XYZ) = (left, up, back)

### JSON format

We provide preliminary data that might be useful in our `labels.json`

```yaml
{
  "camera" : {
    "pos": [0, 0, 0], # world camera position
    "rot": [0, 0, 0], # world camera rotation (euler, radians)
    "fov": 60.0 # camera field of view (degrees)
  },
  
  "foot" : {
      "name": "0009-A" # Foot3D scan used   
  },
  
  "keypoints" : {
      "big toe": [0, 0], # pixel coordinates
      ...
  }
}
```

Keypoints available are: `['big toe', '2nd toe', '3rd toe', '4th toe', 'little toe', 'heel', 'outer extrema', 'inner extrema']`


### Citation

If you use our work, please cite:

```
@inproceedings{boyne2023found,
            title={FOUND: {F}oot {O}ptimisation with {U}ncertain {N}ormals for Surface {D}eformation using Synthetic Data},
            author={Boyne, Oliver, and Bae, Gwangbin, and Charles, James and Cipolla, Roberto},
            booktitle={Winter Conference on Applications of Computer Vision (WACV)},
            year={2024}
}
```
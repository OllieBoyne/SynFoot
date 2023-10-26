# V1

We provide folders with different data types. As new versions of the dataset are released, they may have different formats available.

| Data type | Description                                                        |
|-----------|--------------------------------------------------------------------|
| `rgb`     | RGB images                                                         |
| `mask`    | Binary mask of foot                                                |
| `normals` | Predicted normals                                                  |
| `labels`  | JSON files with additional information [(more info)](#json-format) |


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


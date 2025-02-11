# V2

This version was produced for the paper [FOCUS](https://www.ollieboyne.com/FOCUS/).

| Data type | Description                                                        |
|-----------|--------------------------------------------------------------------|
| `rgb`     | RGB images                                                         |
| `mask`    | Binary mask of foot                                                |
| `normals` | Predicted normals                                                  |
| `labels`  | JSON files with additional information [(more info)](#json-format) |
| `TOC` | Dense correspondences as described in FOCUS |

### JSON format

We provide preliminary data that might be useful in our `labels.json`

```yaml
{  
  "foot-id" : "0009-A", # Foot3D scan used
  "camera_position" : [0, 0, 0], # world camera position
  "camera_look_at" : [0, 0, 0], # world camera look at position
  
  "foot_poses" : {
      "Dorsiflextion": 0.0,
      ...
    }, # degrees used of our available pose deformations
  
  "foot_shape" : {
      "Length": 1.0,
      ...
  }, # selected parameters of our available shape deformations
  
  "lighting" : {
        ...
  }, # details of HDRI & point light setup

  "floor_material" : {
      ...
  } # details of floor material

}

```
<p align="center">
  <img width=70% src="https://ollieboyne.github.io/FOUND/images/logos/synfoot_v1.png">
</p>

# SynFoot


![](https://img.shields.io/endpoint?url=https%3A%2F%2Fscript.google.com%2Fmacros%2Fs%2FAKfycbyRdZfs9jmLEnq_cmwsLwkd_L3R9JroevQqD-duufVXgplUDRJu-dXfSnvaSqYsQxsoaA%2Fexec
)

Synthetic foot datasets used for foot prediction tasks.

Data was produced using our [BlenderSynth](https://ollieboyne.github.io/BlenderSynth) package.

As used in our paper [FOUND](https://ollieboyne.github.io/FOUND).

## Install

| Dataset | Description               | Download Link                                   | Readme                 |
|---------|---------------------------|-------------------------------------------------|------------------------|
| V1      | 50K RGB + Normals + Masks | [Download](https://forms.gle/jZqoLPfQrkEa5XUF8) | [readme](v1_layout.md) |

### Normal format

Our normals are formatted in a *camera* relative reference frame, with RGB corresponding to XYZ, normalized in 0-255,
such that (0, 1, 0) -> (128, 255, 128).

In our format, (XYZ) = (left, up, back)


### Citation

If you use our work, please cite:

```
@inproceedings{boyne2024found,
            title={FOUND: {F}oot {O}ptimisation with {U}ncertain {N}ormals for Surface {D}eformation using Synthetic Data},
            author={Boyne, Oliver, and Bae, Gwangbin, and Charles, James and Cipolla, Roberto},
            booktitle={Winter Conference on Applications of Computer Vision (WACV)},
            year={2024}
}
```
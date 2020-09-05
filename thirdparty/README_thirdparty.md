# Thirdparty software

Here, we provide a script to extract NetVLAD descriptors using an existing open-source [TensorFlow implementation](https://github.com/uzh-rpg/netvlad_tf_open/tree/abe37fe9d656bf781cff32caf738efca525b7889) of the [original MATLAB source code](https://github.com/Relja/netvlad).

Please refer to and cite the original sources if using them in your work.

## Usage
For descriptor extraction, it is assumed that you have followed the instructions from the [TensorFlow implementation](https://github.com/uzh-rpg/netvlad_tf_open/tree/abe37fe9d656bf781cff32caf738efca525b7889) for setting up the python environment and have downloaded the checkpoint in the `./netvlad_tf_open/checkpoints/`
 
```python
python extract_netvlad.py -i <path_to_image_dir>
```
Optionally, you can pass the batchSize with `-b` and output directory with `-o`.

Output is stored as an `NxD` array in `.npy` format where `N` is the number of images (names sorted before reading) and `D` is the descriptor dimension (4096 in this case).
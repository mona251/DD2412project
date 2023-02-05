## `dog{xxx}.npz` files
The files are in `numpy` format. They contain the image, and features
from blocks 1, 2, 3, 4.

To **load**, do:

```python
loaded = np.load('data/dog000.npz')
image = loaded['image']
b1 = loaded['b1']
b2 = loaded['b2']
b3 = loaded['b3']
b4 = loaded['b4']
```

for i, (img, blocks) in enumerate(imgs_blocks):
    fname = f'./data/dog{i:0>3}.npz'
    print(f"Saving to: {fname}")
    print("Dims are: ")
    for b in blocks:
        print(b.shape)
    np.savez_compressed(fname, image=img, 
                        b1=blocks[0], 
                        b2=blocks[1], b3=blocks[2], b4=blocks[3])
```

The current dogs images come from the val set of https://drive.google.com/drive/folders/1Ycq9ZU7I1tIavli_aoV-nayMIhkYlovG.

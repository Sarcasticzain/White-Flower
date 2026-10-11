# White Flower Animation

A beautiful interactive white flower animation built with Python, Pygame, NumPy,
and Pillow. The flower gently breathes, glows in the dark, reflects in rippling
water, and releases tiny floating lights from its petals.

## Features

- Soft breathing glow effect

- Rippling water reflection

- Floating light particles from the flower

- Twinkling background sparkles

- Smooth animated zoom effect

- Screenshot support

- Custom flower image support

## Project Files

- `White Flower.py` – the main animation program

- `flower.jpg` – the flower image used by the animation

- `white_flower_shot.png` – screenshot created when you press **S**

## Requirements

- Python 3.9 or newer

- Pygame Community Edition

- NumPy

- Pillow

## Installation

Open a terminal inside the `White-Flower` folder and run:

```bash
python -m pip install --upgrade pip
python -m pip install pygame-ce numpy pillow
```

> Use `pygame-ce` instead of `pygame`. It works more reliably with newer Python
versions, especially on Windows.

## How to Run

Open a terminal in the folder that contains `White Flower.py`, then run:

```bash
python "White Flower.py"
```

### Controls

- Press **ESC** to close the animation

- Press **S** to save a screenshot

## Use Your Own Flower Image

You can replace the default image with your own flower photograph:

1. Choose a JPG or PNG flower image. A portrait image with a dark background
usually gives the best result.

1. Rename the image to `flower.jpg`.

1. Place it in the same folder as `White Flower.py`.

1. Replace the existing `flower.jpg` file.

1. Run the program again.

For a PNG image, update this line in `White Flower.py`:

```python
im = Image.open("flower.jpg").convert("RGB")
```

Change it to:

```python
im = Image.open("flower.png").convert("RGB")
```

Bright backgrounds may reduce the glow effect. Dark or black backgrounds make
the white flower and floating lights stand out more clearly.

## Customization

You can adjust these settings near the top of `White Flower.py`:

| Setting | What it changes |
| --- | --- |
| `IMG_H = 760` | Flower height and window size |
| `N = 3500` | Number of floating light particles |
| `WATER_Y0` | Position where the water reflection begins |
| `0.14 + 0.12 * math.sin(...)` | Strength of the breathing glow |
| `3.2 * np.sin(...)` | Size of the water ripples |
| `pygame.display.set_caption(...)` | Animation window title |

For a faster animation on a slower computer, reduce these values:

```python
IMG_H = 600
N = 1500
```

## Troubleshooting

### `ModuleNotFoundError`

Install the required packages again:

```bash
python -m pip install pygame-ce numpy pillow
```

### `FileNotFoundError: flower.jpg`

Make sure `flower.jpg` is in the same folder as `White Flower.py`, and run the
command from that folder.

### The animation is choppy

Lower the image height and particle count:

```python
IMG_H = 600
N = 1500
```

### The window is too tall

Reduce `IMG_H` to `600` or `500`.

## License

The source code in this project is available under the [MIT License](LICENSE).
You are free to use, copy, modify, and share the code, as long as the license
notice is included.

The `flower.jpg` image may have separate copyright or usage rules. Only upload
an image that you created yourself, have permission to use, or downloaded from
a source that allows redistribution.
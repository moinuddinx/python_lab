# OpenCV Workspace

A collection of computer vision projects using OpenCV and Python.

## Projects

### 01_image_blender

**Location:** `image_blender/01_image_blender.ipynb`

An advanced image blending system that overlays a smaller image (foreground) onto a larger image (background) using mask-based blending techniques.

#### Features

- Automatic mask generation from grayscale conversion
- Precise image alignment with pixel-level offsets
- Seamless blending using bitwise operations
- Modular, reusable function architecture
- Support for any image size and position

#### Usage

Simply provide:

- Background image path
- Foreground image path
- Y-axis offset (vertical position in pixels)
- X-axis offset (horizontal position in pixels)

The rest is handled automatically by the `blend_and_display()` function.

#### Key Functions

- `load_images()` - Load and convert images to RGB
- `create_mask()` - Generate inverted binary mask from foreground
- `extract_regions()` - Extract background and foreground using masks
- `blend_images()` - Perform blending and composition
- `blend_and_display()` - Main orchestration function with visualization

#### How It Works

1. Load background and foreground images
2. Create an inverted mask from the foreground (white = opaque, black = transparent)
3. Extract background regions where mask is white
4. Extract foreground regions where mask is black
5. Add the two regions together for seamless blending
6. Compose the blended ROI back onto the original background image

---

## Data Directory Structure

```
data/
├── images/
│   ├── image1.png    (background/large image)
│   └── image3.png    (foreground/overlay image)
```

## Requirements

- Python 3.9+
- OpenCV (cv2)
- NumPy
- Matplotlib

## Installation

```bash
pip install opencv-python numpy matplotlib
```

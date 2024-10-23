# License Plate Detection Using YOLO V8

## Overview

This project implements a License Plate Detection system using the YOLO (You Only Look Once) V8 architecture. The goal is to accurately detect and localize vehicle license plates in images and videos, enabling further processing such as character recognition or vehicle identification.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Training](#training)
- [Evaluation](#evaluation)
- [Contributing](#contributing)
- [License](#license)

## Features

- Real-time license plate detection
- High accuracy with YOLO V8 model
- Supports both image and video input
- Easy integration with OCR for character recognition

## Requirements

- Python 3.7+
- PyTorch 1.8+
- OpenCV
- NumPy
- Matplotlib
- YOLO V8 weights and configuration files

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/License-Plate-Detection-using-YOLO-V8.git
   cd License-Plate-Detection-using-YOLO-V8
   ```

2. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the YOLO V8 weights and place them in the `weights/` directory.

## Usage

To run the license plate detection on an image:

```bash
python detect.py --image path/to/image.jpg
```

To run the detection on a video:

```bash
python detect.py --video path/to/video.mp4
```

### Command-Line Arguments

- `--image`: Path to the input image.
- `--video`: Path to the input video.
- `--output`: Path to save the output image/video with detected license plates.

## Training

To train the YOLO V8 model on a custom dataset, follow these steps:

1. Prepare your dataset in the YOLO format.
2. Update the configuration file (`config.yaml`) with your dataset details.
3. Start the training process:

   ```bash
   python train.py --config config.yaml
   ```

## Evaluation

After training, you can evaluate the model's performance using:

```bash
python evaluate.py --weights path/to/weights.pt --data path/to/data.yaml
```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your enhancements or bug fixes. Make sure to follow the code style and include tests for new features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
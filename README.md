# Image Colorization with Deep Learning

This project aims to colorize black and white images using deep learning techniques. It leverages a pre-trained convolutional neural network (CNN) to predict the color channels (ab) of grayscale images based on their luminance (L) channel. The model used in this project is based on the Colorization using Optimization approach.

## Overview

The colorization process involves the following steps:

1. Pre-processing: Convert the input black and white image to grayscale and then to LAB color space.
2. Colorization Model: Load a pre-trained CNN model for predicting the ab channels of the LAB image.
3. Post-processing: Combine the original luminance channel (L) with the predicted ab channels to obtain the colorized image.
4. Display: Show the original black and white image alongside its colorized version.

## Getting Started

### Installation

To run the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/athish-ns/colorize.git
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Make sure to download the pre-trained data from this location. At 125 MB it's too large to put into the GitHub. Place the file in the same directory.

https://www.dropbox.com/s/dx0qvhhp5hbcx7z/colorization_release_v2.caffemodel?dl=1


### Usage

1. Run the Streamlit app:

   ```bash
   streamlit run app.py
   ```

2. Upload a black and white image (in JPG or PNG format) using the file uploader in the sidebar.
3. The app will display the original image and its colorized version.

### Model Files

Make sure to include the following model files in your project directory:

- `models_colorization_deploy_v2.prototxt`: Model architecture file.
- `colorization_release_v2.caffemodel`: Pre-trained weights file.
- `pts_in_hull.npy`: Cluster center points file.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

# Workshop 3: Canny Edge Detection
# Name: Sowmiya R
# Register Number: 212225040420

## AIM

To detect edges in an image using Python and OpenCV by converting the image to grayscale, applying Gaussian blur to reduce noise, and using the Canny edge detection algorithm to identify object boundaries.

## SOFTWARE REQUIRED

- Python
- OpenCV
- Matplotlib
- Jupyter Notebook
- Anaconda (optional)

## INSTALLATION

Install the required libraries using the following command:

```bash
pip install opencv-contrib-python-headless matplotlib
```

## ALGORITHM

### Step 1: Import Libraries
- Import OpenCV for image processing.
- Import Matplotlib for displaying images.

### Step 2: Read the Image
- Load the input image `Mine.jpeg` using `cv2.imread()`.
- Convert the image to grayscale using `cv2.IMREAD_GRAYSCALE`.

### Step 3: Apply Gaussian Blur
- Apply Gaussian blur to the grayscale image using `cv2.GaussianBlur()`.
- Use a kernel size of 5 × 5 to reduce noise and unnecessary details.

### Step 4: Perform Canny Edge Detection
- Apply the Canny edge detection algorithm using `cv2.Canny()`.
- Set the lower threshold to 50 and the upper threshold to 150.
- Detect edges and boundaries in the image.

### Step 5: Display the Results
- Create a figure using Matplotlib.
- Display the original grayscale image.
- Display the detected edges.
- Add titles and remove axis labels for clear visualization.

## PROGRAM

```python
import cv2
import matplotlib.pyplot as plt

# Read the image in grayscale
img = cv2.imread('Mine.jpeg', cv2.IMREAD_GRAYSCALE)

# Apply Gaussian blur
blurred = cv2.GaussianBlur(img, (5, 5), 0)

# Detect edges using Canny
edges = cv2.Canny(blurred, 50, 150)

# Display original image and detected edges
plt.figure(figsize=(10, 5))

plt.subplot(121)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(122)
plt.imshow(edges, cmap='gray')
plt.title('Detected Edges')
plt.axis('off')

plt.show()
```

## OUTPUT

##  Original image and detected edges displayed side by side
<img width="1016" height="453" alt="image" src="https://github.com/user-attachments/assets/7c61c105-c412-4f22-a8d5-17f04288e8b7" />


## RESULT

Thus, edge detection was successfully performed using Python, OpenCV, and Matplotlib. Gaussian blur was used to reduce image noise, and the Canny edge detection algorithm identified the edges and boundaries of objects in the image.

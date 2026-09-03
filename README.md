# Image-Segmentation-Using-Thresholding-Techniques-in-OpenCV


## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program
## Developed By

**Name:** Pugazh sozhan.A

**Register No:** 212224240121

## Output

### Original Grayscale Image

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("image8.JPEG")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```


<img width="515" height="370" alt="download" src="https://github.com/user-attachments/assets/2a699710-6ec4-491c-9aef-b89820f00f9f" />

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("image8.JPEG", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```


<img width="515" height="370" alt="download" src="https://github.com/user-attachments/assets/9a2c9cd2-9b05-49a6-9b9d-f304ec7cfdbe" />


```


import cv2
import matplotlib.pyplot as plt
img = cv2.imread("image8.JPEG", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```

<img width="515" height="370" alt="download" src="https://github.com/user-attachments/assets/1545295b-446e-4b9d-83d7-104a475a38f8" />

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("image8.JPEG", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()

```

<img width="515" height="370" alt="download" src="https://github.com/user-attachments/assets/2315e702-413f-4bc2-8443-8cac11ec9211" />


```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("image8.JPEG", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```

<img width="515" height="370" alt="download" src="https://github.com/user-attachments/assets/e0ba74ae-3f64-4162-a19e-8080252da6c2" />

## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 























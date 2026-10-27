import cv2
import numpy as np
from google.colab.patches import cv2_imshow
img = np.ones((300, 300, 3), dtype=np.uint8) * 50
cv2.circle(img, (150, 150), 80, (0, 255, 255), -1)  # Draw a yellow circle
cv2.rectangle(img, (50, 50), (100, 100), (0, 0, 255), -1)  # Draw a red square
ksize = (15, 15)
blur = cv2.GaussianBlur(img, ksize, 0)
print("Original Image:")
cv2_imshow(img)
print("Gaussian Blur Image:")
cv2_imshow(blur)

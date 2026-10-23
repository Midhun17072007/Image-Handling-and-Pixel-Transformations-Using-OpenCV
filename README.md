# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** MIDHUN S 
- **Register Number:** 212224230158

  ### Ex. No. 01

1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```PYTHON
import cv2
import matplotlib.pyplot as plt
```

Read the image using OpenCV
```
img = cv2.imread('VIN.jpeg', cv2.IMREAD_COLOR)
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)#
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Display the image using Matplotlib
```
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
```
Draw a line from top-left to bottom-right
```
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jepg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
(1536, 941, 3)
```
Draw a rectangle around the Whole image
```
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Add text to the image
```
text_img = cv2.putText(img_rgb, "Opencv Drawing", (10, 35), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```



## Output:

## original image
- <img width="650" height="373" alt="image" src="https://github.com/user-attachments/assets/00b600c7-e17f-4326-ae63-92540e131151" />

## Image with Line
<img width="605" height="366" alt="image" src="https://github.com/user-attachments/assets/d11ed377-a61b-4f9a-b029-d2eae60a829f" />

## Image with Circle
<img width="772" height="363" alt="image" src="https://github.com/user-attachments/assets/5febc3a7-9412-4525-86dd-4fa6ad8feb35" />

## Image with Rectangle
<img width="610" height="363" alt="image" src="https://github.com/user-attachments/assets/215f92a4-e492-49e3-aa93-08f0dbfa65d6" />

## Image with Text
<img width="585" height="368" alt="image" src="https://github.com/user-attachments/assets/d11437ab-182c-4f67-9564-76b7ba91d569" />

## Original RGB Image
<img width="625" height="337" alt="image" src="https://github.com/user-attachments/assets/0c7a15cf-f2a2-4b1f-a9a4-e3c4ea18eab1" />

## HSV Image
<img width="620" height="353" alt="image" src="https://github.com/user-attachments/assets/d046e489-32f4-480f-a672-26cd14a34033" />

## Grayscale Image
<img width="593" height="362" alt="image" src="https://github.com/user-attachments/assets/32491383-3787-47b9-8946-58a1b3b540f1" />

## HSV to RGB Image
<img width="598" height="397" alt="image" src="https://github.com/user-attachments/assets/00a335ab-5e57-45b9-9fb2-34132377fa3c" />

## Image with 300x300 White Block
<img width="572" height="352" alt="image" src="https://github.com/user-attachments/assets/69f0f494-c944-4a7d-82b9-71865ad7c35b" />

## Resized Image (Half Size)
<img width="630" height="462" alt="image" src="https://github.com/user-attachments/assets/8ccbad8c-264f-4cdb-a4ad-788b2d3dfd32" />

## Cropped Region of Interest (ROI)
<img width="443" height="461" alt="image" src="https://github.com/user-attachments/assets/ec626a0b-9d89-487f-8833-aabf1394f45d" />

## Flipped Horizontally
<img width="576" height="357" alt="image" src="https://github.com/user-attachments/assets/50fbc331-5e80-4d8b-a42f-8f25e2d6b78e" />

## Flipped Vertically
<img width="582" height="345" alt="image" src="https://github.com/user-attachments/assets/28f13c57-27d4-47fc-83a9-76e867bd6a95" />


## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.


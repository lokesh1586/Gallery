# Ex.08 Design of Interactive Image Gallery
# Date:
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Image Gallery</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: url('batman.webp') no-repeat center center/cover;
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      position: relative;
    }

    h1 {
      position: absolute;
      top: 7px;
      left: 10px;
      font-size: 1.2em;
      text-shadow: 2px 2px 4px black;
      font-weight: normal; 
    }

    
    .gallery-container {
      position: absolute;
      top: 300px; 
      width: 20px;  
      height: 20px; 
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .gallery-container img {
      position: absolute;
      width: 150px; 
      height: 150px;
      object-fit: cover;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .gallery-container img:hover {
      transform: scale(1.05); 
    }

    #modal {
      display: none;
      position: fixed;
      z-index: 1000;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
    }

    #modal img {
      margin: auto;
      display: block;
      max-width: 80%;
      max-height: 80%;
      position: relative;
      top: 10%;
    }

    #close {
      position: absolute;
      top: 20px;
      right: 30px;
      color: white;
      font-size: 2em;
      cursor: pointer;
    }

    footer {
      position: fixed;
      bottom: 10px;
      right: 10px;
      color: #ddd;
      font-size: 1em;
    }

    footer a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
    }

    footer a:hover {
      color: #00c3ff;
    }
  </style>
</head>
<body>

  <h1>Image Gallery</h1>

  <div class="gallery-container">
    <img src="jk.jpg" alt="Image 1" onclick="openModal(this)" style="transform: rotate(0deg) translateY(-190px);">
    <img src="tf.jpg" alt="Image 2" onclick="openModal(this)" style="transform: rotate(46.5deg) translateY(-285px);">
    <img src="deads.jpg" alt="Image 3" onclick="openModal(this)" style="transform: rotate(90deg) translateY(-498px);">
    <img src="peng.jpg" alt="Image 4" onclick="openModal(this)" style="transform: rotate(135deg) translateY(-400px);">
    <img src="bane.jpg" alt="Image 5" onclick="openModal(this)" style="transform: rotate(180deg) translateY(-390px);">
    <img src="ras.jpg" alt="Image 6" onclick="openModal(this)" style="transform: rotate(225deg) translateY(-400px);">
    <img src="death.jpg" alt="Image 7" onclick="openModal(this)" style="transform: rotate(270deg) translateY(-500px);">
    <img src="rid.jpg" alt="Image 8" onclick="openModal(this)" style="transform: rotate(315deg) translateY(-290px);">
  </div>

  <div id="modal">
    <span id="close" onclick="closeModal()">&#10006;</span>
    <img id="modalImage" src="" alt="Expanded View">
  </div>

  <footer>
    <p>Designed by: Sanjit A (212224220087)</p>
  </footer>

  <script>
    function openModal(image) {
      const modal = document.getElementById("modal");
      const modalImage = document.getElementById("modalImage");
      modal.style.display = "block";
      modalImage.src = image.src;
    }

    function closeModal() {
      document.getElementById("modal").style.display = "none";
    }
  </script>

</body>
</html>

````
# OUTPUT:
![Screenshot 2025-05-09 092938](https://github.com/user-attachments/assets/a7f5f735-f506-43ff-8140-5faef0bd94d5)
![Screenshot 2025-05-09 093047](https://github.com/user-attachments/assets/eb777d07-cc84-4e4e-aab7-2d62a4f4fa54)
![Screenshot 2025-05-09 093059](https://github.com/user-attachments/assets/2c32f65d-1eb2-4ec8-947a-075bd7e3af96)
![Screenshot 2025-05-09 093112](https://github.com/user-attachments/assets/5ef02713-1991-42e7-92a6-4169f2965503)
![Screenshot 2025-05-09 093122](https://github.com/user-attachments/assets/5a0d0f5a-e934-40aa-a79e-0b6767d7ef2f)
![Screenshot 2025-05-09 093134](https://github.com/user-attachments/assets/f3fa22c2-56a1-4d17-8e8e-61f7ed1575a1)
![Screenshot 2025-05-09 093231](https://github.com/user-attachments/assets/819f986d-a85d-4cda-bc36-e030ef3437d1)
![Screenshot 2025-05-09 093243](https://github.com/user-attachments/assets/610b334e-215c-4635-8bae-ed8c336f1402)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.

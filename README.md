# Ex.08 Design of Interactive Image Gallery
## Date: 14/05/2025

```
Developed by: Aman Singh
Reg no. 212224040020
```
## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MY GALLERY</title>
  <style>
    html, body {
        height: 100%;
        margin: 0;
        display: flex;
        flex-direction: column;
    }

    .gallery-container {
        flex: 1;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        padding: 20px;
        justify-content: center;
        text-align: center;
        align-items: center;
    }

    .gallery-item {
      width: 200px;
      height: 150px;
      overflow: hidden;
      cursor: pointer;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(12, 215, 93, 0.1);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.1);
    }

    .lightbox {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }

    .lightbox-image {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(223, 123, 8, 0.252);
    }

    .close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 30px;
      color: #fff;
      cursor: pointer;
      z-index: 1001;
    }

    .close:hover {
      color: #ff6b6b;
    }

    .footer {
        text-align: center;
        background-color: #fdd9b5; /* Softer than bisque */
        color: black;
        font-size: 20px;
        padding: 15px;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
  </style>
</head>
<body style="align-items: center;">
  <h1>Interactive Image Gallery- The valour of Indian Armed forces</h1>
  <div class="gallery-container">
    <div class="gallery-item">
      <img src="afs.jpg" alt="Image 1" />
    </div>
    <div class="gallery-item">
      <img src="airf.jpg" alt="Image 2" />
    </div>
    <div class="gallery-item">
      <img src="army.jpeg" alt="Image 3" />
    </div>
    <div class="gallery-item">
      <img src="ins.jpg" alt="Image 4" />
    </div>
    <div class="gallery-item">
      <img src="navy.jpg" alt="Image 5" />
    </div>
    <div class="gallery-item">
      <img src="tanks.jpg" alt="Image 6" />
    </div>
  </div>

  <div class="lightbox">
    <span class="close">&times;</span>
    <img class="lightbox-image" src="" alt="Enlarged Image" />
  </div>

  <div class="footer">
    <footer>
      Designed by Aman Singh (212224040020)
    </footer>
  </div>

  <script>
    // Execute script immediately instead of waiting for DOMContentLoaded
    (function() {
      const galleryItems = document.querySelectorAll('.gallery-item img');
      const lightbox = document.querySelector('.lightbox');
      const lightboxImage = document.querySelector('.lightbox-image');
      const closeBtn = document.querySelector('.close');

      // Add click event to each gallery image
      galleryItems.forEach(item => {
        item.addEventListener('click', function() {
          lightboxImage.src = this.src;
          lightbox.style.display = 'flex';
        });
      });

      // Close lightbox when clicking the close button
      closeBtn.addEventListener('click', function() {
        lightbox.style.display = 'none';
      });

      // Close lightbox when clicking outside the image
      lightbox.addEventListener('click', function(e) {
        if (e.target === lightbox) {
          lightbox.style.display = 'none';
        }
      });
    })();
  </script>
</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot (1930).png>)
<br>
![alt text](<Screenshot (1931).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.

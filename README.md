# Ex.07 Design of Interactive Image Gallery
## Date:13-11-2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Photo Gallery</title>
  <style>
    body{
        background-color: bisque;
    }
    #image {
      background-image: url('');
      background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    background-color: #333;


      background-position: center;
      width: 700px;
      height: 450px;
      border: 2px solid black;
      text-align: center;
      line-height: 300px;
      font-size: 18px;
      color: white;
      font-weight: bold;
    }

    img {
    width: 160px;                     
      height: 120px;                     
      border: 3px solid #2b1313;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.2s, border-color 0.2s;

    }
  </style>
</head>
<body>
    <center><h1>Marvel Superheroes Photo Gallery</h1>
  <div id="image">Hover over an image below to display here.</div>

  <div id="gallery">
    <img src="thor.jpeg" alt="THOR" onmouseover="upDate(this)" onmouseout="undo()">
    <img src="iron.jpg" alt="IRONMAN" onmouseover="upDate(this)" onmouseout="undo()">
    <img src="doctor.jpeg" alt="DOCTOR STRANGE" onmouseover="upDate(this)" onmouseout="undo()">
    <img src="spider.jpg" alt="SPIDERMAN" onmouseover="upDate(this)" onmouseout="undo()">
    <img src="panther.jpg" alt="BLACK PANTHER" onmouseover="upDate(this)" onmouseout="undo()">
  </div>

  <script>
    function upDate(previewPic) {
      // Step 1: check event
      console.log("Event triggered!");
      console.log("Alt text:", previewPic.alt);
      console.log("Source:", previewPic.src);

      // Step 2: get target div
      const imageDiv = document.getElementById('image');

      // Step 3: change background image and text
      imageDiv.style.backgroundImage = `url('${previewPic.src}')`;
      imageDiv.innerHTML = previewPic.alt;
    }

    function undo() {
      console.log("Undo triggered!");
      const imageDiv = document.getElementById('image');

      // Step 4: restore original values
      imageDiv.style.backgroundImage = "url('')";
      imageDiv.innerHTML = "Hover over an image below to display here.";
    }
  </script>
    </center>
</body>
</html>



```

## OUTPUT:

<img width="1919" height="1080" alt="image" src="https://github.com/user-attachments/assets/f274f28f-5a9a-4fdf-8b82-03036465048a" />



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.

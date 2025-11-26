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
    <style>
        h1{
            color: antiquewhite;
            text-shadow: 0 0 10px purple, 0 0 20px purple, 0 0 30px purple;
            position: relative;
            bottom: 27px;
            font-family: Verdana, Geneva, Tahoma, sans-serif;
            font-size: 50px;
        }
        html{
            background-color: black;
        }
        body{
            background: radial-gradient(purple,black);
            border: 2px solid black;
            border-radius: 50px;
            height: 850px;
            width: 1515px;
        }
        .main {
            background-color: black;
            height: 80%;
            width: 68%;
            border: 2px solid black;
            border-radius: 20px;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            position: absolute;
            top: 50%;
            left: 50%;
            translate: -50% -50%;
        }

        .m1 {
            border-radius: 20px;
            background-color: rgb(44, 4, 44);
            margin: 10px;
            height: 650px;
            width: 1000px;
            display: flex;
            flex-wrap: wrap;
            overflow: scroll;
            justify-content: space-around;
            align-items: center;
            transition: all 1.5s ease;
        }
        .m1::-webkit-scrollbar {
            width: 0px; 
            height: 0px; 
        }
        .m2{
            position: absolute;
            top: 50%;
            right: 10px;
            margin: 10px;
            opacity: 0;
            width: 0px;
            height: 0px;
            transition: all 1.5s ease, opacity 0.4s;
            visibility: hidden;
        }

        img {
            margin: 10px;
            width: 300px;
            height: 300px;
            transition: transform 0.5s ease;
            cursor: pointer;
        }
        #i{
            border-radius: 10px;
        }
        #i:hover{
            transform: scale(1.1);
        }
        #ii{
            border-radius: 10px;
            width: 96%;
            height: auto;
        }

        .m1.shrink {
            position: absolute;
            top: 10px;
            left: 10px;
            width: 350px;
            overflow: scroll;
            transition: all 1.5s ease;
        }
        .m1.shrink::-webkit-scrollbar {
            width: 0px; 
            height: 0px; 
        }
        .m2.grow{
            position: absolute;
            top: 10px;
            right: 10px;
            margin: 10px;
            width: 650px;
            height: 650px;
            opacity: 1; 
            visibility: visible; 
            transition: all 1.5s ease, opacity 0.5s ease;  
        }
        footer{
            background-color: white;
            border-radius: 30px;
            width: 25%;
            position: absolute;
            bottom: 40px;
            left: 50%;
            translate: -50%;
        }
    </style>
</head>
<title>SAMPLE</title>
<body>
    <h1 align="center">Movie GALLERY</h1>
    <div class="main">
        <div class="m1">
            <img src="4.webp" alt="" id="i" onclick="f(this)">
            <img src="1.jpg" alt="" id="i" onclick="f(this)">
            <img src="2.jpeg" alt="" id="i" onclick="f(this)">
            <img src="3.jpg" alt="" id="i" onclick="f(this)">
            <img src="5.jpg" alt="" id="i" onclick="f(this)">
            <img src="6.jpg" alt="" id="i" onclick="f(this)">
        </div>
        <div class="m2" id="iii" id="i" onclick="c()">
            <img src="" alt="" id="ii">
        </div>
    </div>
    <footer align="center">
        DESIGNED and DEVELOPED by KAMLESH Y
    </footer>

    <script>
        var a=document.getElementById('iii');
        var b=document.getElementById('ii');
        const d=document.querySelector('.m1');
        const d1=document.querySelector('.m2');
        function f(img) {
            d1.classList.add('grow');
            d.classList.add('shrink');
            a.style.display='flex';
            b.src=img.src;
        }
        function c(){
            d1.classList.remove('grow');
            d.classList.remove('shrink');
        }
    </script>
</body>
</html>

```

## OUTPUT:

<img width="1814" height="979" alt="image" src="https://github.com/user-attachments/assets/56ba3fce-1e0d-4d17-8e3d-978f4822e92b" />

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.

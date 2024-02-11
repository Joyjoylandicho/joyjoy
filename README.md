<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Protest+Riot&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="style.css" />
    <title>Happy Valentine's Day!</title>
</head>
<body>
    <div class="container slides">
        <img src="flower.jpg" class="flower-img">
        <img src="flower2.jpeg" class="flower-img" style="display:none;">
        <img src="flower3.jpg" class="flower-img" style="display:none;">
        <img src="flower4.jpg" class="flower-img" style="display:none;">
        <img src="flower5.jpg" class="flower-img" style="display:none;">
        <img src="flower6.jpg" class="flower-img" style="display:none;">
        
        <input type="checkbox" id="slide-toggle"> <!-- Ensure the id matches the for attribute -->
        <label for="slide-toggle" class="btn">Next Slide</label>
    </div>    
    <p class="title">Happy Valentine's Day,
    Ma'am Cristine Joy Hacildo!</p>
    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.flower-img');

        function nextSlide() {
            slides[currentSlide].style.display = 'none';
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].style.display = 'block';
        }

        document.querySelector('.btn').addEventListener('click', nextSlide); // Changed selector to class
    </script>
</body>
</html>

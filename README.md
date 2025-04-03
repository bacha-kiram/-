# -
just a gift
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Image Toggle and Sound</title>
    <style>
        img {
            display: block;
            margin: 50px auto;
            width: 600px;
            height: 600px;
        }
    </style>
</head>
<body>
    <img id="toggleImage" src="c:/VSCode/HTML/HFD/cat01.png" alt="Image" width="300">
    <audio id="click-sound" src="c:/VSCode/HTML/HFD/cat-meow-297927.mp3" preload="auto"></audio>
    
    <script>
        const image = document.getElementById('toggleImage');
        const audio = document.getElementById('click-sound');
        const firstImage = "c:/VSCode/HTML/HFD/cat01.png"; // Original image
        const secondImage = "c:/VSCode/HTML/HFD/cat02.png"; // Image to change to

        // Play sound and change the image when mouse is pressed down
        image.addEventListener('mousedown', () => {
            audio.play();  // Play sound
            image.src = secondImage;  // Change to second image
        });

        // Revert to the first image when mouse is released
        image.addEventListener('mouseup', () => {
            image.src = firstImage;  // Revert to first image
        });

        // Revert to the first image if mouse leaves the image
        image.addEventListener('mouseleave', () => {
            image.src = firstImage;  // Revert to first image
        });
    </script>
</body>
</html>

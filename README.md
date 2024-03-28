<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>its amazing, right?</title>
<style>
  .shape {
    position: absolute;
    opacity: 0.7; /* Partial transparency */
    animation: moveAndSpin linear infinite, colorChange 5s infinite alternate; /* Add color change animation */
    transition: opacity 0.5s; /* Smooth transition for opacity */
  }

  .circle {
    width: 50px;
    height: 50px;
    border-radius: 50%; /* Circle shape */
    box-shadow: 5px 5px 5px rgba(0, 255, 0, 0.5); /* Box shadow */
    border: 2px solid orange; /* Outline */
  }

  .square {
    width: 60px;
    height: 60px;
    border: 3px solid black;
    border-radius: 10px; /* Rounded corners */
    box-shadow: 5px 5px 5px rgba(0, 0, 255, 0.5); /* Box shadow */
  }

  .triangle {
    width: 0;
    height: 0;
    border-left: 25px solid transparent;
    border-right: 25px solid transparent;
    border-bottom: 50px solid blue; /* Triangle shape */
    box-shadow: 2px 2px 5px rgba(255, 0, 3, 0.5); /* Box shadow */
    border-left: 25px solid transparent; /* Outline */
    border-right: 25px solid transparent; /* Outline */
    border-bottom: 50px solid blue; /* Outline */
  }

  @keyframes moveAndSpin {
    0% {
      transform: translateY(0) rotate(0deg);
    }
    100% {
      transform: translateY(100vh) rotate(360deg);
    }
  }

  @keyframes colorChange {
    0%, 100% {
      background-color: rgba(255, 255, 0, 0.7); /* Start and end color */
    }
    50% {
      background-color: rgba(0, 255, 255, 0.7); /* Middle color */
    }
  }
</style>
</head>
<body>
<script>
  // Function to generate random color
  function getRandomColor() {
    var colors = ['#FF0000', '#FFFF00', '#0000FF']; // Red, Yellow, Blue
    return colors[Math.floor(Math.random() * colors.length)];
  }

  // Function to generate random speed
  function getRandomSpeed() {
    return Math.random() * 5 + 1; // Random speed between 1 and 6 seconds
  }

  // Create circles with random colors and speeds
  for (var i = 0; i < 50; i++) {
    var circle = document.createElement('div');
    circle.className = 'shape circle';
    circle.style.backgroundColor = getRandomColor();
    circle.style.animationDuration = getRandomSpeed() + 's';
    circle.style.left = Math.random() * window.innerWidth + 'px';
    document.body.appendChild(circle);
  }

  // Create squares with random colors and speeds
  for (var i = 0; i < 50; i++) {
    var square = document.createElement('div');
    square.className = 'shape square';
    square.style.backgroundColor = getRandomColor();
    square.style.animationDuration = getRandomSpeed() + 's';
    square.style.left = Math.random() * window.innerWidth + 'px';
    document.body.appendChild(square);
  }

  // Create triangles with random colors and speeds
  for (var i = 0; i < 50; i++) {
    var triangle = document.createElement('div');
    triangle.className = 'shape triangle';
    triangle.style.backgroundColor = getRandomColor();
    triangle.style.animationDuration = getRandomSpeed() + 's';
    triangle.style.left = Math.random() * window.innerWidth + 'px';
    document.body.appendChild(triangle);
  }
</script>
</body>
</html>

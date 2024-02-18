<svg fill="none" viewBox="0 0 600 300" width="600" height="300" xmlns="http://www.w3.org/2000/svg">
  <foreignObject width="100%" height="100%">
<style>
    /* Importing Google font - Inter */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Inter", sans-serif;
}
body {
    display: flex;
    height: 100vh;
    align-items: center;
    justify-content: center;
    background: #1D1E23;
}
h1 {
    color: #fff;
    font-size: 2rem;
    font-weight: 600;
}
h1 span {
    color: #BD53ED;
    position: relative;
}
h1 span::before {
    content: "";
    height: 30px;
    width: 2px;
    position: absolute;
    top: 50%;
    right: -8px;
    background: #BD53ED;
    transform: translateY(-45%);
    animation: blink 0.7s infinite;
}
h1 span.stop-blinking::before {
    animation: none;
}
@keyframes blink {
    50% { opacity: 0 }
}
</style>
   
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typing Text Effect | CodingNepal</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js" defer></script>
</head>
<body>
    <h1>Coding is <span></span></h1>
</body>
</html>

<script>
    const dynamicText = document.querySelector("h1 span");
const words = ["Love", "like Art", "the Future", "Everything"];
// Variables to track the position and deletion status of the word
let wordIndex = 0;
let charIndex = 0;
let isDeleting = false;
const typeEffect = () => {
    const currentWord = words[wordIndex];
    const currentChar = currentWord.substring(0, charIndex);
    dynamicText.textContent = currentChar;
    dynamicText.classList.add("stop-blinking");
    if (!isDeleting && charIndex < currentWord.length) {
        // If condition is true, type the next character
        charIndex++;
        setTimeout(typeEffect, 200);
    } else if (isDeleting && charIndex > 0) {
        // If condition is true, remove the previous character
        charIndex--;
        setTimeout(typeEffect, 100);
    } else {
        // If word is deleted then switch to the next word
        isDeleting = !isDeleting;
        dynamicText.classList.remove("stop-blinking");
        wordIndex = !isDeleting ? (wordIndex + 1) % words.length : wordIndex;
        setTimeout(typeEffect, 1200);
    }
}
typeEffect();
</script> 

  </foreignObject>
</svg>


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
<div>
    <h1>Coding is <span></span></h1>
</div>

  </foreignObject>
</svg>


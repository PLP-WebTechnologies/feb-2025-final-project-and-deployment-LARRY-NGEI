# Final Project and Deployment
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="hero">
            <h1>Welcome to My Site</h1>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 My Website</p>
    </footer>

    <script src="js/script.js"></script>
</body>
</html>


/* Base Styles */
body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
    margin: 0;
}

/* Responsive Navigation */
nav ul {
    display: flex;
    gap: 1rem;
    padding: 1rem;
    background: #333;
}

nav a {
    color: white;
    text-decoration: none;
}

/* Mobile First */
@media (max-width: 600px) {
    nav ul {
        flex-direction: column;
    }
}

/* Hero Section */
.hero {
    min-height: 300px;
    display: grid;
    place-items: center;
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                url('../images/hero-bg.jpg');
    background-size: cover;
    color: white;
}

// Form Validation (contact.html)
document.querySelector('form').addEventListener('submit', (e) => {
    const email = document.getElementById('email').value;
    if (!email.includes('@')) {
        e.preventDefault();
        alert('Please enter a valid email!');
    }
});

// Image Slider (home.html)
let currentSlide = 0;
function showSlide(index) {
    const slides = document.querySelectorAll('.slider img');
    slides.forEach((slide, i) => {
        slide.style.display = i === index ? 'block' : 'none';
    });
}





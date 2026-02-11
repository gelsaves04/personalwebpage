<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Personal Profile Page</title>

<style>
/* ================= RESET ================= */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Arial, sans-serif;
}

/* ================= BASE ================= */
body {
    background-color: #f4f6f8;
    color: #000000;
    max-width: 1200px;
    margin: auto;
    padding: 20px;
    transition: background 0.3s, color 0.3s;
}

/* ================= HEADER ================= */
header {
    background: linear-gradient(135deg, #fe798f, hsl(186, 94%, 75%));
    color: rgb(0, 0, 0);
    text-align: center;
    padding: 40px 20px;
    border-radius: 12px;
    margin-bottom: 30px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.15);
}

header img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    border: 5px solid rgb(103, 7, 76);
    object-fit: cover;
    margin-bottom: 15px;
    animation: float 3s ease-in-out infinite;
}

header h1 {
    font-size: 2.4rem;
}

header p {
    font-size: 1.2rem;
    font-style: italic;
}

/* ================= BUTTON ================= */
#themeToggle {
    margin-top: 15px;
    padding: 10px 18px;
    border-radius: 20px;
    border: none;
    cursor: pointer;
    background: white;
    color: #4e54c8;
    font-size: 14px;
    transition: all 0.3s;
}

#themeToggle:hover {
    background: #4e54c8;
    color: white;
}

/* ================= LAYOUT ================= */
.container {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 25px;
}

main, aside {
    background: white;
    padding: 25px;
    border-radius: 12px;
    box-shadow: 0 6px 15px rgba(0,0,0,0.08);
    transition: transform 0.3s;
}

main:hover, aside:hover {
    transform: translateY(-4px);
}

h2 {
    color: #4e54c8;
    margin-bottom: 15px;
    border-bottom: 2px solid #eee;
    padding-bottom: 5px;
}

section {
    margin-bottom: 25px;
}

/* ================= SKILLS ================= */
ul {
    list-style: adkdk;
}

ul li {
    background: #eef0ff;
    margin-bottom: 10px;
    padding: 10px;
    border-left: 4px solid #4e54c8;
    border-radius: 6px;
    transition: all 0.3s;
}

ul li:hover {
    transform: translateX(6px);
    background: #dde0ff;
}

/* ================= LINKS ================= */
a {
    color: #4b313138;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}

/* ================= FOOTER ================= */
footer {
    text-align: center;
    margin-top: 40px;
    padding: 20px;
    color: #666;
    border-top: 1px solid #ddd;
}


/* ================= ANIMATION ================= */
@keyframes float {
    0% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
    100% { transform: translateY(0); }
}

/* ================= ACCESSIBILITY ================= */
a:focus,
button:focus {
    outline: 3px dashed #8f94fb;
    outline-offset: 4px;
}

/* ================= RESPONSIVE ================= */
@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
    }
}

/* ================= PRINT ================= */
@media print {
    header, footer, #themeToggle {
        display: none;
    }
    body {
        background: white;
        color: black;
    }
}
</style>
</head>

<body>

<header>
    <img src="photo.jpg" alt="My photo" width="300">
    <h1>Anne Gelleen Dunlao</h1>
    <p>Information Technology Student</p>
    
</header>

<div class="container">

    <main>
        <section>
            <h2>About Me</h2>
            <p>Hello! I am Anne Gelleen Aves, an Information Technology student with a passion for learning modern web technologies.</p>
            <p>I enjoy building responsive and accessible websites using HTML, CSS, and JavaScript.</p>
            <p>My goal is to grow as a professional IT practitioner and apply my skills in real-world projects.</p>
        </section>

        <section>
            <h2>Education</h2>
            <article>
                <h3>Bachelor of Science in Information Technology</h3>
                <p>National Teachers College</p>
                <p>2023 – Present</p>
            </article>
        </section>
    </main>

    <aside>
        <section>
            <h2>Skills</h2>
            <ul>
                <li>Visual and layout creation</li>
                <li>Social media posting & basic content creation</li>
                <li>Computer Troubleshooting</li>
                <li>Basic Networking</li>
                <li>System Documentation</li>
            </ul>
        </section>

        <section>
            <h2>Contact</h2>
            <p>📧 anneaves@email.com</p>
            <p>📞 0912-345-6789</p>
            <p>🔗 <a href="https://www.facebook.com/" target="_blank">facebook.com/anneaves</a></p>
        </section>
    </aside>

</div>

<footer>
    <p>© 2026 Anne Gelleen Dunlao. All rights reserved.</p>
    <p>Built with HTML5, CSS3, and JavaScript</p>
</footer>

<script>
const toggleBtn = document.getElementById("themeToggle");
const body = document.body;

toggleBtn.addEventListener("click", () => {
    body.classList.toggle("dark-mode");
    toggleBtn.textContent = body.classList.contains("dark-mode")
        ? "☀️ Light Mode"
        : "🌙 Dark Mode";
});
</script>

</body>
</html>

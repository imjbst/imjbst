<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
    <link rel="stylesheet" href="index.css">
    <title>Portfolio</title>

<style>
:root {
    --primary-color: #f9532d;
    --primary-dark: #1F252E;
}

* {
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
}

body {
    font-family: 'Outfit', sans-serif;
    background: #ffffff;
    height: 100vh;
    color: #000;
}

/* Genral */
.container {
    padding: 0 8.4rem;
}

.img-w {
    width: 100%;
    height: auto;
}

/* Nav */
header {
    box-shadow: 0 4px 17px rgba(0, 0, 0, .1);
    background: #fff;
    position: sticky;
    top: 0;
    z-index: 1;
}

.page-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
}

.logo {
    font-size: 1.5rem;
    font-weight: 800;
    opacity: 0;
    animation: leftSideAni 1s ease forwards;
}

.logo a {
    color: #000;
    text-decoration: none;
}

ul {
    display: flex;
    gap: .6rem;
    list-style-type: none;
    background-color: transparent;
    overflow: hidden;
}

li a {
    display: inline-block;
    padding: .3rem 1rem;
    color: #000;
    text-decoration: none;
    font-size: 1.05rem;
    font-weight: 600;
    letter-spacing: .7px;
    border-radius: 36px;
    line-height: 2;
    transition: .3s;
    opacity: 0;
    animation: navani .3s ease forwards;
    animation-delay: calc(.15s * var(--navAni));
}

li a.active,
li a:hover {
    color: var(--primary-color);
}

#click {
    display: none;
}

.menu {
    display: none;
}

.mode i {
    font-size: 1.4rem;
    cursor: pointer;
    color: var(--primary-color);
    opacity: 0;
    animation: rightSideAni 1.5s ease forwards;
}

/* Nav End */

/* Section 1 */

.main {
    padding: 6rem 0;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    row-gap: 2rem;
    column-gap: 6rem;
    align-items: center;
}

.main h3 {
    color: #000;
    font-size: 1.5rem;
    opacity: 0;
    animation: topSideAni 1s ease forwards;
}

.main h1 {
    color: #000;
    font-size: 4rem;
    font-weight: 600;
    opacity: 0;
    animation: leftSideAni 1s ease forwards;
    animation-delay: 1s;
}

.social {
    display: flex;
    flex-wrap: wrap;
    gap: 1.4rem;
    margin-top: 1.4rem;
}

.social a {
    display: grid;
    place-items: center;
    text-decoration: none;
    color: var(--primary-color);
    border: 1.6px solid var(--primary-color);
    font-size: 1.5rem;
    border-radius: 50%;
    padding: 0.39rem;
    text-align: center;
    opacity: 0;
    animation: SocialAni 1s ease forwards;
    animation-delay: calc(.2s * var(--socialAni));
}

.social a:hover {
    color: var(--primary-dark);
    background-color: var(--primary-color);
    box-shadow: 0 0 20px var(--primary-color);
    transition: all .3s ease-in-out;
}


.images {
    border-radius: 10px;
    width: 450px;
    /* opacity: 0; */
    /* animationhttps://uupload.ir/view/web_19wl.mp4/; */
    /* animation-delay: 1.5s */
}
.images {
    background: linear-gradient(145deg, #e2e8ec, #ffffff);
    box-shadow: 5px 5px 15px #D1D9E6, -5px -5px 15px #ffffff;
    border-top: 2px solid var(--primary-color);
}

/* Section 1 End */


.dark-mode {
    background-color: var(--primary-dark);
    color: #ffffff;
}

.mode input {
    display: none;
}

.dark-mode .logo a, 
.dark-mode ul li a, 
.dark-mode .main h3, 
.dark-mode .main h1 {
    color: #fff;
}
.dark-mode ul li a.active, .dark-mode ul li a:hover {
    color: var(--primary-color);
}
.dark-mode .images {
    background: linear-gradient(145deg, #1f252e, #2e3239);
    box-shadow: 10px 10px 19px #1c1e22, -10px -10px 19px #1b1f27;
    border-top: 2px solid var(--primary-color);
    border-bottom-left-radius: 60px;
    border-bottom-right-radius: 60px;
    margin: auto;
    overflow: hidden;
}

.dark-mode header {
    box-shadow: 0 4px 17px rgb(80 80 80 / 31%);
    background: var(--primary-dark);
}



/* Animation */
@keyframes leftSideAni {
    0% {
        transform: translateX(-100px);
        opacity: 0;
    }

    100% {
        transform: translateX(0);
        opacity: 1;
    }
}

@keyframes navani {
    0% {
        transform: translateY(100px);
        opacity: 0;
    }

    100% {
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes rightSideAni {
    0% {
        transform: translateX(100px);
        opacity: 0;
    }

    100% {
        transform: translateX(0);
        opacity: 1;
    }
}

@keyframes topSideAni {
    0% {
        transform: translateY(-100px);
        opacity: 0;
    }

    100% {
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes SocialAni {
    0% {
        transform: translateY(100px);
        opacity: 0;
    }

    100% {
        transform: translateY(0);
        opacity: 1;
    }
}

/* @keyframes ImgAni {
    0% {
        transform: translateX(0);
    }
    50% {
        transform: translateX(-9px);
    }
    100% {
        transform: translateX(0);
    }
} */
@keyframes imageAni {
    0% {
        opacity: 0;
        transform: scale(0);
    }

    100% {
        opacity: 1;
        transform: scale(1);
    }
}

@media screen and (max-width: 1024px) {
    .container {
        padding: 0 4.4rem;
    }

    .main h3 {
        color: #000;
        margin-top: 1rem;
    }
}

@media screen and (max-width: 768px) {
    .container {
        padding: 0 1.6rem;
    }
}

@media screen and (max-width:600px) {
    body {
        height: auto;
    }

    header {
        height: auto;
    }

    ul {
        background: #fff;
        width: 100%;
        height: 100vh;
        position: absolute;
        display: flex;
        flex-direction: column;
        text-align: center;
        top: 3.4rem;
        left: -100%;
        z-index: 111111;
    }

    .menu {
        display: block;
        font-size: 1.5rem;
        font-weight: bold;
        color: var(--primary-color);
    }

    #click:checked~ul {
        left: 0%;
        transition: all 0.3s ease;
    }
    .dark-mode .menu {
        color: var(--primary-color);
    }

    .dark-mode ul {
        background: var(--primary-dark);
    }

    .mode {
        position: absolute;
        right: 4rem;
    }
    .images {
        width: 100%;
        margin: auto;
    }

    .main {
        margin-top: 2rem;
    }
}
</style>
</head>

<body>
    <header class="container">
        <div class="page-header">
            <div class="logo">
                <a href="#">imjbst</a>
            </div>
            <input type="checkbox" id="click">

            <label for="click" class="mainicon">
                <div class="menu">
                    <i class='bx bx-menu'></i>
                </div>
            </label>
            <ul>
                <li><a href="#"  class="active" style="--navAni:1">Home</a></li>
                <li><a href="#" style="--navAni:2">About</a></li>
                <li><a href="#" style="--navAni:3">Skills</a></li>
                <li><a href="#" style="--navAni:4">Portfolio</a></li>
                <li><a href="#" style="--navAni:5">Contact</a></li>
            </ul>
            <label class="mode">
                <input type="checkbox" id="darkModeToggle">
                <i class='bx bxs-moon'></i>
            </label>
        </div>
    </header>


    <section class="container">
        <div class="main">
            <div class="images">
                <img src="https://s6.uupload.ir/files/photo8224240412_5f4b.jpg" alt="" class="img-w">
                <span class="bg-effect-1">
                <span class="bg-effect-1"></span>

                </span>
            </div>
            <div class="detail">
                <h3>Hi, I'm</h3>
                <h1><span style="color:#f9532d;">mohammad javad </span> Basati</h1> 
                <p>I'm a professional Web Developer. Our Main Goal to help & Satisficed the Local & Global Clients by
                    web development solutions
                </p>  
                <div class="social">
                    <a href="https://www.linkedin.com/in/imjbst/" style="--socialAni:1"><i class='bx bxl-linkedin'></i></a>
                    <a href="https://www.instagram.com/imjbst/" style="--socialAni:2"><i class='bx bxl-instagram'></i></a>
                    <a href="https://github.com/imjbst" style="--socialAni:3"><i class='bx bxl-github'></i></a>
                    <a href="https://www.youtube.com/@imjbst" style="--socialAni:4"><i class='bx bxl-youtube'></i></a>
                </div>
            </div>
        </div>
    </section>

    <script>
        const darkModeToggle = document.getElementById('darkModeToggle');
        const body = document.body;
        const isDarkMode = localStorage.getItem('darkMode') === 'enabled';
        if (isDarkMode) {
            body.classList.add('dark-mode');
            darkModeToggle.checked = true;
        }
        darkModeToggle.addEventListener('change', () => {
            if (darkModeToggle.checked) {
                body.classList.add('dark-mode');
                localStorage.setItem('darkMode', 'enabled');
            } else {
                body.classList.remove('dark-mode');
                localStorage.setItem('darkMode', 'disabled');
            }
        });
    </script>
</body>

</html>


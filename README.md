
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Cards</title>
    <link rel="stylesheet" href="style.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #191c29;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .card-link {
            text-decoration: none;
        }

        .card {
            width: 200px;
            height: 400px;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            padding: 0 36px;
            perspective: 2500px;
            margin: 0 50px;
            background: #191c29;
            transition: transform 0.5s;
        }

        .card:hover .wrapper {
            transform: perspective(900px) translateY(-5%) rotateX(390deg) translateZ(0);
            box-shadow: 2px 35px 32px -8px rgba(138, 43, 226, 0.75); /* Purple shadow color */
            -webkit-box-shadow: 2px 35px 32px -8px rgba(138, 43, 226, 0.75); /* Purple shadow color */
            -moz-box-shadow: 2px 35px 32px -8px rgba(138, 43, 226, 0.75); /* Purple shadow color */
        }

        .cover-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .wrapper {
            transition: all 0.5s;
            position: absolute;
            width: 100%;
            z-index: -1;
        }

        .card:hover .wrapper::before,
        .wrapper::after {
            opacity: 1;
        }

        .card:hover .wrapper::after {
            height: 120px;
        }

        .title {
            width: 100%;
            transition: transform 0.5s;
        }

        .card:hover .title {
            transform: translate3d(0%, -50px, 100px);
        }

        .character {
            width: 100%;
            opacity: 0;
            transition: all 0.5s;
            position: absolute;
            z-index: -1;
        }

        .card:hover .character {
            opacity: 1;
            transform: translate3d(0%, -30%, 100px);
        }
    </style>
</head>
<body>
    <a href="https://rustyloot.gg/r/LEFAY" alt="Mythrill" target="_blank" class="card-link">
        <div class="card">
            <div class="wrapper">
                <img src="https://i.ibb.co/P9q2MLr/Purple-Modern-Coming-Soon-Instagram-Post.png" class="cover-image" />
            </div>
            <img src="https://i.ibb.co/hYkknmJ/Namnl-s-design-1-removebg-preview.png" class="title" alt="Namnl-s-design-1" />
            <img src="https://i.ibb.co/3FT9j5j/Green-Floral-Pine-Christmas-Page-Border-4.png" alt="Namnl-s-design-3" class="character" />
        </div>
    </a>

    <a href="https://bandit.camp/r/LEFAY" alt="Mythrill" target="_blank" class="card-link">
        <div class="card">
            <div class="wrapper">
                <img src="https://i.ibb.co/8M7hX5Z/Green-Floral-Pine-Christmas-Page-Border-2.png" class="cover-image" />
            </div>
            <img src="https://i.ibb.co/gr6W3kw/Namnl-s-design-14.png" alt="Namnl-s-design-14" class="title" />
            <img src="https://ggayan.github.io/css-experiments/crds/force_mage-character.webp" class="character" />
        </div>
    </a>

    <script src="script.js"></script>
</body>
</html>

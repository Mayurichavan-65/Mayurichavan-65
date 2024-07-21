<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pet Shop Landing Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://media.istockphoto.com/id/1197037573/vector/pet-store-illustration.jpg?s=612x612&w=0&k=20&c=YS-q7g1H_t21ZtAsnD3LU29jyiyTaasKOVfdYCoUdKg='); /* Replace with your background image */
            background-size: cover;
            background-attachment: fixed;
            background-repeat: no-repeat;
            color: #000000;
        }

        header {
            background-color: rgba(0, 0, 0, 0.8);
            color: rgb(171, 238, 216);
            padding: 1em 0;
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 10px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
        }

        section {
            background-color: rgba(255, 255, 255, 0.8);
            margin: 2em 10%;
            padding: 2em;
            border-radius: 10px;
            text-align: center;
        }

        .gallery {
            display: flex;
            justify-content: center;
        }

        .pet {
            margin: 10px;
            cursor: pointer;
        }

        .pet img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            transition: transform 0.3s;
        }

        .pet img:hover {
            transform: scale(1.1);
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .modal-content {
            background-color: white;
            margin: 15% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            text-align: center;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Pet Shop!</h1>
        <nav>
            <ul>
                <li><a href="#about">About Us</a></li>
                <li><a href="#pets">Our Pets</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="about">
        <h2>About Us</h2>
        <p>We offer a wide variety of pets for adoption. Come visit us to find your new best friend!</p>
    </section>
    
    <section id="pets">
        <h2>Our Pets</h2>
        <div class="gallery">
            <div class="pet" onclick="showInfo('dog')">
                <img src="https://img.freepik.com/free-photo/cute-dog-sleeping-ai-generated_23-2150644023.jpg?size=626&ext=jpg&ga=GA1.1.2008272138.1721347200&semt=ais_user" alt="Dog">
                <p>Dogs</p>
            </div>
            <div class="pet" onclick="showInfo('cat')">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9SS-5zOSVWJbp29slDdgQPGEiOIUxCm-z1Q&s" alt="Cat">
                <p>Cats</p>
            </div>
            <div class="pet" onclick="showInfo('bird')">
                <img src="https://www.tracyvets.com/files/Parakeets.jpeg" alt="Bird">
                <p>Birds</p>
            </div>
        </div>
    </section>
    
    <section id="contact">
        <h2>Contact Us</h2>
        <p>Name: Mayuri Chavan</p>
        <p>Email: contact@petshop.com</p>
        <p>Phone: 123-456-7890</p>
    </section>
    
    <div id="info-modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <p id="modal-text"></p>
        </div>
    </div>
    
    <script>
        function showInfo(pet) {
            var modal = document.getElementById("info-modal");
            var modalText = document.getElementById("modal-text");
            
            if (pet === 'dog') {
                modalText.textContent = "Dogs are loyal and friendly pets. They require regular exercise and love to play.";
            } else if (pet === 'cat') {
                modalText.textContent = "Cats are independent and curious animals. They love to explore and can be very affectionate.";
            } else if (pet === 'bird') {
                modalText.textContent = "Birds are colorful and social pets. They enjoy singing and can be very entertaining.";
            }
            
            modal.style.display = "block";
        }

        function closeModal() {
            var modal = document.getElementById("info-modal");
            modal.style.display = "none";
        }

        // Close the modal when clicking outside of it
        window.onclick = function(event) {
            var modal = document.getElementById("info-modal");
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pet Shop Landing Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://media.istockphoto.com/id/1197037573/vector/pet-store-illustration.jpg?s=612x612&w=0&k=20&c=YS-q7g1H_t21ZtAsnD3LU29jyiyTaasKOVfdYCoUdKg='); /* Replace with your background image */
            background-size: cover;
            background-attachment: fixed;
            background-repeat: no-repeat;
            color: #000000;
        }

        header {
            background-color: rgba(0, 0, 0, 0.8);
            color: rgb(171, 238, 216);
            padding: 1em 0;
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 10px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
        }

        section {
            background-color: rgba(255, 255, 255, 0.8);
            margin: 2em 10%;
            padding: 2em;
            border-radius: 10px;
            text-align: center;
        }

        .gallery {
            display: flex;
            justify-content: center;
        }

        .pet {
            margin: 10px;
            cursor: pointer;
        }

        .pet img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            transition: transform 0.3s;
        }

        .pet img:hover {
            transform: scale(1.1);
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .modal-content {
            background-color: white;
            margin: 15% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            text-align: center;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Pet Shop!</h1>
        <nav>
            <ul>
                <li><a href="#about">About Us</a></li>
                <li><a href="#pets">Our Pets</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="about">
        <h2>About Us</h2>
        <p>We offer a wide variety of pets for adoption. Come visit us to find your new best friend!</p>
    </section>
    
    <section id="pets">
        <h2>Our Pets</h2>
        <div class="gallery">
            <div class="pet" onclick="showInfo('dog')">
                <img src="https://img.freepik.com/free-photo/cute-dog-sleeping-ai-generated_23-2150644023.jpg?size=626&ext=jpg&ga=GA1.1.2008272138.1721347200&semt=ais_user" alt="Dog">
                <p>Dogs</p>
            </div>
            <div class="pet" onclick="showInfo('cat')">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9SS-5zOSVWJbp29slDdgQPGEiOIUxCm-z1Q&s" alt="Cat">
                <p>Cats</p>
            </div>
            <div class="pet" onclick="showInfo('bird')">
                <img src="https://www.tracyvets.com/files/Parakeets.jpeg" alt="Bird">
                <p>Birds</p>
            </div>
        </div>
    </section>
    
    <section id="contact">
        <h2>Contact Us</h2>
        <p>Name: Mayuri Chavan</p>
        <p>Email: contact@petshop.com</p>
        <p>Phone: 123-456-7890</p>
    </section>
    
    <div id="info-modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <p id="modal-text"></p>
        </div>
    </div>
    
    <script>
        function showInfo(pet) {
            var modal = document.getElementById("info-modal");
            var modalText = document.getElementById("modal-text");
            
            if (pet === 'dog') {
                modalText.textContent = "Dogs are loyal and friendly pets. They require regular exercise and love to play.";
            } else if (pet === 'cat') {
                modalText.textContent = "Cats are independent and curious animals. They love to explore and can be very affectionate.";
            } else if (pet === 'bird') {
                modalText.textContent = "Birds are colorful and social pets. They enjoy singing and can be very entertaining.";
            }
            
            modal.style.display = "block";
        }

        function closeModal() {
            var modal = document.getElementById("info-modal");
            modal.style.display = "none";
        }

        // Close the modal when clicking outside of it
        window.onclick = function(event) {
            var modal = document.getElementById("info-modal");
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pet Shop Landing Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://media.istockphoto.com/id/1197037573/vector/pet-store-illustration.jpg?s=612x612&w=0&k=20&c=YS-q7g1H_t21ZtAsnD3LU29jyiyTaasKOVfdYCoUdKg='); /* Replace with your background image */
            background-size: cover;
            background-attachment: fixed;
            background-repeat: no-repeat;
            color: #000000;
        }

        header {
            background-color: rgba(0, 0, 0, 0.8);
            color: rgb(171, 238, 216);
            padding: 1em 0;
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 10px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
        }

        section {
            background-color: rgba(255, 255, 255, 0.8);
            margin: 2em 10%;
            padding: 2em;
            border-radius: 10px;
            text-align: center;
        }

        .gallery {
            display: flex;
            justify-content: center;
        }

        .pet {
            margin: 10px;
            cursor: pointer;
        }

        .pet img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            transition: transform 0.3s;
        }

        .pet img:hover {
            transform: scale(1.1);
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .modal-content {
            background-color: white;
            margin: 15% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            text-align: center;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Pet Shop!</h1>
        <nav>
            <ul>
                <li><a href="#about">About Us</a></li>
                <li><a href="#pets">Our Pets</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="about">
        <h2>About Us</h2>
        <p>We offer a wide variety of pets for adoption. Come visit us to find your new best friend!</p>
    </section>
    
    <section id="pets">
        <h2>Our Pets</h2>
        <div class="gallery">
            <div class="pet" onclick="showInfo('dog')">
                <img src="https://img.freepik.com/free-photo/cute-dog-sleeping-ai-generated_23-2150644023.jpg?size=626&ext=jpg&ga=GA1.1.2008272138.1721347200&semt=ais_user" alt="Dog">
                <p>Dogs</p>
            </div>
            <div class="pet" onclick="showInfo('cat')">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9SS-5zOSVWJbp29slDdgQPGEiOIUxCm-z1Q&s" alt="Cat">
                <p>Cats</p>
            </div>
            <div class="pet" onclick="showInfo('bird')">
                <img src="https://www.tracyvets.com/files/Parakeets.jpeg" alt="Bird">
                <p>Birds</p>
            </div>
        </div>
    </section>
    
    <section id="contact">
        <h2>Contact Us</h2>
        <p>Name: Mayuri Chavan</p>
        <p>Email: contact@petshop.com</p>
        <p>Phone: 123-456-7890</p>
    </section>
    
    <div id="info-modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <p id="modal-text"></p>
        </div>
    </div>
    
    <script>
        function showInfo(pet) {
            var modal = document.getElementById("info-modal");
            var modalText = document.getElementById("modal-text");
            
            if (pet === 'dog') {
                modalText.textContent = "Dogs are loyal and friendly pets. They require regular exercise and love to play.";
            } else if (pet === 'cat') {
                modalText.textContent = "Cats are independent and curious animals. They love to explore and can be very affectionate.";
            } else if (pet === 'bird') {
                modalText.textContent = "Birds are colorful and social pets. They enjoy singing and can be very entertaining.";
            }
            
            modal.style.display = "block";
        }

        function closeModal() {
            var modal = document.getElementById("info-modal");
            modal.style.display = "none";
        }

        // Close the modal when clicking outside of it
        window.onclick = function(event) {
            var modal = document.getElementById("info-modal");
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
    </script>
</body>
</html>

# friendsinvitation.github.io
<!DOCTYPE html>
<html lang="ru">
    <head>
        <link href="./styles.css" rel="stylesheet"/>
        <style>
            body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 90vh;
    background-color: #f4f6f4;
}

#noButton {
    position: absolute;
    margin-left: 150px;
    transition: 0.5s;
}

#yesButton {
    position: absolute;
    margin-right: 150px;
}

.header_text {
    font-family: 'Nunito';
    font-size: 40px;
    font-weight: bold;
    color: #FFB6C1;
    text-align: center;
    margin-top: 20px;
    margin-bottom: 0px;
}

.buttons {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
    margin-left: 20px;
}

.btn {
    background-color: #FFB6C1;
    color: white;
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border: none;
    border-radius: 12px;
    transition: background-color 0.3s ease;
}

.gif_container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 90px;
}
        </style>
    </head>
    <body>
        <div class="container">
            <div>
                <h1 class="header_texst">Пойдешь гулять со мной?</h1>
            </div>
            <div class="gif_container">
                <img src="https://i.postimg.cc/FsSqchXw/pig-pig-funny.gif">
            </div>
            <div class="buttons">
                <button class="btn" id="yesButton" onclick="nextPage()">Да</button>
                <button class="btn" id="noButton" onmouseover="moveButton()" onclick="moveButton()">Нет</button>
                <script>
                    function nextPage() {
                        window.location.href = "yes.html";
                    }

                    function moveButton() {
                        var x = Math.random() * (window.innerWidth - document.getElementById('noButton').offsetWidth);
                        var y = Math.random() * (window.innerHeight - document.getElementById('noButton').offsetHeight);
                        document.getElementById('noButton').style.left = `${x}px`;
                        document.getElementById('noButton').style.top = `${y}px`;
                    }
                </script>
            </div>
        </div>
    </body>
</html>

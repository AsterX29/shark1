<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Кнопка на сайте</title>
    <style>
        body {
            /* Устанавливаем фоновую картинку и настраиваем ее свойства */
            background-image: url('Эльбрус.jpg'); /* Укажите путь к вашей картинке */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            height: 100vh; /* Это позволит вашему фону занимать всю высоту экрана */
            margin: 0; /* Убираем отступы по умолчанию */
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Стили для кнопки (можно настроить по своему вкусу) */
        .my-button {
            display: inline-block;
            padding: 10px 20px;
            font-size: 16px;
            text-align: center;
            text-decoration: none;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <!-- HTML-элемент кнопки -->
    <button onclick="hideElements()">Нажми, чтобы скрыть</button>
<img id="myImage" src="1.jpg" alt="Ваше изображение" height="600px">
        <script>
        function hideElements() {
            var button = document.querySelector('button');
            var image = document.getElementById('myImage');
    
            // Скрываем кнопку
            button.style.display = 'none';
    
            // Скрываем изображение
            image.style.display = 'none';
        }
    </script>
</body>
</html>

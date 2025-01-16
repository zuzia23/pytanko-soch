<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Czy zostaniesz moją walentynką?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffe4e1;
            margin: 0;
            padding: 0;
        }
        h1 {
            margin-top: 50px;
            color: #d62d5e;
        }
        form {
            margin-top: 30px;
        }
        label {
            font-size: 20px;
            margin: 20px;
            color: #555;
        }
        button {
            display: block;
            margin: 20px auto;
            padding: 10px 20px;
            font-size: 18px;
            background-color: #d62d5e;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #c22753;
        }
        .thanks {
            margin-top: 30px;
            font-size: 24px;
            color: #d62d5e;
        }
    </style>
</head>
<body>
    <h1>Czy zostaniesz moją walentynką?</h1>
    <form id="survey-form">
        <label>
            <input type="radio" name="valentine" value="yes" required> Tak
        </label>
        <label>
            <input type="radio" name="valentine" value="no" required> Nie
        </label>
        <button type="submit">Odpowiedz</button>
    </form>
    <div id="thanks-message" class="thanks" style="display: none;">
        Dziękuję, kocham cię ❤️
    </div>
    <script>
        const form = document.getElementById('survey-form');
        const thanksMessage = document.getElementById('thanks-message');

        form.addEventListener('submit', function(event) {
            event.preventDefault(); // Zapobiega odświeżeniu strony
            thanksMessage.style.display = 'block';
            form.style.display = 'none'; // Ukrywa formularz po odpowiedzi
        });
    </script>
</body>
</html>

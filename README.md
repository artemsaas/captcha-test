<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Captcha Verification</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f3f4f6;
            font-family: Arial, sans-serif;
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            text-align: center;
        }
        button {
            background-color: #2563eb;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            transition: all 0.3s;
        }
        button:hover {
            background-color: #1d4ed8;
        }
    </style>
    <script src="https://www.google.com/recaptcha/api.js" async defer></script>
</head>
<body>
    <div class="container">
        <h1>Пожалуйста, подтвердите, что вы не робот</h1>
        <form id="captchaForm">
            <div class="g-recaptcha" data-sitekey="6LekGs8qAAAAAEot_mA3tPhn4oiBcjCv4UgPyiW0"></div>
            <button type="submit">Перейти на оффер</button>
        </form>
    </div>

    <script>
        const form = document.getElementById('captchaForm');
        const redirectUrl = "https://piratecpa.net/";

        form.addEventListener('submit', (event) => {
            event.preventDefault();
            const response = grecaptcha.getResponse();

            if (response.length === 0) {
                alert("Пожалуйста, решите капчу!");
            } else {
                // Перенаправление после успешного решения капчи
                window.location.href = redirectUrl;
            }
        });
    </script>
</body>
</html>


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
            margin: 0;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            text-align: center;
            max-width: 100%;
            width: 400px;
        }
        h1 {
            font-size: 1.5rem;
            margin-bottom: 20px;
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
            width: 100%;
        }
        button:hover {
            background-color: #1d4ed8;
        }
        .g-recaptcha {
            margin-bottom: 15px;
            transform: scale(0.77); /* Уменьшаем размер капчи */
            transform-origin: 0 0; /* Позиционируем уменьшенную капчу в левый верхний угол */
        }
        @media (max-width: 600px) {
            .container {
                padding: 15px;
            }
            h1 {
                font-size: 1.2rem;
            }
            button {
                font-size: 14px;
            }
        }
    </style>
    <!-- Добавлен параметр hl для языка -->
    <script src="https://www.google.com/recaptcha/api.js?hl=ru" async defer></script> 
</head>
<body>
    <div class="container">
        <h1>Пожалуйста, подтвердите, что вы не робот</h1>
        <form id="captchaForm">
            <div class="g-recaptcha" data-sitekey="6LekGs8qAAAAAEot_mA3tPhn4oiBcjCv4UgPyiW0"></div>
            <button type="submit">Перейти</button>
        </form>
    </div>

    <script>
        const form = document.getElementById('captchaForm');
        const redire

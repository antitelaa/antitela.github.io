# antitela.github.io[index.html](https://github.com/user-attachments/files/34131353/index.html)
```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Антитела · метод реальности</title>
    <style>
        /* --- СБРОС --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* --- БАЗА --- */
        body {
            background-color: #080808;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            color: #d0d0d0;
            line-height: 1.4;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
            /* агрессивная текстура + кровавые градиенты */
            background-image:
                radial-gradient(circle at 15% 20%, rgba(200, 0, 30, 0.06) 0%, transparent 35%),
                radial-gradient(circle at 85% 90%, rgba(200, 0, 30, 0.08) 0%, transparent 40%),
                repeating-linear-gradient(
                    45deg,
                    rgba(255, 255, 255, 0.012) 0px,
                    rgba(255, 255, 255, 0.012) 2px,
                    transparent 2px,
                    transparent 8px
                );
            -webkit-font-smoothing: antialiased;
        }

        /* --- КАРТОЧКА --- */
        .card {
            width: 100%;
            max-width: 820px;
            margin: 0 auto;
            padding: 2.75rem 2.25rem 3rem;
            background: rgba(10, 10, 10, 0.92);
            border: 1px solid #202020;
            border-left: 6px solid #b3001b;
            box-shadow:
                0 30px 50px -12px rgba(0, 0, 0, 0.95),
                0 0 0 1px rgba(180, 0, 27, 0.15) inset;
            backdrop-filter: blur(2px);
            animation: reveal 0.5s ease-out;
        }

        @keyframes reveal {
            from { opacity: 0; transform: translateY(12px); }
            to   { opacity: 1; transform: translateY(0); }
        }

        /* --- ЗАГОЛОВОК --- */
        h1 {
            font-size: clamp(3.5rem, 15vw, 6.5rem);
            font-weight: 900;
            line-height: 0.9;
            letter-spacing: -0.04em;
            text-transform: uppercase;
            color: #ffffff;
            margin-bottom: 0.4rem;
            text-shadow:
                3px 3px 0 #5a0010,
                0 0 30px rgba(180, 0, 27, 0.5);
            position: relative;
            display: inline-block;
            padding-bottom: 0.18em;
            word-break: break-word;
        }

        h1::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, #b3001b 0%, #b3001b 45%, #2a0006 100%);
            box-shadow: 0 0 14px #b3001b;
        }

        /* --- ПОДЗАГОЛОВОК --- */
        .subhead {
            font-size: clamp(1.15rem, 4.5vw, 1.7rem);
            font-weight: 700;
            letter-spacing: 0.32em;
            text-transform: uppercase;
            color: #a8a8a8;
            margin-top: 0.9rem;
            margin-bottom: 2.25rem;
            padding-bottom: 1.25rem;
            border-bottom: 1px solid #1e1e1e;
            word-spacing: 0.2em;
            text-shadow: 0 0 10px rgba(255, 40, 60, 0.15);
        }

        .subhead span {
            color: #b3001b;
            font-weight: 800;
            text-shadow: 0 0 12px rgba(180, 0, 27, 0.8);
        }

        /* --- ТЕКСТ ОБО МНЕ --- */
        .about {
            font-size: 1.15rem;
            font-weight: 400;
            line-height: 1.65;
            letter-spacing: 0.015em;
            color: #b8b8b8;
            margin-bottom: 2.75rem;
            padding: 1rem 0 1rem 1.5rem;
            border-left: 3px solid #b3001b;
            background: linear-gradient(90deg, rgba(180, 0, 27, 0.09) 0%, transparent 75%);
            max-width: 92%;
        }

        .about strong {
            color: #ffffff;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.03em;
            background: rgba(180, 0, 27, 0.28);
            padding: 0 0.22em;
        }

        /* --- КНОПКА TELEGRAM --- */
        .tg-button {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.8rem;
            background: #b3001b;
            color: #ffffff;
            text-decoration: none;
            text-transform: uppercase;
            font-weight: 800;
            font-size: clamp(1.15rem, 4vw, 1.5rem);
            letter-spacing: 0.18em;
            padding: 1.4rem 2.5rem;
            width: 100%;
            max-width: 440px;
            border: 1px solid #ff2e4a;
            box-shadow:
                0 8px 0 #390007,
                0 14px 32px rgba(180, 0, 27, 0.45);
            transition: all 0.12s ease;
            position: relative;
            cursor: pointer;
            text-align: center;
            line-height: 1.2;
        }

        .tg-button svg {
            width: 1.5em;
            height: 1.5em;
            flex-shrink: 0;
            transition: transform 0.12s ease;
        }

        /* ховер — резкое, агрессивное движение */
        .tg-button:hover {
            background: #d60021;
            box-shadow:
                0 8px 0 #390007,
                0 18px 38px rgba(230, 0, 35, 0.7);
            transform: translateY(-1px);
            border-color: #ff4d66;
        }

        .tg-button:hover svg {
            transform: translateX(4px) scale(1.05);
        }

        /* актив — вдавливание */
        .tg-button:active {
            transform: translateY(6px);
            box-shadow:
                0 2px 0 #390007,
                0 6px 16px rgba(180, 0, 27, 0.5);
        }

        /* фокус — доступность */
        .tg-button:focus-visible {
            outline: 2px solid #ff4d66;
            outline-offset: 4px;
        }

        /* --- АДАПТИВ --- */
        @media (max-width: 560px) {
            .card {
                padding: 2rem 1.35rem 2.5rem;
                border-left-width: 4px;
            }

            .about {
                font-size: 1.05rem;
                max-width: 100%;
                padding-left: 1rem;
            }

            .tg-button {
                padding: 1.25rem 1.5rem;
                letter-spacing: 0.12em;
                gap: 0.6rem;
            }
        }
    </style>
</head>
<body>
    <main class="card">
        <h1>Антитела</h1>
        <div class="subhead">
            <span>метод</span> реальности
        </div>

        <div class="about">
            Я — <strong>не про мотивацию</strong>. Я про систему, которая работает,
            когда мотивация сдохла. Дисциплина как антитело против хаоса.
            Здесь — спорт, мышление и жёсткая работа над собой.
            Без соплей. Без оправданий. <strong>Только метод</strong>.
        </div>

        <a class="tg-button" href="https://t.me/antitela_official" target="_blank" rel="noopener noreferrer">
            <!-- Иконка Telegram (стилизованная) -->
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
                <path d="M21.9 3.8L2.9 11.2C1.9 11.6 1.9 12.1 2.7 12.3L7.6 13.8L9.7 20.2C9.9 20.8 10.3 21 10.7 20.7L13.4 18.5L18.3 22.1C19.2 22.6 19.8 22.3 20 21.2L22.9 4.7C23.1 3.5 22.5 3 21.9 3.8Z" fill="currentColor"/>
                <path d="M7.6 13.8L18.5 6.8C19.1 6.4 19.7 6.6 19.2 7.1L10.8 14.7L10.5 19.1L7.6 13.8Z" fill="#080808" opacity="0.35"/>
            </svg>
            Перейти в Telegram
        </a>
    </main>
</body>
</html>
```

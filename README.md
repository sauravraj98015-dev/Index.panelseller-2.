# Index.panelseller-2
.<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#05070b">
    <meta name="description" content="Welcome to Panel Seller. Continue to Telegram.">
    <title>Panel Seller | Welcome</title>

    <style>
        :root {
            --bg: #05070b;
            --panel: rgba(10, 14, 22, 0.88);
            --green: #20ff9b;
            --red: #ff3155;
            --white: #ffffff;
            --muted: #a9b4c4;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            min-height: 100%;
            background: var(--bg);
        }

        body {
            min-height: 100vh;
            min-height: 100svh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 24px 15px;
            overflow-x: hidden;
            color: var(--white);
            background:
                radial-gradient(circle at 10% 15%, rgba(255, 49, 85, 0.15), transparent 35%),
                radial-gradient(circle at 90% 85%, rgba(32, 255, 155, 0.13), transparent 35%),
                var(--bg);
            font-family: Inter, system-ui, -apple-system, "Segoe UI", sans-serif;
        }

        /* Animated background */

        .background {
            position: fixed;
            inset: 0;
            z-index: 0;
            overflow: hidden;
            pointer-events: none;
        }

        .background-logo {
            position: absolute;
            width: min(100vw, 750px);
            height: min(100vw, 750px);
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background-image: url("logo.jpg");
            background-size: contain;
            background-position: center;
            background-repeat: no-repeat;
            opacity: 0.13;
            filter: saturate(1.4);
            animation: logoFloat 8s ease-in-out infinite;
        }

        .background::after {
            content: "";
            position: absolute;
            inset: 0;
            background: linear-gradient(
                180deg,
                rgba(5, 7, 11, 0.35),
                rgba(5, 7, 11, 0.82)
            );
        }

        .glow {
            position: absolute;
            width: 260px;
            height: 260px;
            border-radius: 50%;
            filter: blur(100px);
            opacity: 0.25;
            animation: glowMove 8s ease-in-out infinite alternate;
        }

        .glow-red {
            top: 5%;
            left: -100px;
            background: var(--red);
        }

        .glow-green {
            right: -100px;
            bottom: 5%;
            background: var(--green);
            animation-delay: -4s;
        }

        @keyframes logoFloat {
            0%, 100% {
                transform: translate(-50%, -50%) scale(1);
            }

            50% {
                transform: translate(-50%, -50%) scale(1.06);
            }
        }

        @keyframes glowMove {
            from {
                transform: translateY(-15px);
            }

            to {
                transform: translateY(20px);
            }
        }

        /* Main card */

        .container {
            position: relative;
            z-index: 1;
            width: 100%;
            max-width: 440px;
            padding: 1px;
            border-radius: 28px;
            background: linear-gradient(
                135deg,
                var(--red),
                rgba(255, 255, 255, 0.12),
                var(--green)
            );
            box-shadow:
                0 25px 80px rgba(0, 0, 0, 0.6),
                0 0 35px rgba(32, 255, 155, 0.08);
            animation: cardAppear 0.9s ease both;
        }

        .card {
            padding: 30px 23px 24px;
            border-radius: 27px;
            text-align: center;
            background: var(--panel);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
        }

        @keyframes cardAppear {
            from {
                opacity: 0;
                transform: translateY(25px) scale(0.97);
            }

            to {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        /* Logo */

        .logo-wrapper {
            display: inline-block;
            position: relative;
            margin-bottom: 20px;
        }

        .logo-wrapper::before {
            content: "";
            position: absolute;
            inset: -7px;
            border-radius: 28px;
            border: 1px solid rgba(32, 255, 155, 0.5);
            animation: borderPulse 3s ease-in-out infinite;
        }

        .logo {
            display: block;
            width: 125px;
            height: 125px;
            object-fit: cover;
            border-radius: 22px;
            border: 2px solid var(--green);
            box-shadow:
                0 0 20px rgba(32, 255, 155, 0.25),
                0 0 25px rgba(255, 49, 85, 0.15);
        }

        @keyframes borderPulse {
            0%, 100% {
                opacity: 0.45;
                transform: scale(1);
            }

            50% {
                opacity: 1;
                transform: scale(1.05);
            }
        }

        /* Branding */

        .badge {
            display: inline-block;
            padding: 8px 13px;
            margin-bottom: 14px;
            border-radius: 30px;
            border: 1px solid rgba(32, 255, 155, 0.25);
            background: rgba(32, 255, 155, 0.07);
            color: var(--green);
            font-size: 11px;
            font-weight: 800;
            letter-spacing: 1.5px;
        }

        h1 {
            font-size: clamp(30px, 8vw, 38px);
            font-weight: 900;
            letter-spacing: 1px;
            line-height: 1.2;
            margin-bottom: 12px;
            background: linear-gradient(
                90deg,
                #ffffff,
                var(--green),
                #ffffff
            );
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .subtitle {
            max-width: 340px;
            margin: 0 auto 23px;
            color: var(--muted);
            font-size: 14px;
            line-height: 1.8;
        }

        /* Feature cards */

        .features {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 9px;
            margin-bottom: 24px;
        }

        .feature {
            padding: 14px 5px;
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 14px;
            background: rgba(255, 255, 255, 0.035);
            transition:
                transform 0.25s ease,
                border-color 0.25s ease,
                background 0.25s ease;
        }

        .feature:hover {
            transform: translateY(-4px);
            border-color: rgba(32, 255, 155, 0.45);
            background: rgba(32, 255, 155, 0.06);
        }

        .feature-icon {
            display: block;
            margin-bottom: 8px;
            font-size: 22px;
        }

        .feature-text {
            display: block;
            color: #dce4ed;
            font-size: 10px;
            font-weight: 700;
        }

        /* Telegram button */

        .join-button {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            width: 100%;
            padding: 17px 15px;
            border: none;
            border-radius: 14px;
            color: #04110b;
            background: linear-gradient(100deg, var(--green), #8affc9);
            text-decoration: none;
            font-size: 14px;
            font-weight: 900;
            letter-spacing: 0.5px;
            box-shadow: 0 0 25px rgba(32, 255, 155, 0.15);
            transition:
                transform 0.2s ease,
                box-shadow 0.2s ease;
        }

        .join-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 0 35px rgba(32, 255, 155, 0.35);
        }

        .join-button:active {
            transform: scale(0.98);
        }

        .button-arrow {
            font-size: 20px;
        }

        /* Countdown */

        .timer-box {
            margin-top: 24px;
            padding: 19px 15px;
            border-radius: 16px;
            background: rgba(255, 255, 255, 0.035);
            border: 1px solid rgba(255, 255, 255, 0.07);
        }

        .timer-label {
            color: var(--muted);
            font-size: 11px;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .timer-line {
            display: flex;
            justify-content: center;
            align-items: baseline;
            gap: 9px;
            margin: 8px 0 14px;
        }

        .timer {
            color: var(--green);
            font-size: 55px;
            font-weight: 900;
            line-height: 1.1;
            text-shadow: 0 0 25px rgba(32, 255, 155, 0.25);
            font-variant-numeric: tabular-nums;
        }

        .seconds {
            color: var(--muted);
            font-size: 12px;
            font-weight: 800;
            letter-spacing: 2px;
        }

        /* Progress bar */

        .progress-track {
            height: 5px;
            border-radius: 10px;
            overflow: hidden;
            background: rgba(255, 255, 255, 0.08);
        }

        .progress-bar {
            width: 100%;
            height: 100%;
            border-radius: 10px;
            background: linear-gradient(90deg, var(--red), var(--green));
            transform-origin: left;
            animation: progressCountdown 5s linear forwards;
        }

        @keyframes progressCountdown {
            from {
                transform: scaleX(1);
            }

            to {
                transform: scaleX(0);
            }
        }

        /* Manual link and footer */

        .manual-link {
            display: inline-block;
            margin-top: 20px;
            color: var(--green);
            font-size: 13px;
            font-weight: 700;
            text-decoration: none;
        }

        .manual-link:hover {
            text-decoration: underline;
        }

        .footer {
            margin-top: 24px;
            padding-top: 17px;
            border-top: 1px solid rgba(255, 255, 255, 0.09);
            color: #7f8b9d;
            font-size: 11px;
            line-height: 1.8;
        }

        .footer strong {
            color: #dce4ed;
        }

        .noscript {
            margin-top: 15px;
            color: var(--red);
            font-size: 12px;
        }

        /* Responsive layout */

        @media (max-width: 360px) {
            .card {
                padding: 25px 16px 20px;
            }

            .logo {
                width: 105px;
                height: 105px;
            }

            .feature-text {
                font-size: 9px;
            }

            .join-button {
                font-size: 12px;
            }
        }

        @media (prefers-reduced-motion: reduce) {
            *,
            *::before,
            *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }
    </style>
</head>

<body>

    <div class="background" aria-hidden="true">
        <div class="background-logo"></div>
        <div class="glow glow-red"></div>
        <div class="glow glow-green"></div>
    </div>

    <main class="container">
        <section class="card">

            <div class="logo-wrapper">
                <img
                    src="logo.jpg"
                    alt="Panel Seller Logo"
                    class="logo"
                >
            </div>

            <div class="badge">
                ⚡ WELCOME TO PANEL SELLER
            </div>

            <h1>Panel Seller</h1>

            <p class="subtitle">
                Your destination is just one step away.
                <br>
                Get ready and continue to Telegram.
            </p>

            <div class="features">
                <div class="feature">
                    <span class="feature-icon">⚡</span>
                    <span class="feature-text">QUICK ACCESS</span>
                </div>

                <div class="feature">
                    <span class="feature-icon">🚀</span>
                    <span class="feature-text">EASY JOIN</span>
                </div>

                <div class="feature">
                    <span class="feature-icon">📲</span>
                    <span class="feature-text">TELEGRAM</span>
                </div>
            </div>

            <a
                class="join-button"
                id="joinButton"
                href="https://t.me/boost?c=4297286588"
            >
                <span>CONTINUE TO TELEGRAM</span>
                <span class="button-arrow">↗</span>
            </a>

            <div class="timer-box">
                <div class="timer-label">
                    Automatic redirect in
                </div>

                <div class="timer-line">
                    <span class="timer" id="timer" aria-live="off">5</span>
                    <span class="seconds">SECONDS</span>
                </div>

                <div class="progress-track" aria-hidden="true">
                    <div class="progress-bar" id="progressBar"></div>
                </div>
            </div>

            <a
                class="manual-link"
                id="manualLink"
                href="https://t.me/boost?c=4297286588"
            >
                Not redirected? Tap here →
            </a>

            <div class="footer">
                <strong>Panel Seller</strong>
                <br>
                Thanks for visiting. Continue to Telegram whenever you're ready.
            </div>

            <noscript>
                <p class="noscript">
                    JavaScript is disabled. Use the button above to continue.
                </p>
            </noscript>

        </section>
    </main>

    <script>
        (() => {
            "use strict";

            const TELEGRAM_LINK = "https://t.me/boost?c=4297286588";
            const COUNTDOWN_SECONDS = 5;

            const timerElement = document.getElementById("timer");
            const joinButton = document.getElementById("joinButton");
            const manualLink = document.getElementById("manualLink");
            const progressBar = document.getElementById("progressBar");

            // Set Telegram destinations.
            joinButton.href = TELEGRAM_LINK;
            manualLink.href = TELEGRAM_LINK;

            // Initialize the countdown.
            let remaining = COUNTDOWN_SECONDS;
            timerElement.textContent = remaining;

            // Synchronize the progress bar with the countdown.
            progressBar.style.animation = "none";
            void progressBar.offsetWidth;
            progressBar.style.animation =
                `progressCountdown ${COUNTDOWN_SECONDS}s linear forwards`;

            // Automatically redirect after five seconds.
            const countdown = setInterval(() => {
                remaining--;

                timerElement.textContent = Math.max(remaining, 0);

                if (remaining <= 0) {
                    clearInterval(countdown);
                    window.location.replace(TELEGRAM_LINK);
                }
            }, 1000);
        })();
    </script>

</body>
</html>

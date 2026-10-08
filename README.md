<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Consistency Is Key</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html,
        body {
            width: 100%;
            height: 100%;
            background: #000;
            font-family: Arial, Helvetica, sans-serif;
        }

        .poster {
            position: relative;
            width: min(100vw, 760px);
            height: 100vh;
            min-height: 650px;
            margin: auto;
            overflow: hidden;
            background: #111;
        }

        /* Background image */
        .poster-image {
            position: absolute;
            inset: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
            filter:
                grayscale(100%)
                contrast(125%)
                brightness(70%);
            transform: scale(1.01);
        }

        /* Dark cinematic overlay */
        .overlay {
            position: absolute;
            inset: 0;
            background:
                linear-gradient(
                    to bottom,
                    rgba(0,0,0,0.75) 0%,
                    rgba(0,0,0,0.05) 30%,
                    rgba(0,0,0,0.10) 55%,
                    rgba(0,0,0,0.65) 100%
                );
        }

        /* Top left */
        .top-left {
            position: absolute;
            top: 36px;
            left: 35px;

            color: #fff;
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 0.4px;
            text-transform: uppercase;
        }

        /* Top right */
        .top-right {
            position: absolute;
            top: 36px;
            right: 35px;

            color: #fff;
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 0.4px;
            text-transform: uppercase;
        }

        /* Center logo */
        .logo {
            position: absolute;
            top: 34px;
            left: 50%;
            transform: translateX(-50%);

            color: #fff;
            font-size: 24px;
            font-weight: 900;
            font-style: italic;
            letter-spacing: -7px;
        }

        /* Main title */
        .main-title {
            position: absolute;
            top: 50%;
            left: 50%;

            transform: translate(-50%, -50%);

            width: 90%;
            text-align: center;

            color: white;
            font-size: clamp(25px, 5vw, 38px);
            font-weight: 800;
            letter-spacing: -1.5px;
            line-height: 1;
            text-transform: uppercase;

            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }

        /* Bottom navigation */
        .bottom-left,
        .bottom-center,
        .bottom-right {
            position: absolute;
            bottom: 34px;

            color: #fff;
            font-size: 8px;
            font-weight: 700;
            letter-spacing: 0.3px;
            text-transform: uppercase;
        }

        .bottom-left {
            left: 35px;
        }

        .bottom-center {
            left: 50%;
            transform: translateX(-50%);
        }

        .bottom-right {
            right: 35px;
        }

        /* Subtle grain */
        .grain {
            position: absolute;
            inset: 0;
            pointer-events: none;
            opacity: 0.08;

            background-image:
                url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.35'/%3E%3C/svg%3E");

            mix-blend-mode: overlay;
        }

        /* Mobile */
        @media (max-width: 600px) {

            .poster {
                width: 100%;
                height: 100svh;
                min-height: 550px;
            }

            .top-left {
                top: 25px;
                left: 22px;
                font-size: 7px;
            }

            .top-right {
                top: 25px;
                right: 22px;
                font-size: 7px;
            }

            .logo {
                top: 24px;
                font-size: 20px;
            }

            .main-title {
                font-size: 27px;
                letter-spacing: -1px;
            }

            .bottom-left {
                bottom: 24px;
                left: 22px;
                font-size: 7px;
            }

            .bottom-center {
                bottom: 24px;
                font-size: 7px;
            }

            .bottom-right {
                bottom: 24px;
                right: 22px;
                font-size: 7px;
            }
        }
    </style>
</head>

<body>

    <main class="poster">

        <!-- Your image -->
        <img
            class="poster-image"
            src="0491bc4318a756f584036798ae92f405.jpg"
            alt="Consistency Is Key"
        >

        <!-- Dark overlay -->
        <div class="overlay"></div>

        <!-- Top information -->
        <div class="top-left">
            NEW MENTALITIES 2024©
        </div>

        <div class="top-right">
            SEND THIS TO A FRIEND
        </div>

        <!-- Center logo -->
        <div class="logo">
            //
        </div>

        <!-- Main message -->
        <div class="main-title">
            CONSISTENCY IS KEY
        </div>

        <!-- Bottom information -->
        <div class="bottom-left">
            LIKE
        </div>

        <div class="bottom-center">
            COMMENT
        </div>

        <div class="bottom-right">
            BOOKMARK
        </div>

        <!-- Film grain -->
        <div class="grain"></div>

    </main>

</body>
</html>

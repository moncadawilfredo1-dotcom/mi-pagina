```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Descargas - Tu Canal de YouTube</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: white;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        
        .header {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .logo {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            overflow: hidden;
            margin: 0 auto 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 3px solid #ff4d4d;
        }
        
        .logo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #ff0000, #ff4d4d);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: #a0a0c0;
            margin-bottom: 30px;
        }
        
        .downloads-container {
            display: grid;
            gap: 30px;
        }
        
        .download-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        
        .download-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.15);
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        }
        
        .download-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(45deg, #ff0000, #ff4d4d);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
        }
        
        .download-icon i {
            font-size: 35px;
            color: white;
        }
        
        .download-card h2 {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: #fff;
        }
        
        .download-card p {
            color: #b0b0d0;
            margin-bottom: 25px;
            line-height: 1.6;
        }
        
        .buttons-container {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-top: 20px;
        }
        
        .btn {
            padding: 12px 25px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            text-decoration: none;
            border: none;
            text-align: center;
        }
        
        .subscribe-btn {
            background: linear-gradient(45deg, #ff0000, #ff4d4d);
            color: white;
        }
        
        .subscribe-btn:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 20px rgba(255, 0, 0, 0.4);
        }
        
        .download-btn {
            background: linear-gradient(45deg, #4ecdc4, #44a08d);
            color: white;
        }
        
        .download-btn:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 20px rgba(78, 205, 196, 0.4);
        }
        
        .donate-btn {
            background: linear-gradient(45deg, #0070ba, #0096ff);
            color: white;
        }
        
        .donate-btn:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 20px rgba(0, 118, 186, 0.4);
        }
        
        .social-btn {
            padding: 10px 20px;
            font-size: 0.95rem;
            border-radius: 50px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .discord-btn {
            background: linear-gradient(45deg, #5865F2, #7289DA);
            color: white;
        }
        
        .discord-btn:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 20px rgba(88, 101, 242, 0.4);
        }
        
        .tiktok-btn {
            background: linear-gradient(45deg, #000000, #69C9D0);
            color: white;
        }
        
        .tiktok-btn:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .socials-section {
            margin-top: 25px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        .socials-title {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: #ff4d4d;
        }
        
        .socials-buttons {
            display: flex;
            gap: 12px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .donation-section {
            margin-top: 25px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        .donation-title {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: #0096ff;
        }
        
        .footer {
            text-align: center;
            margin-top: 40px;
            color: #8080a0;
            font-size: 0.9rem;
        }
        
        @media (max-width: 600px) {
            h1 {
                font-size: 2rem;
            }
            
            .download-card {
                padding: 20px;
            }
            
            .btn, .social-btn {
                padding: 10px 20px;
                font-size: 0.95rem;
            }
            
            .buttons-container {
                gap: 10px;
            }
            
            .socials-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="logo">
                <img src="https://i.imgur.com/5JZQKzH.jpg" alt="Logo del canal">
            </div>
            <h1>¡Gracias por el Apoyo!</h1>
            <p class="subtitle">Suscríbete y únete a la comunidad para acceder a todo el contenido</p>
        </div>
        
        <div class="downloads-container">
            <div class="download-card">
                <div class="download-icon">
                    <i class="fas fa-mobile-alt"></i>
                </div>
                <h2>Aplicación para Celular</h2>
                <p>Descarga la app oficial para jugar tus juegos Flash favoritos directamente desde tu dispositivo móvil.</p>
                <div class="buttons-container">
                    <a href="https://youtube.com/@player1w.w?si=Vrh-7A2Yrl1NLcDB" target="_blank" class="btn subscribe-btn">
                        <i class="fab fa-youtube"></i> Suscríbete a mi canal
                    </a>
                    <a href="https://play.google.com/store/apps/details?id=com.flasharch.player&pcampaignid=web_share" target="_blank" class="btn download-btn">
                        <i class="fab fa-google-play"></i> Ir a Google Play
                    </a>
                </div>
                <div class="socials-section">
                    <div class="socials-title">¡Únete también en redes!</div>
                    <div class="socials-buttons">
                        <a href="https://discord.gg/MZxMA2cd" target="_blank" class="social-btn discord-btn">
                            <i class="fab fa-discord"></i> Discord
                        </a>
                        <a href="https://www.tiktok.com/@player1w.w?is_from_webapp=1&sender_device=pc" target="_blank" class="social-btn tiktok-btn">
                            <i class="fab fa-tiktok"></i> TikTok
                        </a>
                    </div>
                </div>
                <div class="donation-section">
                    <div class="donation-title">¿Quieres apoyarme?</div>
                    <a href="https://paypal.me/wilfredo10534" target="_blank" class="btn donate-btn">
                        <i class="fab fa-paypal"></i> Donar vía PayPal
                    </a>
                </div>
            </div>
            
            <div class="download-card">
                <div class="download-icon">
                    <i class="fas fa-desktop"></i>
                </div>
                <h2>Juegos Flash Player para PC</h2>
                <p>Colección completa de juegos Flash listos para jugar en tu computadora. ¡Incluye clásicos como Sonny y Superfighters!</p>
                <div class="buttons-container">
                    <a href="https://youtube.com/@player1w.w?si=Vrh-7A2Yrl1NLcDB" target="_blank" class="btn subscribe-btn">
                        <i class="fab fa-youtube"></i> Suscríbete a mi canal
                    </a>
                    <a href="https://www.mediafire.com/file/gtbwdeaa8jf60ok/juegos_flas_PC.rar/file" target="_blank" class="btn download-btn">
                        <i class="fas fa-download"></i> Descargar para PC
                    </a>
                </div>
                <div class="socials-section">
                    <div class="socials-title">¡Únete también en redes!</div>
                    <div class="socials-buttons">
                        <a href="https://discord.gg/MZxMA2cd" target="_blank" class="social-btn discord-btn">
                            <i class="fab fa-discord"></i> Discord
                        </a>
                        <a href="https://www.tiktok.com/@player1w.w?is_from_webapp=1&sender_device=pc" target="_blank" class="social-btn tiktok-btn">
                            <i class="fab fa-tiktok"></i> TikTok
                        </a>
                    </div>
                </div>
                <div class="donation-section">
                    <div class="donation-title">¿Quieres apoyarme?</div>
                    <a href="https://paypal.me/wilfredo10534" target="_blank" class="btn donate-btn">
                        <i class="fab fa-paypal"></i> Donar vía PayPal
                    </a>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <p>© 2026 - Todos los derechos reservados</p>
        </div>
    </div>
</body>
</html>
```

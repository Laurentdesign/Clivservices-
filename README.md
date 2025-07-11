# Clivservices-
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ClivServices - Vos services digitaux premium</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700;900&family=Exo+2:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #0a0a2a;
            --secondary: #00f3ff;
            --accent: #ff00c8;
            --light: #ffffff;
            --dark: #000022;
            --gray: #a0a0c0;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            font-family: 'Exo 2', sans-serif;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }
        
        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 10% 20%, rgba(0, 243, 255, 0.05) 0%, transparent 15%),
                radial-gradient(circle at 90% 80%, rgba(255, 0, 200, 0.05) 0%, transparent 15%),
                linear-gradient(135deg, transparent 49.9%, rgba(0, 243, 255, 0.1) 50%, transparent 50.1%),
                linear-gradient(45deg, transparent 49.9%, rgba(255, 0, 200, 0.1) 50%, transparent 50.1%);
            background-size: 100px 100px;
            z-index: -1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }
        
        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 3.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 15px rgba(0, 243, 255, 0.3);
            letter-spacing: 1px;
        }
        
        .subtitle {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 40px;
            font-weight: 300;
            position: relative;
            display: inline-block;
        }
        
        .subtitle::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            border-radius: 3px;
        }
        
        .services-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 30px;
            margin: 60px 0;
        }
        
        .service-btn {
            width: 100%;
            max-width: 500px;
            padding: 25px;
            border: none;
            border-radius: 15px;
            background: linear-gradient(145deg, rgba(10, 10, 42, 0.9), rgba(0, 0, 34, 0.9));
            color: var(--light);
            font-family: 'Orbitron', sans-serif;
            font-size: 1.5rem;
            font-weight: 500;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2),
                        0 0 20px rgba(0, 243, 255, 0.2),
                        inset 0 0 10px rgba(255, 0, 200, 0.3);
        }
        
        .service-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3),
                        0 0 30px rgba(0, 243, 255, 0.4),
                        inset 0 0 15px rgba(255, 0, 200, 0.5);
        }
        
        .service-btn::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }
        
        .service-btn:hover::before {
            left: 100%;
        }
        
        .service-btn i {
            font-size: 2rem;
            color: var(--secondary);
            transition: all 0.3s ease;
        }
        
        .service-btn:hover i {
            color: var(--accent);
            transform: scale(1.2);
        }
        
        footer {
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
            background: rgba(10, 10, 42, 0.8);
            border-radius: 20px 20px 0 0;
            box-shadow: 0 -5px 20px rgba(0, 0, 0, 0.2);
            color: var(--light);
        }
        
        .contact-text {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--gray);
        }
        
        .whatsapp-contact {
            display: inline-flex;
            align-items: center;
            gap: 15px;
            background: linear-gradient(to right, #25D366, #128C7E);
            padding: 15px 30px;
            border-radius: 50px;
            color: white;
            font-size: 1.4rem;
            text-decoration: none;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: all 0.3s ease;
        }
        
        .whatsapp-contact:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }
        
        .whatsapp-contact i {
            font-size: 2.2rem;
        }
        
        /* Animations */
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(0, 243, 255, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(0, 243, 255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(0, 243, 255, 0); }
        }
        
        /* Loading animation */
        .loader {
            display: none;
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            background: rgba(10, 10, 42, 0.9);
            border-radius: 15px;
            z-index: 10;
            justify-content: center;
            align-items: center;
        }
        
        .loader.active {
            display: flex;
            animation: fadeIn 0.3s;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .spinner {
            width: 50px;
            height: 50px;
            border: 5px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top: 5px solid var(--secondary);
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Service Content */
        .service-content {
            display: none;
            padding: 30px;
            background: rgba(10, 10, 42, 0.95);
            border-radius: 20px;
            margin: 30px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            position: relative;
            overflow: hidden;
        }
        
        .service-content::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
        }
        
        .back-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid var(--secondary);
            color: var(--light);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .back-btn:hover {
            background: var(--secondary);
            transform: rotate(360deg);
        }
        
        .service-title {
            text-align: center;
            color: var(--light);
            font-family: 'Orbitron', sans-serif;
            font-size: 2.2rem;
            margin-bottom: 30px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .logos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 25px;
            margin: 30px 0;
        }
        
        .logo-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 243, 255, 0.2);
        }
        
        .logo-item:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0, 243, 255, 0.2);
            border-color: var(--secondary);
        }
        
        .logo-item i {
            font-size: 3.5rem;
            margin-bottom: 15px;
        }
        
        .logo-item.netflix i { color: #e50914; }
        .logo-item.prime i { color: #00a8e1; }
        .logo-item.disney i { color: #113ccf; }
        .logo-item.crunchyroll i { color: #f47521; }
        .logo-item.fire i { color: #f8c300; }
        .logo-item.cod i { color: #00a2ff; }
        .logo-item.dream i { color: #00cc66; }
        .logo-item.efootball i { color: #ff3333; }
        
        .logo-text {
            color: var(--gray);
            font-size: 0.9rem;
            text-align: center;
        }
        
        .action-btn {
            display: block;
            width: 100%;
            max-width: 300px;
            margin: 40px auto 20px;
            padding: 18px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            border: none;
            border-radius: 50px;
            color: var(--primary);
            font-family: 'Orbitron', sans-serif;
            font-size: 1.3rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            text-decoration: none;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .action-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }
        
        .action-btn i {
            margin-left: 10px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.8rem;
            }
            
            .subtitle {
                font-size: 1.5rem;
            }
            
            .service-btn {
                font-size: 1.3rem;
                padding: 20px;
            }
            
            .logos-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            }
        }
        
        @media (max-width: 480px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .service-btn {
                font-size: 1.1rem;
                padding: 18px;
            }
            
            .logo-item i {
                font-size: 2.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 class="pulse">BIENVENUE SUR CLIV SERVICES</h1>
            <div class="subtitle">COMMENT POUVONS-NOUS VOUS AIDER ?</div>
        </header>
        
        <div class="services-container">
            <div class="service-btn" id="streamingBtn">
                <div class="loader" id="streamingLoader">
                    <div class="spinner"></div>
                </div>
                <i class="fas fa-tv"></i>
                <span>STREAMING</span>
            </div>
            
            <div class="service-btn" id="topupBtn">
                <div class="loader" id="topupLoader">
                    <div class="spinner"></div>
                </div>
                <i class="fas fa-gem"></i>
                <span>TOP UP JEUX MOBILES</span>
            </div>
            
            <div class="service-btn" id="orderBtn">
                <div class="loader" id="orderLoader">
                    <div class="spinner"></div>
                </div>
                <i class="fas fa-shopping-cart"></i>
                <span>COMMANDE EN LIGNE</span>
            </div>
        </div>
        
        <!-- Streaming Content -->
        <div class="service-content" id="streamingContent">
            <button class="back-btn" id="backFromStreaming">
                <i class="fas fa-arrow-left"></i>
            </button>
            <h2 class="service-title">CHOISISSEZ VOTRE PLATEFORME DE STREAMING</h2>
            
            <div class="logos-grid">
                <div class="logo-item netflix">
                    <i class="fab fa-netflix"></i>
                    <span class="logo-text">Netflix</span>
                </div>
                
                <div class="logo-item prime">
                    <i class="fab fa-amazon"></i>
                    <span class="logo-text">Prime Video</span>
                </div>
                
                <div class="logo-item disney">
                    <i class="fab fa-disney"></i>
                    <span class="logo-text">Disney+</span>
                </div>
                
                <div class="logo-item crunchyroll">
                    <i class="fas fa-dragon"></i>
                    <span class="logo-text">Crunchyroll</span>
                </div>
            </div>
            
            <a href="https://wa.me/qr/OJLWDFJRUAFQD1" class="action-btn" target="_blank">
                PRENDRE UN ABONNEMENT <i class="fab fa-whatsapp"></i>
            </a>
        </div>
        
        <!-- Top Up Content -->
        <div class="service-content" id="topupContent">
            <button class="back-btn" id="backFromTopup">
                <i class="fas fa-arrow-left"></i>
            </button>
            <h2 class="service-title">CHOISISSEZ VOTRE JEU</h2>
            
            <div class="logos-grid">
                <div class="logo-item fire">
                    <i class="fas fa-fire"></i>
                    <span class="logo-text">Free Fire</span>
                </div>
                
                <div class="logo-item cod">
                    <i class="fas fa-crosshairs"></i>
                    <span class="logo-text">Call of Duty</span>
                </div>
                
                <div class="logo-item dream">
                    <i class="fas fa-futbol"></i>
                    <span class="logo-text">Dream League</span>
                </div>
                
                <div class="logo-item efootball">
                    <i class="fas fa-gamepad"></i>
                    <span class="logo-text">eFootball 2025</span>
                </div>
            </div>
            
            <a href="https://wa.me/qr/OJLWDFJRUAFQD1" class="action-btn" target="_blank">
                FAIRE TOP UP <i class="fab fa-whatsapp"></i>
            </a>
        </div>
        
        <!-- Order Content -->
        <div class="service-content" id="orderContent">
            <button class="back-btn" id="backFromOrder">
                <i class="fas fa-arrow-left"></i>
            </button>
            <h2 class="service-title">COMMANDE EN LIGNE</h2>
            
            <p style="color: var(--gray); text-align: center; margin: 30px 0; line-height: 1.6;">
                Passer votre commande en ligne et nous vous contacterons pour confirmer les détails et le mode de livraison.
            </p>
            
            <a href="https://wa.me/qr/OJLWDFJRUAFQD1" class="action-btn" target="_blank">
                PLACER UNE COMMANDE <i class="fab fa-whatsapp"></i>
            </a>
        </div>
        
        <footer>
            <div class="contact-text">CONTACTEZ-NOUS SUR</div>
            <a href="https://wa.me/50940998395" class="whatsapp-contact" target="_blank">
                <i class="fab fa-whatsapp"></i>
                +(509) 4099-8395
            </a>
        </footer>
    </div>

    <script>
        // Elements
        const streamingBtn = document.getElementById('streamingBtn');
        const topupBtn = document.getElementById('topupBtn');
        const orderBtn = document.getElementById('orderBtn');
        
        const streamingLoader = document.getElementById('streamingLoader');
        const topupLoader = document.getElementById('topupLoader');
        const orderLoader = document.getElementById('orderLoader');
        
        const streamingContent = document.getElementById('streamingContent');
        const topupContent = document.getElementById('topupContent');
        const orderContent = document.getElementById('orderContent');
        
        const backFromStreaming = document.getElementById('backFromStreaming');
        const backFromTopup = document.getElementById('backFromTopup');
        const backFromOrder = document.getElementById('backFromOrder');
        
        // Function to hide all service content
        function hideAllContent() {
            streamingContent.style.display = 'none';
            topupContent.style.display = 'none';
            orderContent.style.display = 'none';
        }
        
        // Show loading and then content
        function showContent(loader, content) {
            loader.classList.add('active');
            
            setTimeout(() => {
                loader.classList.remove('active');
                hideAllContent();
                content.style.display = 'block';
                
                // Scroll to content
                content.scrollIntoView({ behavior: 'smooth' });
            }, 1000);
        }
        
        // Event Listeners
        streamingBtn.addEventListener('click', () => {
            showContent(streamingLoader, streamingContent);
        });
        
        topupBtn.addEventListener('click', () => {
            showContent(topupLoader, topupContent);
        });
        
        orderBtn.addEventListener('click', () => {
            showContent(orderLoader, orderContent);
        });
        
        // Back buttons
        backFromStreaming.addEventListener('click', () => {
            hideAllContent();
            document.querySelector('header').scrollIntoView({ behavior: 'smooth' });
        });
        
        backFromTopup.addEventListener('click', () => {
            hideAllContent();
            document.querySelector('header').scrollIntoView({ behavior: 'smooth' });
        });
        
        backFromOrder.addEventListener('click', () => {
            hideAllContent();
            document.querySelector('header').scrollIntoView({ behavior: 'smooth' });
        });
        
        // Add hover effect to logo items
        const logoItems = document.querySelectorAll('.logo-item');
        logoItems.forEach(item => {
            item.addEventListener('mouseenter', () => {
                const icon = item.querySelector('i');
                icon.style.transform = 'scale(1.2)';
                icon.style.transition = 'transform 0.3s ease';
            });
            
            item.addEventListener('mouseleave', () => {
                const icon = item.querySelector('i');
                icon.style.transform = 'scale(1)';
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ClivServices - Vos services digitaux premium</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700;900&family=Exo+2:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #0a0a2a;
            --secondary: #00f3ff;
            --accent: #ff00c8;
            --light: #ffffff;
            --dark: #000022;
            --gray: #a0a0c0;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            font-family: 'Exo 2', sans-serif;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }
        
        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 10% 20%, rgba(0, 243, 255, 0.05) 0%, transparent 15%),
                radial-gradient(circle at 90% 80%, rgba(255, 0, 200, 0.05) 0%, transparent 15%),
                linear-gradient(135deg, transparent 49.9%, rgba(0, 243, 255, 0.1) 50%, transparent 50.1%),
                linear-gradient(45deg, transparent 49.9%, rgba(255, 0, 200, 0.1) 50%, transparent 50.1%);
            background-size: 100px 100px;
            z-index: -1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }
        
        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 3.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 15px rgba(0, 243, 255, 0.3);
            letter-spacing: 1px;
        }
        
        .subtitle {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 40px;
            font-weight: 300;
            position: relative;
            display: inline-block;
        }
        
        .subtitle::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            border-radius: 3px;
        }
        
        .services-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 30px;
            margin: 60px 0;
        }
        
        .service-btn {
            width: 100%;
            max-width: 500px;
            padding: 25px;
            border: none;
            border-radius: 15px;
            background: linear-gradient(145deg, rgba(10, 10, 42, 0.9), rgba(0, 0, 34, 0.9));
            color: var(--light);
            font-family: 'Orbitron', sans-serif;
            font-size: 1.5rem;
            font-weight: 500;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2),
                        0 0 20px rgba(0, 243, 255, 0.2),
                        inset 0 0 10px rgba(255, 0, 200, 0.3);
        }
        
        .service-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3),
                        0 0 30px rgba(0, 243, 255, 0.4),
                        inset 0 0 15px rgba(255, 0, 200, 0.5);
        }
        
        .service-btn::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }
        
        .service-btn:hover::before {
            left: 100%;
        }
        
        .service-btn i {
            font-size: 2rem;
            color: var(--secondary);
            transition: all 0.3s ease;
        }
        
        .service-btn:hover i {
            color: var(--accent);
            transform: scale(1.2);
        }
        
        footer {
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
            background: rgba(10, 10, 42, 0.8);
            border-radius: 20px 20px 0 0;
            box-shadow: 0 -5px 20px rgba(0, 0, 0, 0.2);
            color: var(--light);
        }
        
        .contact-text {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--gray);
        }
        
        .whatsapp-contact {
            display: inline-flex;
            align-items: center;
            gap: 15px;
            background: linear-gradient(to right, #25D366, #128C7E);
            padding: 15px 30px;
            border-radius: 50px;
            color: white;
            font-size: 1.4rem;
            text-decoration: none;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: all 0.3s ease;
        }
        
        .whatsapp-contact:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }
        
        .whatsapp-contact i {
            font-size: 2.2rem;
        }
        
        /* Animations */
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(0, 243, 255, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(0, 243, 255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(0, 243, 255, 0); }
        }
        
        /* Loading animation */
        .loader {
            display: none;
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            background: rgba(10, 10, 42, 0.9);
            border-radius: 15px;
            z-index: 10;
            justify-content: center;
            align-items: center;
        }
        
        .loader.active {
            display: flex;
            animation: fadeIn 0.3s;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .spinner {
            width: 50px;
            height: 50px;
            border: 5px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top: 5px solid var(--secondary);
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Service Content */
        .service-content {
            display: none;
            padding: 30px;
            background: rgba(10, 10, 42, 0.95);
            border-radius: 20px;
            margin: 30px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            position: relative;
            overflow: hidden;
        }
        
        .service-content::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
        }
        
        .back-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid var(--secondary);
            color: var(--light);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .back-btn:hover {
            background: var(--secondary);
            transform: rotate(360deg);
        }
        
        .service-title {
            text-align: center;
            color: var(--light);
            font-family: 'Orbitron', sans-serif;
            font-size: 2.2rem;
            margin-bottom: 30px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .logos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 25px;
            margin: 30px 0;
        }
        
        .logo-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 243, 255, 0.2);
        }
        
        .logo-item:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0, 243, 255, 0.2);
            border-color: var(--secondary);
        }
        
        .logo-item i {
            font-size: 3.5rem;
            margin-bottom: 15px;
        }
        
        .logo-item.netflix i { color: #e50914; }
        .logo-item.prime i { color: #00a8e1; }
        .logo-item.disney i { color: #113ccf; }
        .logo-item.crunchyroll i { color: #f47521; }
        .logo-item.fire i { color: #f8c300; }
        .logo-item.cod i { color: #00a2ff; }
        .logo-item.dream i { color: #00cc66; }
        .logo-item.efootball i { color: #ff3333; }
        
        .logo-text {
            color: var(--gray);
            font-size: 0.9rem;
            text-align: center;
        }
        
        .action-btn {
            display: block;
            width: 100%;
            max-width: 300px;
            margin: 40px auto 20px;
            padding: 18px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            border: none;
            border-radius: 50px;
            color: var(--primary);
            font-family: 'Orbitron', sans-serif;
            font-size: 1.3rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            text-decoration: none;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .action-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }
        
        .action-btn i {
            margin-left: 10px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.8rem;
            }
            
            .subtitle {
                font-size: 1.5rem;
            }
            
            .service-btn {
                font-size: 1.3rem;
                padding: 20px;
            }
            
            .logos-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            }
        }
        
        @media (max-width: 480px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .service-btn {
                font-size: 1.1rem;
                padding: 18px;
            }
            
            .logo-item i {
                font-size: 2.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 class="pulse">BIENVENUE SUR CLIV SERVICES</h1>
            <div class="subtitle">COMMENT POUVONS-NOUS VOUS AIDER ?</div>
        </header>
        
        <div class="services-container">
            <div class="service-btn" id="streamingBtn">
                <div class="loader" id="streamingLoader">
                    <div class="spinner"></div>
                </div>
                <i class="fas fa-tv"></i>
                <span>STREAMING</span>
            </div>
            
            <div class="service-btn" id="topupBtn">
                <div class="loader" id="topupLoader">
                    <div class="spinner"></div>
                </div>
                <i class="fas fa-gem"></i>
                <span>TOP UP JEUX MOBILES</span>
            </div>
            
            <div class="service-btn" id="orderBtn">
                <div class="loader" id="orderLoader">
                    <div class="spinner"></div>
                </div>
                <i class="fas fa-shopping-cart"></i>
                <span>COMMANDE EN LIGNE</span>
            </div>
        </div>
        
        <!-- Streaming Content -->
        <div class="service-content" id="streamingContent">
            <button class="back-btn" id="backFromStreaming">
                <i class="fas fa-arrow-left"></i>
            </button>
            <h2 class="service-title">CHOISISSEZ VOTRE PLATEFORME DE STREAMING</h2>
            
            <div class="logos-grid">
                <div class="logo-item netflix">
                    <i class="fab fa-netflix"></i>
                    <span class="logo-text">Netflix</span>
                </div>
                
                <div class="logo-item prime">
                    <i class="fab fa-amazon"></i>
                    <span class="logo-text">Prime Video</span>
                </div>
                
                <div class="logo-item disney">
                    <i class="fab fa-disney"></i>
                    <span class="logo-text">Disney+</span>
                </div>
                
                <div class="logo-item crunchyroll">
                    <i class="fas fa-dragon"></i>
                    <span class="logo-text">Crunchyroll</span>
                </div>
            </div>
            
            <a href="https://wa.me/qr/OJLWDFJRUAFQD1" class="action-btn" target="_blank">
                PRENDRE UN ABONNEMENT <i class="fab fa-whatsapp"></i>
            </a>
        </div>
        
        <!-- Top Up Content -->
        <div class="service-content" id="topupContent">
            <button class="back-btn" id="backFromTopup">
                <i class="fas fa-arrow-left"></i>
            </button>
            <h2 class="service-title">CHOISISSEZ VOTRE JEU</h2>
            
            <div class="logos-grid">
                <div class="logo-item fire">
                    <i class="fas fa-fire"></i>
                    <span class="logo-text">Free Fire</span>
                </div>
                
                <div class="logo-item cod">
                    <i class="fas fa-crosshairs"></i>
                    <span class="logo-text">Call of Duty</span>
                </div>
                
                <div class="logo-item dream">
                    <i class="fas fa-futbol"></i>
                    <span class="logo-text">Dream League</span>
                </div>
                
                <div class="logo-item efootball">
                    <i class="fas fa-gamepad"></i>
                    <span class="logo-text">eFootball 2025</span>
                </div>
            </div>
            
            <a href="https://wa.me/qr/OJLWDFJRUAFQD1" class="action-btn" target="_blank">
                FAIRE TOP UP <i class="fab fa-whatsapp"></i>
            </a>
        </div>
        
        <!-- Order Content -->
        <div class="service-content" id="orderContent">
            <button class="back-btn" id="backFromOrder">
                <i class="fas fa-arrow-left"></i>
            </button>
            <h2 class="service-title">COMMANDE EN LIGNE</h2>
            
            <p style="color: var(--gray); text-align: center; margin: 30px 0; line-height: 1.6;">
                Passer votre commande en ligne et nous vous contacterons pour confirmer les détails et le mode de livraison.
            </p>
            
            <a href="https://wa.me/qr/OJLWDFJRUAFQD1" class="action-btn" target="_blank">
                PLACER UNE COMMANDE <i class="fab fa-whatsapp"></i>
            </a>
        </div>
        
        <footer>
            <div class="contact-text">CONTACTEZ-NOUS SUR</div>
            <a href="https://wa.me/50940998395" class="whatsapp-contact" target="_blank">
                <i class="fab fa-whatsapp"></i>
                +(509) 4099-8395
            </a>
        </footer>
    </div>

    <script>
        // Elements
        const streamingBtn = document.getElementById('streamingBtn');
        const topupBtn = document.getElementById('topupBtn');
        const orderBtn = document.getElementById('orderBtn');
        
        const streamingLoader = document.getElementById('streamingLoader');
        const topupLoader = document.getElementById('topupLoader');
        const orderLoader = document.getElementById('orderLoader');
        
        const streamingContent = document.getElementById('streamingContent');
        const topupContent = document.getElementById('topupContent');
        const orderContent = document.getElementById('orderContent');
        
        const backFromStreaming = document.getElementById('backFromStreaming');
        const backFromTopup = document.getElementById('backFromTopup');
        const backFromOrder = document.getElementById('backFromOrder');
        
        // Function to hide all service content
        function hideAllContent() {
            streamingContent.style.display = 'none';
            topupContent.style.display = 'none';
            orderContent.style.display = 'none';
        }
        
        // Show loading and then content
        function showContent(loader, content) {
            loader.classList.add('active');
            
            setTimeout(() => {
                loader.classList.remove('active');
                hideAllContent();
                content.style.display = 'block';
                
                // Scroll to content
                content.scrollIntoView({ behavior: 'smooth' });
            }, 1000);
        }
        
        // Event Listeners
        streamingBtn.addEventListener('click', () => {
            showContent(streamingLoader, streamingContent);
        });
        
        topupBtn.addEventListener('click', () => {
            showContent(topupLoader, topupContent);
        });
        
        orderBtn.addEventListener('click', () => {
            showContent(orderLoader, orderContent);
        });
        
        // Back buttons
        backFromStreaming.addEventListener('click', () => {
            hideAllContent();
            document.querySelector('header').scrollIntoView({ behavior: 'smooth' });
        });
        
        backFromTopup.addEventListener('click', () => {
            hideAllContent();
            document.querySelector('header').scrollIntoView({ behavior: 'smooth' });
        });
        
        backFromOrder.addEventListener('click', () => {
            hideAllContent();
            document.querySelector('header').scrollIntoView({ behavior: 'smooth' });
        });
        
        // Add hover effect to logo items
        const logoItems = document.querySelectorAll('.logo-item');
        logoItems.forEach(item => {
            item.addEventListener('mouseenter', () => {
                const icon = item.querySelector('i');
                icon.style.transform = 'scale(1.2)';
                icon.style.transition = 'transform 0.3s ease';
            });
            
            item.addEventListener('mouseleave', () => {
                const icon = item.querySelector('i');
                icon.style.transform = 'scale(1)';
            });
        });
    </script>
</body>
</html>

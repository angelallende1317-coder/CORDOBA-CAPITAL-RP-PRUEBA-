<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Córdoba Capital RP | Oficial</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --cba-rojo: #C83338;
            --cba-blanco: #FFFFFF;
            --cba-azul: #006699;
            --accent: #ffca28;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #000;
            color: white;
            margin: 0;
            overflow-x: hidden;
        }

        .hero-bg {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('bandera.jpg');
            background-size: cover;
            background-position: center;
            z-index: -1;
        }

        /* STICKERS */
        .sticker-v {
            position: fixed;
            z-index: 1000;
            display: flex;
            flex-direction: column;
            align-items: center;
            animation: float 5s ease-in-out infinite;
        }
        .fernet-v { bottom: 40px; left: 40px; color: #3d1b10; transform: rotate(-15deg); }
        .coca-v { top: 40px; right: 40px; color: #e41e26; transform: rotate(15deg); }
        
        .sticker-label {
            font-size: 0.9rem; background: white; color: black; padding: 4px 12px;
            border-radius: 5px; margin-top: -10px; border: 2px solid black; font-weight: 900;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(-10deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        header {
            height: 70vh; /* Más alto para que luzca el título */
            display: flex; flex-direction: column;
            justify-content: center; align-items: center; text-align: center; padding: 20px;
        }

        /* EL TITULO AHORA ES GIGANTE */
        .titulo-cba {
            font-size: clamp(5rem, 25vw, 15rem); /* Aumentado a lo loco */
            font-weight: 1000; 
            margin: 0;
            line-height: 0.8;
            letter-spacing: -5px;
            background: linear-gradient(to right, var(--cba-rojo) 33%, var(--cba-blanco) 33%, var(--cba-blanco) 66%, var(--cba-azul) 66%);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 0 40px rgba(0,0,0,0.9));
            text-transform: uppercase;
        }

        .sub-titulo {
            font-size: clamp(2rem, 6vw, 4rem); /* Capital RP más grande */
            letter-spacing: 15px; 
            font-weight: 200; 
            margin: 20px 0 0 0;
            color: var(--cba-blanco);
            text-shadow: 2px 5px 15px rgba(0,0,0,0.8);
        }

        .card-valen {
            background: rgba(0, 0, 0, 0.85); border: 3px solid var(--accent);
            border-radius: 30px; padding: 40px; max-width: 500px; 
            margin: -80px auto 50px; text-align: center; backdrop-filter: blur(15px);
            box-shadow: 0 10px 40px rgba(0,0,0,0.7);
        }

        .card-valen h2 { font-size: 3rem; margin: 10px 0; }

        .facciones-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px; padding: 0 5% 100px;
        }

        .f-card {
            background: rgba(255,255,255,0.07); border-radius: 25px; height: 250px;
            position: relative; overflow: hidden; border: 1px solid rgba(255,255,255,0.15);
            transition: 0.4s ease;
        }

        .f-card:hover { transform: translateY(-15px); background: rgba(255,255,255,0.1); }

        .f-info i { font-size: 4.5rem; }
        .f-info h3 { font-size: 2rem; }

        .f-jefe h3 { font-size: 2.5rem; font-weight: 900; }

        #music-btn {
            position: fixed; bottom: 30px; right: 30px;
            background: var(--accent); color: #000; padding: 20px 30px;
            border-radius: 60px; font-size: 1.2rem; font-weight: 900;
            cursor: pointer; z-index: 9999; border: none;
            display: flex; align-items: center; gap: 15px;
            box-shadow: 0 5px 25px rgba(255,202,40,0.6);
        }

        .discord-btn {
            background: #5865F2; color: white; padding: 25px 55px;
            border-radius: 15px; text-decoration: none; font-weight: 900;
            font-size: 1.5rem; display: inline-block; margin-bottom: 80px;
            transition: 0.3s;
        }
    </style>
</head>
<body>

<div class="hero-bg"></div>

<button id="music-btn" onclick="controlarMusica()">
    <i id="icon-m" class="fas fa-play"></i> 
    <span id="text-m">PONER CUARTETO</span>
</button>

<div class="sticker-v fernet-v">
    <i class="fas fa-wine-bottle fa-5x"></i>
    <div class="sticker-label">FERNET</div>
</div>
<div class="sticker-v coca-v">
    <i class="fas fa-glass-whiskey fa-5x"></i>
    <div class="sticker-label">COCA COLA</div>
</div>

<header>
    <h1 class="titulo-cba">CÓRDOBA</h1>
    <h2 class="sub-titulo">CAPITAL RP</h2>
</header>

<div class="card-valen">
    <i class="fas fa-crown" style="color: var(--accent); font-size: 4rem;"></i>
    <h2 style="text-transform: uppercase; letter-spacing: 5px;">VALEN</h2>
    <p style="color: var(--accent); font-weight: bold; font-size: 1.4rem; letter-spacing: 4px;">FUNDADOR</p>
    <p style="color: #2ecc71; font-weight: 900; margin-top: 20px; background: rgba(46, 204, 113, 0.15); padding: 8px 20px; border-radius: 12px; display: inline-block; font-size: 1.1rem;">
        <i class="fas fa-circle"></i> FUNDADOR ACTIVO
    </p>
</div>

<div style="text-align: center;">
    <a href="#" class="discord-btn"><i class="fab fa-discord"></i> ENTRAR AL DISCORD</a>
</div>

<div class="facciones-grid">
    <div class="f-card" style="border-bottom: 7px solid #0056b3;">
        <div class="f-info"><i class="fas fa-shield-halved"></i><h3>Policía de Córdoba</h3></div>
        <div class="f-jefe" style="background: #0056b3;"><p>JEFE DE FACCIÓN</p><h3>VALEN</h3></div>
    </div>
    <div class="f-card" style="border-bottom: 7px solid #002244;">
        <div class="f-info"><i class="fas fa-building-shield"></i><h3>Policía Federal</h3></div>
        <div class="f-jefe" style="background: #002244;"><p>JEFE DE FACCIÓN</p><h3>LAUTARO</h3></div>
    </div>
    <div class="f-card" style="border-bottom: 7px solid #ff6600;">
        <div class="f-info"><i class="fas fa-anchor"></i><h3>Prefectura</h3></div>
        <div class="f-jefe" style="background: #ff6600;"><p>JEFE DE FACCIÓN</p><h3>BENJAMÍN</h3></div>
    </div>
    <div class="f-card" style="border-bottom: 7px solid #d32f2f;">
        <div class="f-info"><i class="fas fa-fire"></i><h3>Bomberos</h3></div>
        <div class="f-jefe" style="background: #d32f2f;"><p>JEFE DE FACCIÓN</p><h3>[Pendiente]</h3></div>
    </div>
    <div class="f-card" style="border-bottom: 7px solid #28a745;">
        <div class="f-info"><i class="fas fa-ambulance"></i><h3>107 Cordobés</h3></div>
        <div class="f-jefe" style="background: #28a745;"><p>JEFE DE FACCIÓN</p><h3>ISA</h3></div>
    </div>
    <div class="f-card" style="border-bottom: 7px solid #f1c40f;">
        <div class="f-info"><i class="fas fa-car-side" style="color: #f1c40f;"></i><h3>Seguridad Vial</h3></div>
        <div class="f-jefe" style="background: #f1c40f; color: black;"><p>JEFE DE FACCIÓN</p><h3>ALAN</h3></div>
    </div>
    <div class="f-card" style="border-bottom: 7px solid #7f8c8d;">
        <div class="f-info"><i class="fas fa-user-shield"></i><h3>Guardia Local</h3></div>
        <div class="f-jefe" style="background: #7f8c8d;"><p>JEFE DE FACCIÓN</p><h3>IAN</h3></div>
    </div>
</div>

<audio id="musica" crossorigin="anonymous">
    <source src="https://sc.mvy.com.ar:9964/stream" type="audio/mpeg">
</audio>

<script>
    const player = document.getElementById("musica");
    const btnText = document.getElementById("text-m");
    const btnIcon = document.getElementById("icon-m");
    player.volume = 0.20;

    function controlarMusica() {
        if (player.paused) {
            player.play().then(() => {
                btnText.innerText = "PAUSAR";
                btnIcon.classList.replace("fa-play", "fa-pause");
            }).catch(e => console.log("Error"));
        } else {
            player.pause();
            btnText.innerText = "PONER CUARTETO";
            btnIcon.classList.replace("fa-pause", "fa-play");
        }
    }
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Música Retro y Más</title>
  <link href="https://fonts.googleapis.com/css2?family=Tilt+Neon&display=swap" rel="stylesheet" />
  <style>
    body {
      background-color: black;
      color: #39ff14;
      font-family: 'Tilt Neon', cursive;
      text-align: center;
      padding: 40px;
    }
    h1 {
      font-size: 60px;
      text-shadow: 0 0 10px #39ff14, 0 0 20px #39ff14;
    }
    h2 {
      margin-top: 40px;
      text-shadow: 0 0 8px #39ff14;
      cursor: pointer;
    }
    h3 {
      margin-top: 30px;
      text-shadow: 0 0 6px #39ff14;
    }
    #imagen-led {
      display: inline-block;
      padding: 10px;
      border: 6px solid #39ff14;
      border-radius: 10px;
      box-shadow: 0 0 25px #39ff14;
      transition: box-shadow 0.2s ease, border-color 0.2s ease;
    }
    #imagen-led img {
      border-radius: 8px;
      width: 400px;
    }
    audio {
      margin: 15px auto;
      filter: drop-shadow(0 0 8px #39ff14);
    }
    #titulo-cancion {
      margin-top: 10px;
      font-size: 20px;
      text-shadow: 0 0 6px #39ff14;
    }
    button {
      background: transparent;
      border: 2px solid #39ff14;
      color: #39ff14;
      font-family: 'Tilt Neon', cursive;
      font-size: 18px;
      margin: 6px 8px;
      padding: 6px 20px;
      cursor: pointer;
      border-radius: 5px;
      text-shadow: 0 0 5px #39ff14;
    }
    button:hover {
      background-color: #39ff14;
      color: black;
      text-shadow: none;
    }
    a {
      color: #39ff14;
      text-decoration: none;
      font-weight: bold;
      text-shadow: 0 0 5px #39ff14;
    }
    a:hover {
      color: white;
      text-shadow: 0 0 10px white;
    }
    .cancion-fila {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 12px;
      margin-bottom: 10px;
      flex-wrap: wrap;
    }
    .cancion-fila span {
      font-size: 20px;
      cursor: pointer;
      text-shadow: 0 0 5px #39ff14;
    }
    .cancion-fila span:hover {
      color: white;
      transform: scale(1.05);
      text-shadow: 0 0 10px white;
    }
    .boton-descarga {
      text-decoration: none;
      color: #39ff14;
      border: 1px solid #39ff14;
      padding: 4px 10px;
      border-radius: 5px;
      font-size: 16px;
      font-family: 'Tilt Neon', cursive;
      text-shadow: 0 0 5px #39ff14;
    }
    .boton-descarga:hover {
      background-color: #39ff14;
      color: black;
      text-shadow: none;
    }
  </style>
</head>
<body>
  <h1>¡Bienvenidos a Música Retro y Más!</h1>
  <p>Hola mundo!!!</p>
  <div id="imagen-led">
    <img src="elneo2xs.PNG" alt="Mi imagen personal" />
  </div>
<div style="text-align: right; margin-top: 10px; padding: 10px;">
  <input
    type="text"
    id="buscador"
    placeholder="Buscar..."
    oninput="buscarCanciones()"
    style="padding: 6px 12px; font-size: 14px; border-radius: 5px;
           border: 1px solid #39ff14; background: #111; color: #39ff14;
           box-shadow: 0 0 8px #39ff14;"
  />
</div>
  <h2 onclick="toggleMenu()">🎶 Música</h2>
  <div id="menu-musica" style="display: none;">
    <button onclick="mostrarCategoria('angel canales')">Angel Canales</button>
    <button onclick="mostrarCategoria('grupo abba')">Grupo abba</button>
    <button onclick="mostrarCategoria('grupo bota')">Grupo bota</button>
    <button onclick="mostrarCategoria('changa')">Changa</button>
    <button onclick="mostrarCategoria('chatarritas')">Chatarritas</button>
    <button onclick="mostrarCategoria('chayanne')">Chayanne</button>
    <button onclick="mostrarCategoria('grupo niche')">Grupo niche</button>
    <button onclick="mostrarCategoria('yoe arroyo')">Yoe arroyo</button>
    <button onclick="mostrarCategoria('juan gabriel')">Juan Gabriel</button>
    <button onclick="mostrarCategoria('julio iglesias')">Julio Iglesias</button>
    <button onclick="mostrarCategoria('llaneras')">LLaneras</button>
    <button onclick="mostrarCategoria('los angeles negros')">Los Angeles Negros</button>
    <button onclick="mostrarCategoria('los blancos de maracaibo')">Los Blancos de Maracaibo</button>
    <button onclick="mostrarCategoria('los corraleros de majagual')">Los corraleros de Majagual</button>
    <button onclick="mostrarCategoria('los hermanos lebron')">Los hermanos Lebron</button>
    <button onclick="mostrarCategoria('los melodicoss')">Los Melodicos</button>
    <button onclick="mostrarCategoria('los pasteles verdes')">Los pasteles verdes</button>
    <button onclick="mostrarCategoria('Maelo Ruiz')">Maelo Ruiz</button>
    <button onclick="mostrarCategoria('micaela')">Sonora Carrueseles</button>
    <button onclick="mostrarCategoria('michael jackson')">Michael Jackson</button>
    <button onclick="mostrarCategoria('oscar de leon dimension latina')">Oscar de leon</button>
    <button onclick="mostrarCategoria('Oscar Santa')">Oscar Santana</button>
    <button onclick="mostrarCategoria('pastor lopez')">Pastor Lopez</button>
    <button onclick="mostrarCategoria('pete conde rodriguez')">Pete Conde Rodriguez</button>
    <button onclick="mostrarCategoria('piero')">Piero</button>
    <button onclick="mostrarCategoria('Renovacion vallenata')">Renovacion Vallenata</button>
    <button onclick="mostrarCategoria('Roberto Blades')">Roberto Blades</button>
    <button onclick="mostrarCategoria('ruben blades')">Ruben Blades</button>
    <button onclick="mostrarCategoria('Survivor')">Survivor</button>
    <button onclick="mostrarCategoria('tambor')">Tambor</button>
    <button onclick="mostrarCategoria('variados')">Variados</button>
    <button onclick="mostrarCategoria('vicente fernandez')">Vicente Fernandez</button>
    <button onclick="mostrarCategoria('contrapunteo venezolano')">Contrapunteo</button>
    <button onclick="mostrarCategoria('el gran combo de puerto rico')">El Gran Combo</button>
    <button onclick="mostrarCategoria('fruko')">Fruko</button>
    <button onclick="mostrarCategoria('Gilberto santa rosa')">Gilberto S. Rosa</button>
  </div>

  <div id="contenedor-musica"></div>

  <h2>Sigueme en</h2>
  <ul>
    <li><a href="https://www.tiktok.com/@bruwolf13" target="_blank">TikTok</a></li>
  </ul>
<script>
  const categorias = {
  "angel canales": [
    {
      "nombre": "A Usted [k-nj7uONgg0]",
      "ruta": "música/angel canales/A Usted [k-nj7uONgg0].mp3"
    },
    {
      "nombre": "Angel Canales - Sol de Mi Vida (Audio Oficial) [ICJ3zjFcxHg] (1)",
      "ruta": "música/angel canales/Angel Canales - Sol de Mi Vida (Audio Oficial) [ICJ3zjFcxHg] (1).mp3"
    },
    {
      "nombre": "Angel Canales - Nadie como tu [W31wRDPXO1Q]",
      "ruta": "música/angel canales/Angel Canales - Nadie como tu [W31wRDPXO1Q].mp3"
    },
    {
      "nombre": "Angel Canales - Sol de Mi Vida (Audio Oficial) [ICJ3zjFcxHg]",
      "ruta": "música/angel canales/Angel Canales - Sol de Mi Vida (Audio Oficial) [ICJ3zjFcxHg].mp3"
    },
    {
      "nombre": "ANA ISAOCO - ANGEL CANALES [eX7uWNZMLdU]",
      "ruta": "música/angel canales/ANA ISAOCO - ANGEL CANALES [eX7uWNZMLdU].mp3"
    },
    {
      "nombre": "El Cantante y La Orquesta [81aZs3O4VR8]",
      "ruta": "música/angel canales/El Cantante y La Orquesta [81aZs3O4VR8].mp3"
    },
    {
      "nombre": "GUANTANAMO - ANGEL CANALES [RUxRPY0hXaA]",
      "ruta": "música/angel canales/GUANTANAMO - ANGEL CANALES [RUxRPY0hXaA].mp3"
    },
    {
      "nombre": "BOMBA CARAMBOMBA - ANGEL CANALES [JHBFrfYGBlY]",
      "ruta": "música/angel canales/BOMBA CARAMBOMBA - ANGEL CANALES [JHBFrfYGBlY].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - ANGEL CANALES - EL CANTANTE Y LA ORQUESTA (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - ANGEL CANALES - EL CANTANTE Y LA ORQUESTA (320 KBps).mp3"
    },
    {
      "nombre": "FARO DE LUZ - ANGEL CANALES [Rf4bv0n0als]",
      "ruta": "música/angel canales/FARO DE LUZ - ANGEL CANALES [Rf4bv0n0als].mp3"
    },
    {
      "nombre": "Saraguay Santoja [qjg2cJk4IUM]",
      "ruta": "música/angel canales/Saraguay Santoja [qjg2cJk4IUM].mp3"
    },
    {
      "nombre": "Tenemos Que Echar Pa'Lante Angel Canales.wmv [pUsgVdZNn_0]",
      "ruta": "música/angel canales/Tenemos Que Echar Pa'Lante Angel Canales.wmv [pUsgVdZNn_0].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Angel Canales - Lejos de Ti (Audio Oficial) (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - Angel Canales - Lejos de Ti (Audio Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "La vida es una caja de sorpresa [lG5PFs--6YA]",
      "ruta": "música/angel canales/La vida es una caja de sorpresa [lG5PFs--6YA].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Angel Canales - Aguardiente (Audio Oficial) (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - Angel Canales - Aguardiente (Audio Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Angel Canales - Mi Irmita (Audio Oficial) (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - Angel Canales - Mi Irmita (Audio Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Angel Canales - Tiene Sabor (Audio Oficial) (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - Angel Canales - Tiene Sabor (Audio Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Sabor Los Rumberos Nuevos - Angel Canales Y Su Orquesta Sabor (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - Sabor Los Rumberos Nuevos - Angel Canales Y Su Orquesta Sabor (320 KBps).mp3"
    },
    {
      "nombre": "La Sombra, Angel Canales.wmv [9ShRKKkM7lM]",
      "ruta": "música/angel canales/La Sombra, Angel Canales.wmv [9ShRKKkM7lM].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Ángel Canales - Perico Macona (Official Audio) (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - Ángel Canales - Perico Macona (Official Audio) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - ️El Barrio - Angel Canales (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - ️El Barrio - Angel Canales (320 KBps).mp3"
    },
    {
      "nombre": "Ángel Canales - Hace Tiempo (Official Audio) [_mrAESYCV3I]",
      "ruta": "música/angel canales/Ángel Canales - Hace Tiempo (Official Audio) [_mrAESYCV3I].mp3"
    },
    {
      "nombre": "Ángel Canales - Perico Macona (Official Audio) [GC8a-evaC5g]",
      "ruta": "música/angel canales/Ángel Canales - Perico Macona (Official Audio) [GC8a-evaC5g].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Angel Canales - Brujería (Audio Oficial) (320 KBps)",
      "ruta": "música/angel canales/wwd.mp3juice.blog - Angel Canales - Brujería (Audio Oficial) (320 KBps).mp3"
    }
  ],
  "changa": [
    {
      "nombre": "Changa de los 80 mezclado",
      "ruta": "música/changa/Changa de los 80 mezclado.mp3"
    },
    {
      "nombre": "Magic Mezclas I Lado B Magic Record 1985.wmv [TAN_eWYinyA]",
      "ruta": "música/changa/Magic Mezclas I Lado B Magic Record 1985.wmv [TAN_eWYinyA].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - CHANGA RETRO DE LOS 80s (320 KBps)",
      "ruta": "música/changa/wwd.mp3juice.blog - CHANGA RETRO DE LOS 80s (320 KBps).mp3"
    },
    {
      "nombre": "magic mezclas 2 [zfbJyjqeoJU]",
      "ruta": "música/changa/magic mezclas 2 [zfbJyjqeoJU].mp3"
    },
    {
      "nombre": "magic mezclas musica de los 70,80 y 90... [hfcWx0m7hHM]",
      "ruta": "música/changa/magic mezclas musica de los 70,80 y 90... [hfcWx0m7hHM].mp3"
    },
    {
      "nombre": "LOS 80  DJ MARCOS",
      "ruta": "música/changa/LOS 80  DJ MARCOS.mp3"
    }
  ],
  "chatarritas": [
    {
      "nombre": "YouTube [eu9QJ0g-r0A]",
      "ruta": "música/chatarritas/YouTube [eu9QJ0g-r0A].mp3"
    },
    {
      "nombre": "Led Zeppelin - Stairway to Heaven_Escalera al Cielo (Subtítulos en Español) [mVeG0OWjRG8]",
      "ruta": "música/chatarritas/Led Zeppelin - Stairway to Heaven_Escalera al Cielo (Subtítulos en Español) [mVeG0OWjRG8].mp3"
    },
    {
      "nombre": "BAJANDO POR EL RIO - NEIL YOUNG [rXNcBy4RvyI]",
      "ruta": "música/chatarritas/BAJANDO POR EL RIO - NEIL YOUNG [rXNcBy4RvyI].mp3"
    },
    {
      "nombre": "Eagles - Hotel California (Live 1977) (Official Video) [HD] [09839DpTctU]",
      "ruta": "música/chatarritas/Eagles - Hotel California (Live 1977) (Official Video) [HD] [09839DpTctU].mp3"
    }
  ],
  "chayanne": [
    {
      "nombre": "Chayanne - Bailando Bachata",
      "ruta": "música/chayanne/Chayanne - Bailando Bachata.mp3"
    },
    {
      "nombre": "Chayanne - Necesito Un Segundo (1)",
      "ruta": "música/chayanne/Chayanne - Necesito Un Segundo (1).mp3"
    },
    {
      "nombre": "Chayanne - La Clave",
      "ruta": "música/chayanne/Chayanne - La Clave.mp3"
    },
    {
      "nombre": "Chayanne - De Tanto",
      "ruta": "música/chayanne/Chayanne - De Tanto.mp3"
    },
    {
      "nombre": "Chayanne - Se Me Quedó",
      "ruta": "música/chayanne/Chayanne - Se Me Quedó.mp3"
    },
    {
      "nombre": "Chayanne - Vivir Bonito (ByWalterWeb)",
      "ruta": "música/chayanne/Chayanne - Vivir Bonito (ByWalterWeb).mp3"
    },
    {
      "nombre": "Chayanne - Como Tú Y Yo",
      "ruta": "música/chayanne/Chayanne - Como Tú Y Yo.mp3"
    },
    {
      "nombre": "Chayanne Full Álbum _ 15 Canciones Inolvidables para Cantar y Bailar sin Parar [GB6INnIsKOw]",
      "ruta": "música/chayanne/Chayanne Full Álbum _ 15 Canciones Inolvidables para Cantar y Bailar sin Parar [GB6INnIsKOw].mp3"
    },
    {
      "nombre": "Chayanne Exitos 2024 ~ 15 Super Éxitos de Chayanne ~ Colección Completa de Sus Mejores Canciones [rzVpUtoROgE]",
      "ruta": "música/chayanne/Chayanne Exitos 2024 ~ 15 Super Éxitos de Chayanne ~ Colección Completa de Sus Mejores Canciones [rzVpUtoROgE].mp3"
    },
    {
      "nombre": "Chayanne - Te Amo y Punto",
      "ruta": "música/chayanne/Chayanne - Te Amo y Punto.mp3"
    },
    {
      "nombre": "Chayanne - Necesito Un Segundo",
      "ruta": "música/chayanne/Chayanne - Necesito Un Segundo.mp3"
    }
  ],
  "contrapunteo venezolano": [
    {
      "nombre": "wwd.mp3juice.blog - 05 UN MALANDRO Y DOS LLANEROS (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - 05 UN MALANDRO Y DOS LLANEROS (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Alberto Castillo y Miguelito Díaz - Dos Coleadores Rivales (Vídeo Oficial) (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Alberto Castillo y Miguelito Díaz - Dos Coleadores Rivales (Vídeo Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - CONTRAPUNTEO Defendiendo nuestro llano - Reyes Domínguez y Julio Pantoja (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - CONTRAPUNTEO Defendiendo nuestro llano - Reyes Domínguez y Julio Pantoja (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Luchar por la misma causa - Reyes Dominguez Argenis salazar (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Luchar por la misma causa - Reyes Dominguez Argenis salazar (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Dos Gatos Con Cara E Tigre - Jesus Daniel Quintero y Cesar Montoya (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Dos Gatos Con Cara E Tigre - Jesus Daniel Quintero y Cesar Montoya (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Hombre no deja a mujer - Norelkys Rondon y Ulises Baptista (Contrapunteo) (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Hombre no deja a mujer - Norelkys Rondon y Ulises Baptista (Contrapunteo) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - JORGE GUERRERO Y NERYS PADRON - Contrapunteo Arrimese A Los Bordones (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - JORGE GUERRERO Y NERYS PADRON - Contrapunteo Arrimese A Los Bordones (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - LO QUE VALE Y PESA EL LLANO- WALTER SILVA Y JORGE GUERRERO (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - LO QUE VALE Y PESA EL LLANO- WALTER SILVA Y JORGE GUERRERO (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Dos paisanos de Maisanta - Jose Cheo Colmenarez y Bladimir Villanueva Silva (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Dos paisanos de Maisanta - Jose Cheo Colmenarez y Bladimir Villanueva Silva (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Cantores de un mismo llano - Gerbys Montoya y Jhony Delgado (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Cantores de un mismo llano - Gerbys Montoya y Jhony Delgado (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Llanero de Aquellos Tiempos - Teo Galindez Reyes Dominguez (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Llanero de Aquellos Tiempos - Teo Galindez Reyes Dominguez (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Miguelito Díaz ft Cholo Valderrama - Verso a Verso (Vídeo Oficial) (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Miguelito Díaz ft Cholo Valderrama - Verso a Verso (Vídeo Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - CONTRAPUNTEO Rafael Carrasco Armando Villanueva EXAMEN LLANERO (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - CONTRAPUNTEO Rafael Carrasco Armando Villanueva EXAMEN LLANERO (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Un coplero en el oriente - Freddy Arevalo vs Jose Zamora El pollo de Sacuima (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Un coplero en el oriente - Freddy Arevalo vs Jose Zamora El pollo de Sacuima (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - CONTRAPUNTEO (JORGE GUERRERO y CARLOS MELENDEZ) Musica Llanera Venezolana (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - CONTRAPUNTEO (JORGE GUERRERO y CARLOS MELENDEZ) Musica Llanera Venezolana (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Me encontre con Cheo Hernandez - Miguel Suarez y Cheo Hernandez Prisco (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - Me encontre con Cheo Hernandez - Miguel Suarez y Cheo Hernandez Prisco (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - el mejor contrapunteo llanero, José Medina vs Orlando Medina parte 1 (buena calidad) (320 KBps)",
      "ruta": "música/contrapunteo venezolano/wwd.mp3juice.blog - el mejor contrapunteo llanero, José Medina vs Orlando Medina parte 1 (buena calidad) (320 KBps).mp3"
    }
  ],
  "el gran combo de puerto rico": [
    {
      "nombre": "EL GRAN COMBO DE PUERTO RICO",
      "ruta": "música/el gran combo de puerto rico/EL GRAN COMBO DE PUERTO RICO.mp3"
    },
    {
      "nombre": "mix el gran combo",
      "ruta": "música/el gran combo de puerto rico/mix el gran combo.mp3"
    }
  ],
  "fruko": [
    {
      "nombre": "wwd.mp3juice.blog - Fruko Y Sus Tesos -- Grandes Exitos (320 KBps)",
      "ruta": "música/fruko/wwd.mp3juice.blog - Fruko Y Sus Tesos -- Grandes Exitos (320 KBps).mp3"
    }
  ],
  "Gilberto santa rosa": [
    {
      "nombre": "Gilberto Santa Rosa - Almas Gemelas",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Almas Gemelas.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Amandote",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Amandote.mp3"
    },
    {
      "nombre": "Franco de Vita - Te Veo Venir Soledad (Live Video (Short Version)) ft. Gilberto Santa Rosa [LYVipCVCdLg]",
      "ruta": "música/Gilberto santa rosa/Franco de Vita - Te Veo Venir Soledad (Live Video (Short Version)) ft. Gilberto Santa Rosa [LYVipCVCdLg].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Apaga la Luz (En Vivo) [KXl_EHr2P4k]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Apaga la Luz (En Vivo) [KXl_EHr2P4k].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Cartas Sobre La Mesa (Lyric Video) [uKFXoNzMNKo]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Cartas Sobre La Mesa (Lyric Video) [uKFXoNzMNKo].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Conciencia",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Conciencia.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Conteo Regresivo",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Conteo Regresivo.mp3"
    },
    {
      "nombre": "Ednita Nazario - Ser Tu Amigo (Audio) ft. Gilberto Santa Rosa [sK5DtDBdp8M]",
      "ruta": "música/Gilberto santa rosa/Ednita Nazario - Ser Tu Amigo (Audio) ft. Gilberto Santa Rosa [sK5DtDBdp8M].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - La Sigo Amando Tanto (Cover Audio) [MG_lI-zH1ok]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - La Sigo Amando Tanto (Cover Audio) [MG_lI-zH1ok].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - La Agarro Bajando",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - La Agarro Bajando.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Me Cambiaron Las Preguntas (feat. Rubén Blades) (Album Version)",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Me Cambiaron Las Preguntas (feat. Rubén Blades) (Album Version).mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Mal Herido (Album Version)",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Mal Herido (Album Version).mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Dolia Menos",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Dolia Menos.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Me Volvieron A Hablar De Ella",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Me Volvieron A Hablar De Ella.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Enseñame A Vivir Sin Ti (Video Version) [J-fOlGCesNw]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Enseñame A Vivir Sin Ti (Video Version) [J-fOlGCesNw].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Ni Bien Ni Mal (En Vivo) [K9n3_m_TjRs]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Ni Bien Ni Mal (En Vivo) [K9n3_m_TjRs].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - No Estoy Para Tí (Salsa Version (Cover Audio)) [NmKTmlpGX30]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - No Estoy Para Tí (Salsa Version (Cover Audio)) [NmKTmlpGX30].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - No Olvides Recordarme (En Vivo) [Y3lPwa3ROzE]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - No Olvides Recordarme (En Vivo) [Y3lPwa3ROzE].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - No Pensé Enamorarme Otra Vez (Bolero (Cover Audio)) [inVFIG4E2Zw]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - No Pensé Enamorarme Otra Vez (Bolero (Cover Audio)) [inVFIG4E2Zw].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Para Decir Te Amo",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Para Decir Te Amo.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Perdóname",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Perdóname.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - No Te Vayas",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - No Te Vayas.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Pueden Decir (Video Version) [_ZZabmuL8rk]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Pueden Decir (Video Version) [_ZZabmuL8rk].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Por Mas Que Intento (Video Version) [Wlyaug3o8wI]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Por Mas Que Intento (Video Version) [Wlyaug3o8wI].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Se Supone",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Se Supone.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Qué Manera De Quererte",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Qué Manera De Quererte.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Nunca Te He Dicho (Cover Audio) [uiwSz1eyrOA]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Nunca Te He Dicho (Cover Audio) [uiwSz1eyrOA].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Sin Voluntad",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Sin Voluntad.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Sombra Loca",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Sombra Loca.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Te Propongo",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Te Propongo.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Vivir Sin Ella",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Vivir Sin Ella.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Viceversa",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Viceversa.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Un Montón de Estrellas",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Un Montón de Estrellas.mp3"
    },
    {
      "nombre": "Me Equivoque - A.B, Quintanilla Feat Giberto Santa Rosa [woPo3BOrw04]",
      "ruta": "música/Gilberto santa rosa/Me Equivoque - A.B, Quintanilla Feat Giberto Santa Rosa [woPo3BOrw04].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Dejame Sentirte",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Dejame Sentirte.mp3"
    },
    {
      "nombre": "Vico C & Gilberto Santa rosa - Lo Grande que es Perdonar (con letra) [_S-VzLLdkv4]",
      "ruta": "música/Gilberto santa rosa/Vico C & Gilberto Santa rosa - Lo Grande que es Perdonar (con letra) [_S-VzLLdkv4].mp3"
    },
    {
      "nombre": "No Hay Nada Mas Importante [S4dV4O6_eq8]",
      "ruta": "música/Gilberto santa rosa/No Hay Nada Mas Importante [S4dV4O6_eq8].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Yo No Te Pido",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Yo No Te Pido.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Que Alguien Me Diga",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Que Alguien Me Diga.mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Si No Lo Digo Ahora (Cover Audio) [RtkEeT6D_70]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Si No Lo Digo Ahora (Cover Audio) [RtkEeT6D_70].mp3"
    },
    {
      "nombre": "Gilberto Santa Rosa - Sin Voluntad (Official Video) [VelD64XLvjI]",
      "ruta": "música/Gilberto santa rosa/Gilberto Santa Rosa - Sin Voluntad (Official Video) [VelD64XLvjI].mp3"
    }
  ],
  "grupo abba": [
    {
      "nombre": "Grandes éxitos de ABBA - Colección de canciones de ABBA [WJl5Vj4MkI0]",
      "ruta": "música/grupo abba/Grandes éxitos de ABBA - Colección de canciones de ABBA [WJl5Vj4MkI0].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - ABBA - Chiquitita (320 KBps)",
      "ruta": "música/grupo abba/wwd.mp3juice.blog - ABBA - Chiquitita (320 KBps).mp3"
    }
  ],
  "grupo bota": [
    {
      "nombre": "wwd.mp3juice.blog - Frank Quintero¤°.¸¸.• Amantes de luna llena (320 KBps)",
      "ruta": "música/grupo bota/wwd.mp3juice.blog - Frank Quintero¤°.¸¸.• Amantes de luna llena (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - GRUPO BOTA - Yo No He Dicho (320 KBps)",
      "ruta": "música/grupo bota/wwd.mp3juice.blog - GRUPO BOTA - Yo No He Dicho (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Solitario Grupo Bota (320 KBps)",
      "ruta": "música/grupo bota/wwd.mp3juice.blog - Solitario Grupo Bota (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - GRUPO BOTA-1974-75 -76 -77 -78 .............(((ECOS DE JUVENTUD))) (320 KBps)",
      "ruta": "música/grupo bota/wwd.mp3juice.blog - GRUPO BOTA-1974-75 -76 -77 -78 .............(((ECOS DE JUVENTUD))) (320 KBps).mp3"
    }
  ],
  "grupo niche": [
    {
      "nombre": "wwd.mp3juice.blog - Éxitos Del Grupo Niche - Salsa Power (320 KBps)",
      "ruta": "música/grupo niche/wwd.mp3juice.blog - Éxitos Del Grupo Niche - Salsa Power (320 KBps).mp3"
    }
  ],
  "juan gabriel": [
    {
      "nombre": "wwd.mp3juice.blog - Ana Gabriel - Simplemente Amigos (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Ana Gabriel - Simplemente Amigos (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Abrázame Muy Fuerte (En Vivo Desde Bellas Artes, México 2013) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Abrázame Muy Fuerte (En Vivo Desde Bellas Artes, México 2013) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Amor Eterno (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Amor Eterno (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Insensible (En Vivo Desde Bellas Artes, México 2013) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Insensible (En Vivo Desde Bellas Artes, México 2013) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Hasta Que Te Conocí (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Hasta Que Te Conocí (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Por Qué Me Haces Llorar (En Vivo Desde Bellas Artes, México 2013) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Por Qué Me Haces Llorar (En Vivo Desde Bellas Artes, México 2013) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Se Me Olvidó Otra Vez (Letra Lyrics) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Se Me Olvidó Otra Vez (Letra Lyrics) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - ha llegado un angel JUAN GABRIEL.mpg (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - ha llegado un angel JUAN GABRIEL.mpg (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Así Fue (En Vivo Desde Bellas Artes, México 2013) ft. Isabel Pantoja (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Así Fue (En Vivo Desde Bellas Artes, México 2013) ft. Isabel Pantoja (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Caray Esta Noche Voy A Verla Juntos Me Gustas Mucho(En Vivo Desde Bellas Artes, México 2013 Medley) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Caray Esta Noche Voy A Verla Juntos Me Gustas Mucho(En Vivo Desde Bellas Artes, México 2013 Medley) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Te Sigo Amando (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Te Sigo Amando (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Ya Lo Sé Que Tú Te Vas (Letra Lyrics) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Ya Lo Sé Que Tú Te Vas (Letra Lyrics) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Querida (En Vivo Desde Bellas Artes, México 2013) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Querida (En Vivo Desde Bellas Artes, México 2013) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Si Quieres (Cover Audio) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Si Quieres (Cover Audio) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Inocente Pobre Amigo (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Inocente Pobre Amigo (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Yo Te Recuerdo ft. Marc Anthony (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Yo Te Recuerdo ft. Marc Anthony (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel - Hasta Que Te Conocí (Letra Lyrics) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel - Hasta Que Te Conocí (Letra Lyrics) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Juan Gabriel y Rocio Durcal El Destino en el Festival Acapulco 97 (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Juan Gabriel y Rocio Durcal El Destino en el Festival Acapulco 97 (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Leo Dan - Tú Llegaste Cuando Menos Te Esperaba (En Vivo) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Leo Dan - Tú Llegaste Cuando Menos Te Esperaba (En Vivo) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Te Lo Pido por Favor (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps)",
      "ruta": "música/juan gabriel/wwd.mp3juice.blog - Te Lo Pido por Favor (En Vivo Desde el Instituto Nacional de Bellas Artes ) (320 KBps).mp3"
    }
  ],
  "julio iglesias": [
    {
      "nombre": "Julio Iglesias Grandes Exitos, Sus Mejores Canciones - Las Mejores Canciones De Julio Iglesias #a21 [U155XDQdtX0]",
      "ruta": "música/julio iglesias/Julio Iglesias Grandes Exitos, Sus Mejores Canciones - Las Mejores Canciones De Julio Iglesias #a21 [U155XDQdtX0].mp3"
    },
    {
      "nombre": "JULIO IGLESIAS TODOS SUS 30 GRANDES EXITOS INMORTALES - LAS MEJORES CANCIONES DE JULIO IGLESIAS [Ub1qVcG57rw]",
      "ruta": "música/julio iglesias/JULIO IGLESIAS TODOS SUS 30 GRANDES EXITOS INMORTALES - LAS MEJORES CANCIONES DE JULIO IGLESIAS [Ub1qVcG57rw].mp3"
    }
  ],
  "llaneras": [
    {
      "nombre": "🇻🇪🎧Luis Silva Éxitos Mix Latín Pawer Dj Albert fl DJ Moises figuera🎧🇻🇪 [DW9EehSkZ_c]",
      "ruta": "música/llaneras/🇻🇪🎧Luis Silva Éxitos Mix Latín Pawer Dj Albert fl DJ Moises figuera🎧🇻🇪 [DW9EehSkZ_c].mp3"
    },
    {
      "nombre": "José Luis Perales Sus Mejores Éxitos - Recopilación 30 Canciones De José Luis Perales #t74 [-M8CvAZurRk]",
      "ruta": "música/llaneras/José Luis Perales Sus Mejores Éxitos - Recopilación 30 Canciones De José Luis Perales #t74 [-M8CvAZurRk].mp3"
    },
    {
      "nombre": "Reynaldo Armas - 15 Grandes Exitos _ The Best (Recopilación) [25eAP1fPvgY]",
      "ruta": "música/llaneras/Reynaldo Armas - 15 Grandes Exitos _ The Best (Recopilación) [25eAP1fPvgY].mp3"
    },
    {
      "nombre": "Luis Silva - Romance Quinceañero (Audio Oficial) [usr05xrJS24]",
      "ruta": "música/llaneras/Luis Silva - Romance Quinceañero (Audio Oficial) [usr05xrJS24].mp3"
    },
    {
      "nombre": "SUPER LLANERAS MIX ★ 60 EXITOS ★ LA MEJOR MUSICA LLANERA @ELAPODERADO ✔ [M3QAQr9fcTo]",
      "ruta": "música/llaneras/SUPER LLANERAS MIX ★ 60 EXITOS ★ LA MEJOR MUSICA LLANERA @ELAPODERADO ✔ [M3QAQr9fcTo].mp3"
    }
  ],
  "los angeles negros": [
    {
      "nombre": "wwd.mp3juice.blog - Los Angeles Negros - 30 Exitos Inmortales (Disco Completo) (320 KBps)",
      "ruta": "música/los angeles negros/wwd.mp3juice.blog - Los Angeles Negros - 30 Exitos Inmortales (Disco Completo) (320 KBps).mp3"
    }
  ],
  "los blancos de maracaibo": [
    {
      "nombre": "Cuando florezcan las amapolas [qIOdN7Vjfns]",
      "ruta": "música/los blancos de maracaibo/Cuando florezcan las amapolas [qIOdN7Vjfns].mp3"
    },
    {
      "nombre": "La Pollera Colorá Los Blanco [lMTfej9zQxU]",
      "ruta": "música/los blancos de maracaibo/La Pollera Colorá Los Blanco [lMTfej9zQxU].mp3"
    },
    {
      "nombre": "La Mecedora Los Blanco [9IUAP9dvFwE]",
      "ruta": "música/los blancos de maracaibo/La Mecedora Los Blanco [9IUAP9dvFwE].mp3"
    },
    {
      "nombre": "Cuando florezcan las amapolas [qIOdN7Vjfns] (1)",
      "ruta": "música/los blancos de maracaibo/Cuando florezcan las amapolas [qIOdN7Vjfns] (1).mp3"
    },
    {
      "nombre": "Te Quiero - Los Blanco de Maracaibo [pPBC2hBnVPs]",
      "ruta": "música/los blancos de maracaibo/Te Quiero - Los Blanco de Maracaibo [pPBC2hBnVPs].mp3"
    },
    {
      "nombre": "Joe Arroyo y La Verdad - En Barranquilla me Quedo (Video Oficial) _ Discos Fuentes [ZGjt_dXh1Lo]",
      "ruta": "música/los blancos de maracaibo/Joe Arroyo y La Verdad - En Barranquilla me Quedo (Video Oficial) _ Discos Fuentes [ZGjt_dXh1Lo].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - La Burrita - Los Corraleros de Majagual Discos Fuentes (320 KBps)",
      "ruta": "música/los blancos de maracaibo/wwd.mp3juice.blog - La Burrita - Los Corraleros de Majagual Discos Fuentes (320 KBps).mp3"
    },
    {
      "nombre": "Los Blanco La Verdugo 2016 [zlpaMkYY8EU]",
      "ruta": "música/los blancos de maracaibo/Los Blanco La Verdugo 2016 [zlpaMkYY8EU].mp3"
    },
    {
      "nombre": "La Cañá...Los Blanco [hEngOXz8YBw]",
      "ruta": "música/los blancos de maracaibo/La Cañá...Los Blanco [hEngOXz8YBw].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - El NEGRITO DE LA SALSA (320 KBps)",
      "ruta": "música/los blancos de maracaibo/wwd.mp3juice.blog - El NEGRITO DE LA SALSA (320 KBps).mp3"
    },
    {
      "nombre": "Que Muchacho Los Blanco [eMo6KZOZpDA]",
      "ruta": "música/los blancos de maracaibo/Que Muchacho Los Blanco [eMo6KZOZpDA].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Loquito Por Ti - Armando Hernandez con El Combo Caribe (Video Oficial) Discos Fuentes (320 KBps)",
      "ruta": "música/los blancos de maracaibo/wwd.mp3juice.blog - Loquito Por Ti - Armando Hernandez con El Combo Caribe (Video Oficial) Discos Fuentes (320 KBps).mp3"
    },
    {
      "nombre": "lOS BLANCO APRETAITO EN VIVO [G3ZeDOYEax8]",
      "ruta": "música/los blancos de maracaibo/lOS BLANCO APRETAITO EN VIVO [G3ZeDOYEax8].mp3"
    }
  ],
  "los corraleros de majagual": [
    {
      "nombre": "CABALLO VIEJO (CORRALEROS DE MAJAGUAL).wmv [b1byBaf1M44]",
      "ruta": "música/los corraleros de majagual/CABALLO VIEJO (CORRALEROS DE MAJAGUAL).wmv [b1byBaf1M44].mp3"
    },
    {
      "nombre": "POR ESTAS CALLES - YORDANO [5WDXjSv68Xc]",
      "ruta": "música/los corraleros de majagual/POR ESTAS CALLES - YORDANO [5WDXjSv68Xc].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - EL BAILADOR - Los Corraleros de Majagual feat. Julio Erazo (Video Letra) (320 KBps)",
      "ruta": "música/los corraleros de majagual/wwd.mp3juice.blog - EL BAILADOR - Los Corraleros de Majagual feat. Julio Erazo (Video Letra) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - El Parrandón, Rafael Orozco Con El Binomio De Oro - Video Oficial (320 KBps)",
      "ruta": "música/los corraleros de majagual/wwd.mp3juice.blog - El Parrandón, Rafael Orozco Con El Binomio De Oro - Video Oficial (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - LOS SABANALES - LOS CORRALEROS DE MAJAGUAL (320 KBps)",
      "ruta": "música/los corraleros de majagual/wwd.mp3juice.blog - LOS SABANALES - LOS CORRALEROS DE MAJAGUAL (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - La Bonga - Los corraleros de Majagual Discos Fuentes (320 KBps)",
      "ruta": "música/los corraleros de majagual/wwd.mp3juice.blog - La Bonga - Los corraleros de Majagual Discos Fuentes (320 KBps).mp3"
    },
    {
      "nombre": "LA BURRITA los corraleros de majagual HD audio HQ [rSPvF4tLKms]",
      "ruta": "música/los corraleros de majagual/LA BURRITA los corraleros de majagual HD audio HQ [rSPvF4tLKms].mp3"
    }
  ],
  "los hermanos lebron": [
    {
      "nombre": "Diez Lagrimas - Los Hermanos Lebron [NIPS8Tvd3SY]",
      "ruta": "música/los hermanos lebron/Diez Lagrimas - Los Hermanos Lebron [NIPS8Tvd3SY].mp3"
    },
    {
      "nombre": "Hermanos Lebron (Lebron Brother's) - Mi Fracaso (HQ Audio) [GaiW5rkzokY]",
      "ruta": "música/los hermanos lebron/Hermanos Lebron (Lebron Brother's) - Mi Fracaso (HQ Audio) [GaiW5rkzokY].mp3"
    },
    {
      "nombre": "Hermanos Lebron - Temperatura(Video Oficial)HD - HQ remasterizado (la temperatura - lebron brothers) [VCEYsBBNzJ4]",
      "ruta": "música/los hermanos lebron/Hermanos Lebron - Temperatura(Video Oficial)HD - HQ remasterizado (la temperatura - lebron brothers) [VCEYsBBNzJ4].mp3"
    },
    {
      "nombre": "HERMANOS LEBRON 3 HORAS DJ NEGRO ANDRES [Dzzc6u3IFiE]",
      "ruta": "música/los hermanos lebron/HERMANOS LEBRON 3 HORAS DJ NEGRO ANDRES [Dzzc6u3IFiE].mp3"
    },
    {
      "nombre": "Lebrón Brothers - Tu Llegaste a Mi Vida (Audio Oficial) [zCFaWsO3wqQ]",
      "ruta": "música/los hermanos lebron/Lebrón Brothers - Tu Llegaste a Mi Vida (Audio Oficial) [zCFaWsO3wqQ].mp3"
    },
    {
      "nombre": "La Ley [yv7e6kMcuNo]",
      "ruta": "música/los hermanos lebron/La Ley [yv7e6kMcuNo].mp3"
    },
    {
      "nombre": "Dulzura - Los Hermanos Lebron _ Letra [QBPJ6OJiatM]",
      "ruta": "música/los hermanos lebron/Dulzura - Los Hermanos Lebron _ Letra [QBPJ6OJiatM].mp3"
    },
    {
      "nombre": "Hermanos Lebrón - Qué Pena _ Salsa & Letra [VzY4ZdxZwys] (1)",
      "ruta": "música/los hermanos lebron/Hermanos Lebrón - Qué Pena _ Salsa & Letra [VzY4ZdxZwys] (1).mp3"
    },
    {
      "nombre": "m1",
      "ruta": "música/los hermanos lebron/m1.mp3"
    },
    {
      "nombre": "Regresa a mi - Los Hermanos Lebrón [nG9PIHCle6I]",
      "ruta": "música/los hermanos lebron/Regresa a mi - Los Hermanos Lebrón [nG9PIHCle6I].mp3"
    },
    {
      "nombre": "QUE HACES AQUÍ - The LeBron Brothers (Video Oficial) - Los Hermanos LeBron [DXWnZFS_nnI]",
      "ruta": "música/los hermanos lebron/QUE HACES AQUÍ - The LeBron Brothers (Video Oficial) - Los Hermanos LeBron [DXWnZFS_nnI].mp3"
    },
    {
      "nombre": "Lebrón Brothers - Salsa y Control (Audio Oficial) [UynbPaAT7wQ]",
      "ruta": "música/los hermanos lebron/Lebrón Brothers - Salsa y Control (Audio Oficial) [UynbPaAT7wQ].mp3"
    },
    {
      "nombre": "Diez Lagrimas - Los Hermanos Lebron [NIPS8Tvd3SY] (1)",
      "ruta": "música/los hermanos lebron/Diez Lagrimas - Los Hermanos Lebron [NIPS8Tvd3SY] (1).mp3"
    },
    {
      "nombre": "Son Sabrosón [UWjgtY1Zm5c]",
      "ruta": "música/los hermanos lebron/Son Sabrosón [UWjgtY1Zm5c].mp3"
    },
    {
      "nombre": "Llegamos - Hermanos Lebrón (Vídeo Oficial HD-HQ) [8PO-DbbQLWU]",
      "ruta": "música/los hermanos lebron/Llegamos - Hermanos Lebrón (Vídeo Oficial HD-HQ) [8PO-DbbQLWU].mp3"
    },
    {
      "nombre": "Sin Negro No Hay Guaguancó [Pw8gxhMaKnw]",
      "ruta": "música/los hermanos lebron/Sin Negro No Hay Guaguancó [Pw8gxhMaKnw].mp3"
    },
    {
      "nombre": "Salsa Clásica_ Mix de Hermanos Lebrón [o5cr2wqT-r8]",
      "ruta": "música/los hermanos lebron/Salsa Clásica_ Mix de Hermanos Lebrón [o5cr2wqT-r8].mp3"
    },
    {
      "nombre": "TE ENCONTRE - LOS HERMANOS LEBRON [UbBMDB_vjck]",
      "ruta": "música/los hermanos lebron/TE ENCONTRE - LOS HERMANOS LEBRON [UbBMDB_vjck].mp3"
    },
    {
      "nombre": "Hermanos Lebrón - Qué Pena _ Salsa & Letra [VzY4ZdxZwys]",
      "ruta": "música/los hermanos lebron/Hermanos Lebrón - Qué Pena _ Salsa & Letra [VzY4ZdxZwys].mp3"
    },
    {
      "nombre": "The Lebron Brothers - Solita [DOm2axSvgak]",
      "ruta": "música/los hermanos lebron/The Lebron Brothers - Solita [DOm2axSvgak].mp3"
    },
    {
      "nombre": "Con Una Mentira Se Tapa Otra Mentira",
      "ruta": "música/los hermanos lebron/Con Una Mentira Se Tapa Otra Mentira.mp3"
    },
    {
      "nombre": "m2",
      "ruta": "música/los hermanos lebron/m2.mp3"
    },
    {
      "nombre": "Lo Tuyo Llegará - Los Hermanos L-Brón [jlFEKhrFJHo]",
      "ruta": "música/los hermanos lebron/Lo Tuyo Llegará - Los Hermanos L-Brón [jlFEKhrFJHo].mp3"
    }
  ],
  "los melodicos": [
    {
      "nombre": "wwd.mp3juice.blog - Los Melódicos - Mi Corazón (320 KBps)",
      "ruta": "música/los melodicos/wwd.mp3juice.blog - Los Melódicos - Mi Corazón (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Los Melódicos El Sonido que Conquistó Corazones (320 KBps)",
      "ruta": "música/los melodicos/wwd.mp3juice.blog - Los Melódicos El Sonido que Conquistó Corazones (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - LOS MELÓDICOS - 40 AÑOS DE ÉXITOS - (CD 1).- (320 KBps)",
      "ruta": "música/los melodicos/wwd.mp3juice.blog - LOS MELÓDICOS - 40 AÑOS DE ÉXITOS - (CD 1).- (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - 1995 - COLECCIÓN DE ÉXITOS DE LOS MELÓDICOS - 17 TEMAS.- (320 KBps)",
      "ruta": "música/los melodicos/wwd.mp3juice.blog - 1995 - COLECCIÓN DE ÉXITOS DE LOS MELÓDICOS - 17 TEMAS.- (320 KBps).mp3"
    }
  ],
  "los pasteles verdes": [
    {
      "nombre": "wwd.mp3juice.blog - Los Pasteles Verdes Exitos Mix - 20 Grandes Éxitos (320 KBps)",
      "ruta": "música/los pasteles verdes/wwd.mp3juice.blog - Los Pasteles Verdes Exitos Mix - 20 Grandes Éxitos (320 KBps).mp3"
    }
  ],
  "Maelo Ruiz": [
    {
      "nombre": "Así Eres Tú, 30 Mejores, Maelo Ruiz - Audio [eh17jn_F8tM]",
      "ruta": "música/Maelo Ruiz/Así Eres Tú, 30 Mejores, Maelo Ruiz - Audio [eh17jn_F8tM].mp3"
    },
    {
      "nombre": "Así No Se Da El Amor, 30 Mejores, Maelo Ruiz - Audio [SHRYGim7ga8]",
      "ruta": "música/Maelo Ruiz/Así No Se Da El Amor, 30 Mejores, Maelo Ruiz - Audio [SHRYGim7ga8].mp3"
    },
    {
      "nombre": "Amor No Me Ignores, 30 Mejores, Maelo Ruiz - Audio [nQ12RWfnCqw]",
      "ruta": "música/Maelo Ruiz/Amor No Me Ignores, 30 Mejores, Maelo Ruiz - Audio [nQ12RWfnCqw].mp3"
    },
    {
      "nombre": "Aroma De Mujer, 30 Mejores, Maelo Ruiz - Audio [BiIlB8Mt1yE]",
      "ruta": "música/Maelo Ruiz/Aroma De Mujer, 30 Mejores, Maelo Ruiz - Audio [BiIlB8Mt1yE].mp3"
    },
    {
      "nombre": "Amiga, 30 Mejores, Maelo Ruiz - Audio [TV8IEgi28I0]",
      "ruta": "música/Maelo Ruiz/Amiga, 30 Mejores, Maelo Ruiz - Audio [TV8IEgi28I0].mp3"
    },
    {
      "nombre": "Culpable O No, 30 Mejores, Maelo Ruiz - Audio [tw2uoJUZHg8]",
      "ruta": "música/Maelo Ruiz/Culpable O No, 30 Mejores, Maelo Ruiz - Audio [tw2uoJUZHg8].mp3"
    },
    {
      "nombre": "Cuando La Olvide Qué, 30 Mejores, Maelo Ruiz - Audio [eE9ly4qPX6k]",
      "ruta": "música/Maelo Ruiz/Cuando La Olvide Qué, 30 Mejores, Maelo Ruiz - Audio [eE9ly4qPX6k].mp3"
    },
    {
      "nombre": "Deseo, 30 Mejores, Maelo Ruiz - Audio [cCTokkrjYD0]",
      "ruta": "música/Maelo Ruiz/Deseo, 30 Mejores, Maelo Ruiz - Audio [cCTokkrjYD0].mp3"
    },
    {
      "nombre": "Esperando Un Nuevo Amor, 30 Mejores, Maelo Ruiz - Audio [hd-tgeJHyrY]",
      "ruta": "música/Maelo Ruiz/Esperando Un Nuevo Amor, 30 Mejores, Maelo Ruiz - Audio [hd-tgeJHyrY].mp3"
    },
    {
      "nombre": "Dile A Tu Dueño, 30 Mejores, Maelo Ruiz - Audio [4RruQqFViRc]",
      "ruta": "música/Maelo Ruiz/Dile A Tu Dueño, 30 Mejores, Maelo Ruiz - Audio [4RruQqFViRc].mp3"
    },
    {
      "nombre": "Bésame Así, 30 Mejores, Maelo Ruiz - Audio [0W_pZKbjTaw]",
      "ruta": "música/Maelo Ruiz/Bésame Así, 30 Mejores, Maelo Ruiz - Audio [0W_pZKbjTaw].mp3"
    },
    {
      "nombre": "He Vuelto Por Ti, 30 Mejores, Maelo Ruiz - Audio [6Jt6jXho8A0](1)",
      "ruta": "música/Maelo Ruiz/He Vuelto Por Ti, 30 Mejores, Maelo Ruiz - Audio [6Jt6jXho8A0](1).mp3"
    },
    {
      "nombre": "Entrégate, 30 Mejores, Maelo Ruiz - Audio [Y0h3LBSvCxI]",
      "ruta": "música/Maelo Ruiz/Entrégate, 30 Mejores, Maelo Ruiz - Audio [Y0h3LBSvCxI].mp3"
    },
    {
      "nombre": "Juégate A La Suerte, 30 Mejores, Maelo Ruiz - Audio [e-UQuNcqAD8]",
      "ruta": "música/Maelo Ruiz/Juégate A La Suerte, 30 Mejores, Maelo Ruiz - Audio [e-UQuNcqAD8].mp3"
    },
    {
      "nombre": "Me Lo Estás Poniendo Difícil, 30 Mejores, Maelo Ruiz - Audio [lglWPvZIgbM]",
      "ruta": "música/Maelo Ruiz/Me Lo Estás Poniendo Difícil, 30 Mejores, Maelo Ruiz - Audio [lglWPvZIgbM].mp3"
    },
    {
      "nombre": "Amor De Cristal, 30 Mejores, Maelo Ruiz - Audio [N-2O8OBkkxw]",
      "ruta": "música/Maelo Ruiz/Amor De Cristal, 30 Mejores, Maelo Ruiz - Audio [N-2O8OBkkxw].mp3"
    },
    {
      "nombre": "Mentiras Que Matan, 30 Mejores, Maelo Ruiz - Audio [oW1R282Jib0]",
      "ruta": "música/Maelo Ruiz/Mentiras Que Matan, 30 Mejores, Maelo Ruiz - Audio [oW1R282Jib0].mp3"
    },
    {
      "nombre": "Muero De Amor, 30 Mejores, Maelo Ruiz - Audio [nDccuJuboec]",
      "ruta": "música/Maelo Ruiz/Muero De Amor, 30 Mejores, Maelo Ruiz - Audio [nDccuJuboec].mp3"
    },
    {
      "nombre": "Me Niegas Tanto Amor, 30 Mejores, Maelo Ruiz - Audio [fMORgllSQ3o]",
      "ruta": "música/Maelo Ruiz/Me Niegas Tanto Amor, 30 Mejores, Maelo Ruiz - Audio [fMORgllSQ3o].mp3"
    },
    {
      "nombre": "Nadie Igual Que Tú, 30 Mejores, Maelo Ruiz - Audio [yfE3pCMuWuk]",
      "ruta": "música/Maelo Ruiz/Nadie Igual Que Tú, 30 Mejores, Maelo Ruiz - Audio [yfE3pCMuWuk].mp3"
    },
    {
      "nombre": "No Más Mentiras, 30 Mejores, Maelo Ruiz - Audio [m3o82C-QQeA]",
      "ruta": "música/Maelo Ruiz/No Más Mentiras, 30 Mejores, Maelo Ruiz - Audio [m3o82C-QQeA].mp3"
    },
    {
      "nombre": "Medley, 30 Mejores, Maelo Ruiz - Audio [TEeREI9rD34]",
      "ruta": "música/Maelo Ruiz/Medley, 30 Mejores, Maelo Ruiz - Audio [TEeREI9rD34].mp3"
    },
    {
      "nombre": "Por Favor Señora, 30 Mejores, Maelo Ruiz - Audio [qNMko1sT9Lk]",
      "ruta": "música/Maelo Ruiz/Por Favor Señora, 30 Mejores, Maelo Ruiz - Audio [qNMko1sT9Lk].mp3"
    },
    {
      "nombre": "Regálame Una Noche, 30 Mejores, Maelo Ruiz - Audio [Vw6gDcIIq5w]",
      "ruta": "música/Maelo Ruiz/Regálame Una Noche, 30 Mejores, Maelo Ruiz - Audio [Vw6gDcIIq5w].mp3"
    },
    {
      "nombre": "Será Que Si, 30 Mejores, Maelo Ruiz - Audio [umpClnP7caM]",
      "ruta": "música/Maelo Ruiz/Será Que Si, 30 Mejores, Maelo Ruiz - Audio [umpClnP7caM].mp3"
    },
    {
      "nombre": "Te Va A Doler, 30 Mejores, Maelo Ruiz - Audio [xl_zM58bEt0]",
      "ruta": "música/Maelo Ruiz/Te Va A Doler, 30 Mejores, Maelo Ruiz - Audio [xl_zM58bEt0].mp3"
    },
    {
      "nombre": "Si Volvieras A Mí, 30 Mejores Maelo Ruiz - Audio [ydZFhARESqQ]",
      "ruta": "música/Maelo Ruiz/Si Volvieras A Mí, 30 Mejores Maelo Ruiz - Audio [ydZFhARESqQ].mp3"
    },
    {
      "nombre": "Tu Forma De Amar, 30 Mejores, Maelo Ruiz - Audio [BCezYp3Y66M]",
      "ruta": "música/Maelo Ruiz/Tu Forma De Amar, 30 Mejores, Maelo Ruiz - Audio [BCezYp3Y66M].mp3"
    },
    {
      "nombre": "Mi Mundo Es Ella, 30 Mejores, Maelo Ruiz - Audio [S--QIoLPJrw]",
      "ruta": "música/Maelo Ruiz/Mi Mundo Es Ella, 30 Mejores, Maelo Ruiz - Audio [S--QIoLPJrw].mp3"
    },
    {
      "nombre": "No Te Vayas, 30 Mejores, Maelo Ruiz - Audio [XPd3O16OasE]",
      "ruta": "música/Maelo Ruiz/No Te Vayas, 30 Mejores, Maelo Ruiz - Audio [XPd3O16OasE].mp3"
    }
  ],
  "micaela": [
    {
      "nombre": "Sonora Carruseles - Micaela (Audio) [5tKzKJob0yA]",
      "ruta": "música/micaela/Sonora Carruseles - Micaela (Audio) [5tKzKJob0yA].mp3"
    }
  ],
  "michael jackson": [
    {
      "nombre": "wwd.mp3juice.blog - Greatest Of Michael Jackson (320 KBps)",
      "ruta": "música/michael jackson/wwd.mp3juice.blog - Greatest Of Michael Jackson (320 KBps).mp3"
    }
  ],
  "Nueva carpeta": [
    {
      "nombre": "Las Cuatro Monedas - Los Grandes Éxitos (1992) __ Full Album __ [d_2vs1TgkjA]",
      "ruta": "música/Nueva carpeta/Las Cuatro Monedas - Los Grandes Éxitos (1992) __ Full Album __ [d_2vs1TgkjA].mp3"
    },
    {
      "nombre": "DAIQUIRI - GRANDES EXITOS [UQniRyJiPwQ]",
      "ruta": "música/Nueva carpeta/DAIQUIRI - GRANDES EXITOS [UQniRyJiPwQ].mp3"
    }
  ],
  "oscar de leon dimension latina": [
    {
      "nombre": "wwd.mp3juice.blog - OSCAR DE LEON DIMENSIÓN LATINA RETRO MIX LO MAS SONADO DE LA DIMENSIÓN LATINA (320 KBps)",
      "ruta": "música/oscar de leon dimension latina/wwd.mp3juice.blog - OSCAR DE LEON DIMENSIÓN LATINA RETRO MIX LO MAS SONADO DE LA DIMENSIÓN LATINA (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - exitos de OSCAR DE LEON con la dimension latina (by DJ COCHOLO) RD 2022 (320 KBps)",
      "ruta": "música/oscar de leon dimension latina/wwd.mp3juice.blog - exitos de OSCAR DE LEON con la dimension latina (by DJ COCHOLO) RD 2022 (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - RETRO - OSCAR D LEON (DIMENSION LATINA) - AÑOS 70 (320 KBps)",
      "ruta": "música/oscar de leon dimension latina/wwd.mp3juice.blog - RETRO - OSCAR D LEON (DIMENSION LATINA) - AÑOS 70 (320 KBps).mp3"
    }
  ],
  "Oscar Santana": [
    {
      "nombre": "Maria Soledad [NzBpg5xXecQ]",
      "ruta": "música/Oscar Santana/Maria Soledad [NzBpg5xXecQ].mp3"
    },
    {
      "nombre": "Murallas De Rencor [739q-QkGsNg] (1)",
      "ruta": "música/Oscar Santana/Murallas De Rencor [739q-QkGsNg] (1).mp3"
    },
    {
      "nombre": "OSCAR SANTANA _LA ÚLTIMA CANCIÓN_ [9PlXMwaEJVw]",
      "ruta": "música/Oscar Santana/OSCAR SANTANA _LA ÚLTIMA CANCIÓN_ [9PlXMwaEJVw].mp3"
    },
    {
      "nombre": "Arena Movediza [vCbHY1ISCKk]",
      "ruta": "música/Oscar Santana/Arena Movediza [vCbHY1ISCKk].mp3"
    },
    {
      "nombre": "Tu No Sabes Querer [VsUHjqCv6oY]",
      "ruta": "música/Oscar Santana/Tu No Sabes Querer [VsUHjqCv6oY].mp3"
    },
    {
      "nombre": "Oscar Santana - La niña Isabel [FyzH5XTexAo]",
      "ruta": "música/Oscar Santana/Oscar Santana - La niña Isabel [FyzH5XTexAo].mp3"
    },
    {
      "nombre": "Oscar Santana - Que lástima [rQtWlZsLu18]",
      "ruta": "música/Oscar Santana/Oscar Santana - Que lástima [rQtWlZsLu18].mp3"
    },
    {
      "nombre": "Dame Otra Oportunidad [9n65-aTJa4M]",
      "ruta": "música/Oscar Santana/Dame Otra Oportunidad [9n65-aTJa4M].mp3"
    },
    {
      "nombre": "Que Seas Feliz [k9zNAmodCUc]",
      "ruta": "música/Oscar Santana/Que Seas Feliz [k9zNAmodCUc].mp3"
    },
    {
      "nombre": "Una Lagrima [vNa91ApHkLs]",
      "ruta": "música/Oscar Santana/Una Lagrima [vNa91ApHkLs].mp3"
    },
    {
      "nombre": "Murallas De Rencor [739q-QkGsNg]",
      "ruta": "música/Oscar Santana/Murallas De Rencor [739q-QkGsNg].mp3"
    }
  ],
  "pastor lopez": [
    {
      "nombre": "Pastor López Sus Mejores Exitos - 30 Grandes Exitos De Pastor López [n_Jrq6aHpjQ]",
      "ruta": "música/pastor lopez/Pastor López Sus Mejores Exitos - 30 Grandes Exitos De Pastor López [n_Jrq6aHpjQ].mp3"
    }
  ],
  "pete conde rodriguez": [
    {
      "nombre": "Areito A Sonar [vDv9FcThnow]",
      "ruta": "música/pete conde rodriguez/Areito A Sonar [vDv9FcThnow].mp3"
    },
    {
      "nombre": "Encántigo [OBeP4qEQOaY]",
      "ruta": "música/pete conde rodriguez/Encántigo [OBeP4qEQOaY].mp3"
    },
    {
      "nombre": "La Abolición [qnX4fpjAOnQ]",
      "ruta": "música/pete conde rodriguez/La Abolición [qnX4fpjAOnQ].mp3"
    },
    {
      "nombre": "Es El Edén [W3RW3PAI4DE]",
      "ruta": "música/pete conde rodriguez/Es El Edén [W3RW3PAI4DE].mp3"
    },
    {
      "nombre": "Gondolero [JQUjhXrxwzM]",
      "ruta": "música/pete conde rodriguez/Gondolero [JQUjhXrxwzM].mp3"
    },
    {
      "nombre": "El Divorcio [3F9aqxim8fc]",
      "ruta": "música/pete conde rodriguez/El Divorcio [3F9aqxim8fc].mp3"
    },
    {
      "nombre": "Perdón Y Olvida [PMNJiWH4m2Q]",
      "ruta": "música/pete conde rodriguez/Perdón Y Olvida [PMNJiWH4m2Q].mp3"
    },
    {
      "nombre": "La Esencia Del Guaguancó [G_cQrxL3v88]",
      "ruta": "música/pete conde rodriguez/La Esencia Del Guaguancó [G_cQrxL3v88].mp3"
    },
    {
      "nombre": "Llegaste Tarde [5Uw5or-UV4E]",
      "ruta": "música/pete conde rodriguez/Llegaste Tarde [5Uw5or-UV4E].mp3"
    },
    {
      "nombre": "Dinga Y Mandinga [eKtgVMmnLG0]",
      "ruta": "música/pete conde rodriguez/Dinga Y Mandinga [eKtgVMmnLG0].mp3"
    },
    {
      "nombre": "La Dicha Mía [WDttv0peQQ8]",
      "ruta": "música/pete conde rodriguez/La Dicha Mía [WDttv0peQQ8].mp3"
    },
    {
      "nombre": "PETE CONDE RODRIGUEZ. _EL TUMBAITO_. [ZoJ1hsg2zXQ]",
      "ruta": "música/pete conde rodriguez/PETE CONDE RODRIGUEZ. _EL TUMBAITO_. [ZoJ1hsg2zXQ].mp3"
    },
    {
      "nombre": "Pete Conde Rodriguez - Catalina La O (Live) [Y3zyOCwFxUk]",
      "ruta": "música/pete conde rodriguez/Pete Conde Rodriguez - Catalina La O (Live) [Y3zyOCwFxUk].mp3"
    },
    {
      "nombre": "Lo Añoro [mc2e6nVK64c]",
      "ruta": "música/pete conde rodriguez/Lo Añoro [mc2e6nVK64c].mp3"
    },
    {
      "nombre": "Los compadres - Pete _El Conde_ Rodríguez [ogPPxDr8SJQ]",
      "ruta": "música/pete conde rodriguez/Los compadres - Pete _El Conde_ Rodríguez [ogPPxDr8SJQ].mp3"
    },
    {
      "nombre": "Pete _El Conde_ Rodríguez - Mi bongo Antillano [I1BUKZO_IwE]",
      "ruta": "música/pete conde rodriguez/Pete _El Conde_ Rodríguez - Mi bongo Antillano [I1BUKZO_IwE].mp3"
    },
    {
      "nombre": "Pete el Conde Rodriguez - El Instrumento [TDvCqo_AGj8]",
      "ruta": "música/pete conde rodriguez/Pete el Conde Rodriguez - El Instrumento [TDvCqo_AGj8].mp3"
    },
    {
      "nombre": "Mujer Ingrata [KVIUQI8SMAw]",
      "ruta": "música/pete conde rodriguez/Mujer Ingrata [KVIUQI8SMAw].mp3"
    },
    {
      "nombre": "Sin Caña Y Sin Platanal [4Cvyc_YbUTc]",
      "ruta": "música/pete conde rodriguez/Sin Caña Y Sin Platanal [4Cvyc_YbUTc].mp3"
    },
    {
      "nombre": "Soy La Ley [BhYQJ09YnrA]",
      "ruta": "música/pete conde rodriguez/Soy La Ley [BhYQJ09YnrA].mp3"
    },
    {
      "nombre": "Pueblo Latino [zGuozXvdoC0]",
      "ruta": "música/pete conde rodriguez/Pueblo Latino [zGuozXvdoC0].mp3"
    },
    {
      "nombre": "Tumbakutun [GAjekimHfCM]",
      "ruta": "música/pete conde rodriguez/Tumbakutun [GAjekimHfCM].mp3"
    },
    {
      "nombre": "Una Guinaita [vXxTfP9-HgA]",
      "ruta": "música/pete conde rodriguez/Una Guinaita [vXxTfP9-HgA].mp3"
    },
    {
      "nombre": "Soñero [dxdYyb0yy2w]",
      "ruta": "música/pete conde rodriguez/Soñero [dxdYyb0yy2w].mp3"
    },
    {
      "nombre": "Yolanda [_wrHkeHRyag]",
      "ruta": "música/pete conde rodriguez/Yolanda [_wrHkeHRyag].mp3"
    },
    {
      "nombre": "Tu Reloj Pastora [hvgH-bJRC2o]",
      "ruta": "música/pete conde rodriguez/Tu Reloj Pastora [hvgH-bJRC2o].mp3"
    }
  ],
  "piero": [
    {
      "nombre": "Piero - Mi viejo (Letra) Viejo, mi querido viejo [iJaIBUe5UgY]",
      "ruta": "música/piero/Piero - Mi viejo (Letra) Viejo, mi querido viejo [iJaIBUe5UgY].mp3"
    }
  ],
  "Renovacion vallenata": [
    {
      "nombre": "LA RENOVACIÓN VALLENATA MIX -Dj JAVIER [6DAzbt3jbXs]",
      "ruta": "música/Renovacion vallenata/LA RENOVACIÓN VALLENATA MIX -Dj JAVIER [6DAzbt3jbXs].mp3"
    },
    {
      "nombre": "RENOVACION VALLENATA VOL 1 DJ KLEIMMER GUILARTE, THE FRONTIER la propia rumba [r4C5usswQcw]",
      "ruta": "música/Renovacion vallenata/RENOVACION VALLENATA VOL 1 DJ KLEIMMER GUILARTE, THE FRONTIER la propia rumba [r4C5usswQcw].mp3"
    }
  ],
  "Roberto Blades": [
    {
      "nombre": "Detalles - Roberto Blades (audio) [-mrqQHqkzf8]",
      "ruta": "música/Roberto Blades/Detalles - Roberto Blades (audio) [-mrqQHqkzf8].mp3"
    },
    {
      "nombre": "FLOR DORMIDA - ROBERTO BLADES [gPo8Y06MMVg]",
      "ruta": "música/Roberto Blades/FLOR DORMIDA - ROBERTO BLADES [gPo8Y06MMVg].mp3"
    },
    {
      "nombre": "La Murga de Panama - Roberto Blades [fZvIfovmltk]",
      "ruta": "música/Roberto Blades/La Murga de Panama - Roberto Blades [fZvIfovmltk].mp3"
    },
    {
      "nombre": "Llorarás [d7vbzA9CCF4]",
      "ruta": "música/Roberto Blades/Llorarás [d7vbzA9CCF4].mp3"
    },
    {
      "nombre": "Papo y Robertito - Roberto Blades feat. Papo Lucca [wmyeJhcZDjA]",
      "ruta": "música/Roberto Blades/Papo y Robertito - Roberto Blades feat. Papo Lucca [wmyeJhcZDjA].mp3"
    },
    {
      "nombre": "Miguelito [4aaGO9Ch2So]",
      "ruta": "música/Roberto Blades/Miguelito [4aaGO9Ch2So].mp3"
    },
    {
      "nombre": "El Drogadicto [NBRlJTNtYWw]",
      "ruta": "música/Roberto Blades/El Drogadicto [NBRlJTNtYWw].mp3"
    },
    {
      "nombre": "Necesito Una Amiga-Salsa Romántica Romantiquisima__ [Ro8epggmWn0]",
      "ruta": "música/Roberto Blades/Necesito Una Amiga-Salsa Romántica Romantiquisima__ [Ro8epggmWn0].mp3"
    },
    {
      "nombre": "Hey [kMlIvb8KGew]",
      "ruta": "música/Roberto Blades/Hey [kMlIvb8KGew].mp3"
    },
    {
      "nombre": "Lagrimas - Roberto Blades (The Palace - Virginia) [Sjed-dybXPo]",
      "ruta": "música/Roberto Blades/Lagrimas - Roberto Blades (The Palace - Virginia) [Sjed-dybXPo].mp3"
    },
    {
      "nombre": "30 Segundos - Roberto Blades [5m2f-StThd8]",
      "ruta": "música/Roberto Blades/30 Segundos - Roberto Blades [5m2f-StThd8].mp3"
    },
    {
      "nombre": "A ti, Roberto Blades [ZGjLQSHBLw0]",
      "ruta": "música/Roberto Blades/A ti, Roberto Blades [ZGjLQSHBLw0].mp3"
    },
    {
      "nombre": "Por El Amor De Una Mujer [yPN8WDb1YOc]",
      "ruta": "música/Roberto Blades/Por El Amor De Una Mujer [yPN8WDb1YOc].mp3"
    },
    {
      "nombre": "por tu amor - roberto blades (salsa) [jx0XOWEgmfU]",
      "ruta": "música/Roberto Blades/por tu amor - roberto blades (salsa) [jx0XOWEgmfU].mp3"
    },
    {
      "nombre": "ROBERTO BLADES - DIME CUAL ES SU NOMBRE _ @SALSA_MX [Si3l0I-dkYc]",
      "ruta": "música/Roberto Blades/ROBERTO BLADES - DIME CUAL ES SU NOMBRE _ @SALSA_MX [Si3l0I-dkYc].mp3"
    },
    {
      "nombre": "Lo que la gente A.C. x _ _ Roberto Blades [F2fdN3nmrWk]",
      "ruta": "música/Roberto Blades/Lo que la gente A.C. x _ _ Roberto Blades [F2fdN3nmrWk].mp3"
    },
    {
      "nombre": "ROBERTO BLADES - LA SELVA DE CEMENTO (1988) L.R.E. [GXRNawkrWcA]",
      "ruta": "música/Roberto Blades/ROBERTO BLADES - LA SELVA DE CEMENTO (1988) L.R.E. [GXRNawkrWcA].mp3"
    },
    {
      "nombre": "Fabricando Fantasias - Tito Nieves feat. Norberto Vélez (Live Sesiones Desde La Loma) [kGyckkCFv0Q]",
      "ruta": "música/Roberto Blades/Fabricando Fantasias - Tito Nieves feat. Norberto Vélez (Live Sesiones Desde La Loma) [kGyckkCFv0Q].mp3"
    },
    {
      "nombre": "Roberto Blades - La solucion [OdRMcmnFRWk](1)",
      "ruta": "música/Roberto Blades/Roberto Blades - La solucion [OdRMcmnFRWk](1).mp3"
    },
    {
      "nombre": "Roberto Blades - La solucion [OdRMcmnFRWk]",
      "ruta": "música/Roberto Blades/Roberto Blades - La solucion [OdRMcmnFRWk].mp3"
    },
    {
      "nombre": "Roberto Blades - Rosas y Espinas (Sonido HQ) [eMpjyXNAYWc]",
      "ruta": "música/Roberto Blades/Roberto Blades - Rosas y Espinas (Sonido HQ) [eMpjyXNAYWc].mp3"
    },
    {
      "nombre": "Roberto Blades - Maria [PPnZA0vx1c0]",
      "ruta": "música/Roberto Blades/Roberto Blades - Maria [PPnZA0vx1c0].mp3"
    },
    {
      "nombre": "Roberto Blades - tempestad [S8qGBxrnOjw]",
      "ruta": "música/Roberto Blades/Roberto Blades - tempestad [S8qGBxrnOjw].mp3"
    },
    {
      "nombre": "Ya no regreso contigo _ Roberto Blades [qqwYjQxUs1E]",
      "ruta": "música/Roberto Blades/Ya no regreso contigo _ Roberto Blades [qqwYjQxUs1E].mp3"
    },
    {
      "nombre": "Tan Enamorado [dTqPyRy9L9M]",
      "ruta": "música/Roberto Blades/Tan Enamorado [dTqPyRy9L9M].mp3"
    },
    {
      "nombre": "Victima De Afecto - Roberto Blades [_EDHNSTGq4s]",
      "ruta": "música/Roberto Blades/Victima De Afecto - Roberto Blades [_EDHNSTGq4s].mp3"
    },
    {
      "nombre": "♫♫Poquita Fe - Roberto Blades - La Casa De La Salsa 14_02_20 [BpnnPeB3vRc]",
      "ruta": "música/Roberto Blades/♫♫Poquita Fe - Roberto Blades - La Casa De La Salsa 14_02_20 [BpnnPeB3vRc].mp3"
    },
    {
      "nombre": "Si Estuvieras Conmigo - Roberto Blades (The Palace - Virginia) [uV_S7HcIN4I]",
      "ruta": "música/Roberto Blades/Si Estuvieras Conmigo - Roberto Blades (The Palace - Virginia) [uV_S7HcIN4I].mp3"
    }
  ],
  "Survivor": [
    {
      "nombre": "wwd.mp3juice.blog - Survivor - Eye Of The Tiger (Official HD Video) (320 KBps)",
      "ruta": "música/Survivor/wwd.mp3juice.blog - Survivor - Eye Of The Tiger (Official HD Video) (320 KBps).mp3"
    }
  ],
  "tambor": [
    {
      "nombre": "Barlovento",
      "ruta": "música/tambor/Barlovento.mp3"
    },
    {
      "nombre": "CANTO",
      "ruta": "música/tambor/CANTO.mp3"
    },
    {
      "nombre": "Dame un Dios",
      "ruta": "música/tambor/Dame un Dios.mp3"
    },
    {
      "nombre": "LA LENGUA _ QUE SE PARE EL TAMBOR VIDEO OFICIAL",
      "ruta": "música/tambor/LA LENGUA _ QUE SE PARE EL TAMBOR VIDEO OFICIAL.mp3"
    },
    {
      "nombre": "Fiebre de Sábado por la noche HD 1977 (1)",
      "ruta": "música/tambor/Fiebre de Sábado por la noche HD 1977 (1).mp3"
    },
    {
      "nombre": "Mix Tambor y Canto Musica ( Cover Tambor Venezolano )",
      "ruta": "música/tambor/Mix Tambor y Canto Musica ( Cover Tambor Venezolano ).mp3"
    },
    {
      "nombre": "MAYORAL TAMBOR URBANO",
      "ruta": "música/tambor/MAYORAL TAMBOR URBANO.mp3"
    },
    {
      "nombre": "El hacha",
      "ruta": "música/tambor/El hacha.mp3"
    },
    {
      "nombre": "No Me Critiques",
      "ruta": "música/tambor/No Me Critiques.mp3"
    },
    {
      "nombre": "Dame un Dios",
      "ruta": "música/tambor/Dame un Dios.mp3"
    },
    {
      "nombre": "A las Mujeres se les da",
      "ruta": "música/tambor/A las Mujeres se les da.mp3"
    },
    {
      "nombre": "TAMBOR URBANO CONCIERTO 33 ANIVERSARIO GRANDES ÉXITOS EN VIVO PARTE 1 FT LOISE",
      "ruta": "música/tambor/TAMBOR URBANO CONCIERTO 33 ANIVERSARIO GRANDES ÉXITOS EN VIVO PARTE 1 FT LOISE.mp3"
    },
    {
      "nombre": "TAMBOR URBANO GRANDES ÉXITOS EN VIVO CONCIERTO 33 ANIVERSARIO FT LOISE PARTE 2",
      "ruta": "música/tambor/TAMBOR URBANO GRANDES ÉXITOS EN VIVO CONCIERTO 33 ANIVERSARIO FT LOISE PARTE 2.mp3"
    },
    {
      "nombre": "Tambor urbano llaneras en tambor",
      "ruta": "música/tambor/Tambor urbano llaneras en tambor.mp3"
    },
    {
      "nombre": "TAMBOR MIX Tambores",
      "ruta": "música/tambor/TAMBOR MIX Tambores.mp3"
    },
    {
      "nombre": "TAMBOR URBANO CONCIERTO 33 ANIVERSARIO EL HACHA EN VIVO FT LOISE PARTE 2",
      "ruta": "música/tambor/TAMBOR URBANO CONCIERTO 33 ANIVERSARIO EL HACHA EN VIVO FT LOISE PARTE 2.mp3"
    },
    {
      "nombre": "La Yuca",
      "ruta": "música/tambor/La Yuca.mp3"
    },
    {
      "nombre": "TAMBOR URBANO QUE SUENEN LOS TAMBORES EN VIVO CONCIERTO 33 ANIVERSARIO",
      "ruta": "música/tambor/TAMBOR URBANO QUE SUENEN LOS TAMBORES EN VIVO CONCIERTO 33 ANIVERSARIO.mp3"
    },
    {
      "nombre": "Andara",
      "ruta": "música/tambor/Andara.mp3"
    },
    {
      "nombre": "TAMBOR URBANO REMIX DE GAITAS FT COQUITO EN VIVO",
      "ruta": "música/tambor/TAMBOR URBANO REMIX DE GAITAS FT COQUITO EN VIVO.mp3"
    },
    {
      "nombre": "TAMBOR URUBANO FT ARMANDO MARTINEZ REMIX EXITOS LLANEROS EN VIVO",
      "ruta": "música/tambor/TAMBOR URUBANO FT ARMANDO MARTINEZ REMIX EXITOS LLANEROS EN VIVO.mp3"
    },
    {
      "nombre": "Tamborero Cumaquero",
      "ruta": "música/tambor/Tamborero Cumaquero.mp3"
    },
    {
      "nombre": "Tambor Urbano Remix Tambores I Son De MI Tierra Primera Temporada",
      "ruta": "música/tambor/Tambor Urbano Remix Tambores I Son De MI Tierra Primera Temporada.mp3"
    }
  ],
  "variados": [
    {
      "nombre": "wwd.mp3juice.blog - Amantes Cobardes Letra (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Amantes Cobardes Letra (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Celia Cruz The Fania All Stars - Quimbara - Zaire, Africa 1974 (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Celia Cruz The Fania All Stars - Quimbara - Zaire, Africa 1974 (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - DÉJALA - Tito Gómez Tito Rojas Video Oficial (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - DÉJALA - Tito Gómez Tito Rojas Video Oficial (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Adolescent s Orquesta - Anhelo (Letra Oficial) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Adolescent s Orquesta - Anhelo (Letra Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Ese soy yo - Willie González (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Ese soy yo - Willie González (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - El Gran Combo - Guaguanco del Gran Combo (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - El Gran Combo - Guaguanco del Gran Combo (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Diego Morán - La Murga (Live) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Diego Morán - La Murga (Live) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Ana Milé, Grupo Niche - Vídeo (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Ana Milé, Grupo Niche - Vídeo (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Banda Blanca - Sopa de Caracol (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Banda Blanca - Sopa de Caracol (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Bobby Valentin - Cuando Te Vea (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Bobby Valentin - Cuando Te Vea (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Cómo Podré Disimular, Tito Gómez - En Vivo (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Cómo Podré Disimular, Tito Gómez - En Vivo (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Cheo Feliciano - Naborí (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Cheo Feliciano - Naborí (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Eddie Santiago Mix - Salsa Romantica Dj.Jesús Alcalá (3ra. Edit) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Eddie Santiago Mix - Salsa Romantica Dj.Jesús Alcalá (3ra. Edit) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Fania All Stars - Pueblo latino (versión inédita) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Fania All Stars - Pueblo latino (versión inédita) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Esa Mujer - Tony Vega (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Esa Mujer - Tony Vega (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Fania All Stars - Siento (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Fania All Stars - Siento (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Fulanito - El Cepillo(VDj Gg Que Comience La Fiesta 2021) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Fulanito - El Cepillo(VDj Gg Que Comience La Fiesta 2021) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Grandes Éxitos de Willie Colon , salsa vieja, salsa pesada (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Grandes Éxitos de Willie Colon , salsa vieja, salsa pesada (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Ismael Miranda - Careta, The Last Salsa Legend En Vivo (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Ismael Miranda - Careta, The Last Salsa Legend En Vivo (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Grupo Niche - Algo Que Se Quede (Video Oficial) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Grupo Niche - Algo Que Se Quede (Video Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Jerry Rivera - Amores Como el Nuestro (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Jerry Rivera - Amores Como el Nuestro (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Ismael Rivera Rafael Cortijo - La Soledad (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Ismael Rivera Rafael Cortijo - La Soledad (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Jerry Rivera - Dame un beso asi (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Jerry Rivera - Dame un beso asi (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Héctor Lavoe Exitos Mix - 30 Grandes Exitos - Musica Cristiana 2018 (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Héctor Lavoe Exitos Mix - 30 Grandes Exitos - Musica Cristiana 2018 (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Jerry Rivera - Mi Libertad ft.Voltio (Video Oficial) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Jerry Rivera - Mi Libertad ft.Voltio (Video Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Jerry Rivera - Vuela Muy Alto (Video Oficial) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Jerry Rivera - Vuela Muy Alto (Video Oficial) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Joe Arroyo y La Verdad - En Barranquilla me Quedo (Video Oficial) Discos Fuentes (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Joe Arroyo y La Verdad - En Barranquilla me Quedo (Video Oficial) Discos Fuentes (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Justo Betancourt - Pedregal (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Justo Betancourt - Pedregal (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Fania All Star - Son Cuero y Boogaloo (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Fania All Star - Son Cuero y Boogaloo (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - JUGUETE De Nadie - Puerto Rican Power Video Oficial (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - JUGUETE De Nadie - Puerto Rican Power Video Oficial (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Las Chicas Del Can - Juana La Cubana (versión discoteca) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Las Chicas Del Can - Juana La Cubana (versión discoteca) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - KULIKITAKA (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - KULIKITAKA (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Lo Mejor De Charlie Zaa Sentimientos Album Completo 2021 Charlie Zaa (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Lo Mejor De Charlie Zaa Sentimientos Album Completo 2021 Charlie Zaa (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Justo Betancourt, Papo Lucca, Johnny Pacheco, and Celia Cruz - Ahora Sí (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Justo Betancourt, Papo Lucca, Johnny Pacheco, and Celia Cruz - Ahora Sí (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Los Karkiks - Se Menea (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Los Karkiks - Se Menea (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Los Del Rio - Macarena (Bayside Boys Remix) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Los Del Rio - Macarena (Bayside Boys Remix) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Luigi Texidor Los clásicos de la salsa en un Mix Linda Teresa, Bomba Carambomba, Naci Moreno (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Luigi Texidor Los clásicos de la salsa en un Mix Linda Teresa, Bomba Carambomba, Naci Moreno (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Marc Anthony - Flor Pálida (Official Video) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Marc Anthony - Flor Pálida (Official Video) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Los Embajadores Vallenatos – Se Le Moja La Canoa – A Oscuras Pero Encendidos (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Los Embajadores Vallenatos – Se Le Moja La Canoa – A Oscuras Pero Encendidos (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Nadie Es ETERNO - Tito Rojas Vídeo Oficial (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Nadie Es ETERNO - Tito Rojas Vídeo Oficial (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Nuestro Sueño, Grupo Niche, Video Letra - Salsa Power (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Nuestro Sueño, Grupo Niche, Video Letra - Salsa Power (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Orquesta El Sabor De Nacho - Rumba Moderna (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Orquesta El Sabor De Nacho - Rumba Moderna (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Nuestro Sueño, Tito Gómez - En Vivo (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Nuestro Sueño, Tito Gómez - En Vivo (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Oro Solido - La Tanguita Roja (OFFICIAL) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Oro Solido - La Tanguita Roja (OFFICIAL) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Orquesta El Sabor De Nacho - Sanson Batalla (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Orquesta El Sabor De Nacho - Sanson Batalla (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Paquito Guzman - Cinco Noches (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Paquito Guzman - Cinco Noches (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Pete El Conde Rodríguez - Catalina La O (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Pete El Conde Rodríguez - Catalina La O (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Orquesta El Sabor De Nacho - Rumba Pa Los Rumberos (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Orquesta El Sabor De Nacho - Rumba Pa Los Rumberos (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Pagina De AMOR - Tito Gómez Video Oficial (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Pagina De AMOR - Tito Gómez Video Oficial (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - POR ESO YO CANTO SALSA- FANIA ALL STARS (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - POR ESO YO CANTO SALSA- FANIA ALL STARS (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Quítate Tú. Fania All-Stars (Our Latin Thing) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Quítate Tú. Fania All-Stars (Our Latin Thing) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Ray Barretto - Vive Y Vacila (320 KBps) (1)",
      "ruta": "música/variados/wwd.mp3juice.blog - Ray Barretto - Vive Y Vacila (320 KBps) (1).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Ray Barretto - Vive Y Vacila (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Ray Barretto - Vive Y Vacila (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Richie Ray Bobby Cruz - Sonido Bestial (Live) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Richie Ray Bobby Cruz - Sonido Bestial (Live) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Se Pareció Tanto A Ti, Grupo Niche, Video Letra - Salsa Power (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Se Pareció Tanto A Ti, Grupo Niche, Video Letra - Salsa Power (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Si SUPIERA - Willie González Video Oficial (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Si SUPIERA - Willie González Video Oficial (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Si Tu FUERAS Mia - Willie González Video Oficial (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Si Tu FUERAS Mia - Willie González Video Oficial (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Sin Sentimiento, Grupo Niche, Video Letra - Salsa Power (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Sin Sentimiento, Grupo Niche, Video Letra - Salsa Power (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Sonora Ponceña Fuego En El 23 (Live) (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Sonora Ponceña Fuego En El 23 (Live) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Sonora Ponceña - Moreno Soy (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Sonora Ponceña - Moreno Soy (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Sonora Ponceña - Moreno Soy (320 KBps) (1)",
      "ruta": "música/variados/wwd.mp3juice.blog - Sonora Ponceña - Moreno Soy (320 KBps) (1).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Tito Gomez - Amor de Papel (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Tito Gomez - Amor de Papel (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vuela la Paloma- Fania All Star (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Vuela la Paloma- Fania All Star (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Tu Amigo O Tu Amante - La Sabrosura Orquesta Discos Fuentes (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Tu Amigo O Tu Amante - La Sabrosura Orquesta Discos Fuentes (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Willie Colón Héctor Lavoe - Abuelita (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Willie Colón Héctor Lavoe - Abuelita (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Willie Gonzalez - Devuelveme (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Willie Gonzalez - Devuelveme (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Willie Gonzalez - Pensando En Ti (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Willie Gonzalez - Pensando En Ti (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Willie gonzalez - Tanto Amor (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Willie gonzalez - Tanto Amor (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Tito Rojas Mix Exitos - Salsa Romanticas Mix 2022 - Las Mejores Canciones De Tito Rojas (320 KBps)",
      "ruta": "música/variados/wwd.mp3juice.blog - Tito Rojas Mix Exitos - Salsa Romanticas Mix 2022 - Las Mejores Canciones De Tito Rojas (320 KBps).mp3"
    }
  ],
  "vicente fernandez": [
    {
      "nombre": "Vicente Fernández - El Ayudante (Letra _ Lyrics) [VPO73iJ4l5o]",
      "ruta": "música/vicente fernandez/Vicente Fernández - El Ayudante (Letra _ Lyrics) [VPO73iJ4l5o].mp3"
    },
    {
      "nombre": "Vicente Fernández - A Mi Manera (En Vivo)[Un Azteca en el Azteca] [9F_BRjGi3L8]",
      "ruta": "música/vicente fernandez/Vicente Fernández - A Mi Manera (En Vivo)[Un Azteca en el Azteca] [9F_BRjGi3L8].mp3"
    },
    {
      "nombre": "Vicente Fernández - No Me Hagas Menos (Letra _ Lyrics) [hr9cRW0mUQM]",
      "ruta": "música/vicente fernandez/Vicente Fernández - No Me Hagas Menos (Letra _ Lyrics) [hr9cRW0mUQM].mp3"
    },
    {
      "nombre": "Vicente Fernández - Señora de Tal (Letra_Lyrics) [ddtvc9j5XXc]",
      "ruta": "música/vicente fernandez/Vicente Fernández - Señora de Tal (Letra_Lyrics) [ddtvc9j5XXc].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Acá Entre Nos (En Vivo) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Acá Entre Nos (En Vivo) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - A Pesar de Todo (En Vivo) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - A Pesar de Todo (En Vivo) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Alejandro Fernández - Mátalas (En Vivo) Un Azteca en el Azteca (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Alejandro Fernández - Mátalas (En Vivo) Un Azteca en el Azteca (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Con la Misma Tijera (Cover Audio) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Con la Misma Tijera (Cover Audio) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Cuando Yo Quería Ser Grande (Letra Lyrics) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Cuando Yo Quería Ser Grande (Letra Lyrics) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Pedrito Fernández - La de La Mochila Azul (HD) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Pedrito Fernández - La de La Mochila Azul (HD) (320 KBps).mp3"
    },
    {
      "nombre": "Antonio Aguilar - El Hijo Desobediente (Video Oficial) [q4vLDz4pmxc]",
      "ruta": "música/vicente fernandez/Antonio Aguilar - El Hijo Desobediente (Video Oficial) [q4vLDz4pmxc].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - El Chofer (320 KBps) (1)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - El Chofer (320 KBps) (1).mp3"
    },
    {
      "nombre": "Vicente Fernández - Mujeres Divinas (En Vivo) [xa2GLqL12Zk]",
      "ruta": "música/vicente fernandez/Vicente Fernández - Mujeres Divinas (En Vivo) [xa2GLqL12Zk].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - El Chofer (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - El Chofer (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Estos Celos (En Vivo) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Estos Celos (En Vivo) (320 KBps).mp3"
    },
    {
      "nombre": "Un Millón de Primaveras [b393RtiIA18]",
      "ruta": "música/vicente fernandez/Un Millón de Primaveras [b393RtiIA18].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - La Derrota (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - La Derrota (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - La Ley del Monte (En Vivo) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - La Ley del Monte (En Vivo) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Los Tiros de Mi Canana (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Los Tiros de Mi Canana (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Nos Estorbo La ropa ((Cover Audio La Leyenda Viviente) (Video)) (320 KBps) (1)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Nos Estorbo La ropa ((Cover Audio La Leyenda Viviente) (Video)) (320 KBps) (1).mp3"
    },
    {
      "nombre": "Vicente Fernández - Qué de Raro Tiene (Letra_Lyrics) [NL8e8Wx9UZw]",
      "ruta": "música/vicente fernandez/Vicente Fernández - Qué de Raro Tiene (Letra_Lyrics) [NL8e8Wx9UZw].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Sublime Mujer (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Sublime Mujer (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Hermoso Cariño (En Vivo) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Hermoso Cariño (En Vivo) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Nos Estorbo La ropa ((Cover Audio La Leyenda Viviente) (Video)) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Nos Estorbo La ropa ((Cover Audio La Leyenda Viviente) (Video)) (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Y Me Acordé de Ti (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Y Me Acordé de Ti (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - No Me Sé Rajar Letra (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - No Me Sé Rajar Letra (320 KBps).mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - La Diferencia (Letra Lyrics) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - La Diferencia (Letra Lyrics) (320 KBps).mp3"
    },
    {
      "nombre": "Vicente Fernández - Cruz de Olvido (Letra _ Lyrics) [Q80KELpfYXE]",
      "ruta": "música/vicente fernandez/Vicente Fernández - Cruz de Olvido (Letra _ Lyrics) [Q80KELpfYXE].mp3"
    },
    {
      "nombre": "wwd.mp3juice.blog - Vicente Fernández - Las Botas Del Charro (Audio) (320 KBps)",
      "ruta": "música/vicente fernandez/wwd.mp3juice.blog - Vicente Fernández - Las Botas Del Charro (Audio) (320 KBps).mp3"
    }
  ],
  "yoe arroyo": [
    {
      "nombre": "wwd.mp3juice.blog - Joe Arroyo Éxitos Sus Mejores Canciones - 10 Super Éxitos Románticas Inolvidables Mix (320 KBps)",
      "ruta": "música/yoe arroyo/wwd.mp3juice.blog - Joe Arroyo Éxitos Sus Mejores Canciones - 10 Super Éxitos Románticas Inolvidables Mix (320 KBps).mp3"
    }
  ]
};
  let reproductor, tituloActual, indice = 0;
  let cancionesActivas = [];

  function toggleMenu() {
    const menu = document.getElementById('menu-musica');
    menu.style.display = menu.style.display === 'none' ? 'block' : 'none';
  }

  function mostrarCategoria(categoria) {
    const contenedor = document.getElementById('contenedor-musica');
    contenedor.innerHTML = "";
    cancionesActivas = categorias[categoria];
    indice = 0;

    const titulo = document.createElement("h3");
    titulo.textContent = "🎧 " + categoria.charAt(0).toUpperCase() + categoria.slice(1);
    contenedor.appendChild(titulo);

    cancionesActivas.forEach((cancion, i) => {
      const fila = document.createElement("div");
      fila.className = "cancion-fila";

      const nombre = document.createElement("span");
      nombre.textContent = "🎵 " + cancion.nombre;
      nombre.onclick = () => reproducirIndice(i);

      const descargar = document.createElement("a");
      descargar.href = cancion.ruta;
      descargar.download = "";
      descargar.textContent = "⬇️ Descargar";
      descargar.className = "boton-descarga";

      fila.appendChild(nombre);
      fila.appendChild(descargar);
      contenedor.appendChild(fila);
    });

    reproductor = document.createElement("audio");
    reproductor.controls = true;
    reproductor.style.marginTop = "10px";
    reproductor.style.filter = "drop-shadow(0 0 8px #39ff14)";
    contenedor.appendChild(reproductor);

    reproductor.addEventListener("ended", siguiente);
    reproductor.addEventListener("timeupdate", () => {
      const led = document.getElementById("imagen-led");
      const colores = ["#39ff14", "#ff1493", "#00ffff", "#ff9900", "#ff2222"];
      const color = colores[Math.floor(Math.random() * colores.length)];
      led.style.boxShadow = `0 0 25px ${color}`;
      led.style.borderColor = color;
    });

    tituloActual = document.createElement("div");
    tituloActual.id = "titulo-cancion";
    tituloActual.textContent = "Selecciona una canción";
    contenedor.appendChild(tituloActual);

    const botones = document.createElement("div");
    botones.innerHTML = `
      <button onclick="anterior()">⏮️ Anterior</button>
      <button onclick="reproducir()">▶️ Reproducir</button>
      <button onclick="detener()">⏹️ Detener</button>
      <button onclick="siguiente()">⏭️ Siguiente</button>
    `;
    contenedor.appendChild(botones);

    reproducirIndice(0);
  }

  function reproducirIndice(i) {
    indice = i;
    reproductor.src = cancionesActivas[i].ruta;
    tituloActual.textContent = cancionesActivas[i].nombre;
    reproductor.play();
  }
  function siguiente() {
    indice = (indice + 1) % cancionesActivas.length;
    reproducirIndice(indice);
  }

  function anterior() {
    indice = (indice - 1 + cancionesActivas.length) % cancionesActivas.length;
    reproducirIndice(indice);
  }

  function reproducir() {
    if (reproductor && reproductor.src) {
      reproductor.play();
    }
  }

  function detener() {
    if (reproductor) {
      reproductor.pause();
      reproductor.currentTime = 0;
    }
  }
function buscarCanciones() {
  const termino = document.getElementById("buscador").value.toLowerCase();
  const contenedor = document.getElementById("contenedor-musica");
  contenedor.innerHTML = "";

  if (!termino.trim()) return; // no buscar si está vacío

  let resultados = [];

  for (const categoria in categorias) {
    categorias[categoria].forEach(cancion => {
      const nombreCancion = cancion.nombre.toLowerCase();
      const nombreCategoria = categoria.toLowerCase();
      if (nombreCancion.includes(termino) || nombreCategoria.includes(termino)) {
        resultados.push({ ...cancion, artista: categoria });
      }
    });
  }

  if (resultados.length === 0) {
    contenedor.innerHTML = "<h3>😢 No se encontraron resultados</h3>";
    return;
  }

  const titulo = document.createElement("h3");
  titulo.textContent = "🎧 Resultados de búsqueda:";
  contenedor.appendChild(titulo);

  resultados.forEach((cancion, i) => {
    const fila = document.createElement("div");
    fila.className = "cancion-fila";

    const nombre = document.createElement("span");
    nombre.textContent = `🎵 ${cancion.nombre} — (${cancion.artista})`;
    nombre.onclick = () => {
      cancionesActivas = resultados;
      indice = i;
      reproducirIndice(i);
    };

    const descargar = document.createElement("a");
    descargar.href = cancion.ruta;
    descargar.download = "";
    descargar.textContent = "⬇️ Descargar";
    descargar.className = "boton-descarga";

    fila.appendChild(nombre);
    fila.appendChild(descargar);
    contenedor.appendChild(fila);
  });

  // Agrega reproductor
  reproductor = document.createElement("audio");
  reproductor.controls = true;
  contenedor.appendChild(reproductor);

  tituloActual = document.createElement("div");
  tituloActual.id = "titulo-cancion";
  tituloActual.textContent = "Selecciona una canción";
  contenedor.appendChild(tituloActual);

  const botones = document.createElement("div");
  botones.innerHTML = `
    <button onclick="anterior()">⏮️ Anterior</button>
    <button onclick="reproducir()">▶️ Reproducir</button>
    <button onclick="detener()">⏹️ Detener</button>
    <button onclick="siguiente()">⏭️ Siguiente</button>
  `;
  contenedor.appendChild(botones);
}
</script>
</body>
</html>

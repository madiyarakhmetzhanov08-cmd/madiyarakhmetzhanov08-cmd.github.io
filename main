<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Зарина - Қыз ұзату шақыртуы</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Alice&family=Montserrat:wght@300;400;500;600&family=Great+Vibes&display=swap" rel="stylesheet">
    
    <style>
        :root {
            /* Түстер палитрасы */
            --bg-color-base: #f5f0e6; /* Негізгі бежевый түс */
            --gold: #b8935d; /* Алтын түс */
            --gold-dark: #967646; /* Күңгірт алтын */
            --dark: #3e3e3e; /* Қара-сұр мәтін */
            --border: #e0d5c8; /* Жиектер түсі */
            --soft-green: #7b8a7b; /* Батырма түсі */
            --white: #ffffff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            /* Бежевый текстурлы фон (SVG арқылы мата текстурасы сияқты) */
            background-color: var(--bg-color-base);
            background-image: url('data:image/svg+xml,%3Csvg xmlns="http://www.w3.org/2000/svg" width="4" height="4" viewBox="0 0 4 4"%3E%3Cpath fill="%23c4bda3" fill-opacity="0.15" d="M1 3h1v1H1V3zm2-2h1v1H2V1z"%3E%3C/path%3E%3C/svg%3E');
            
            font-family: 'Alice', serif; /* Қазақша шрифт */
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Анимация үшін стильдер */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 1s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Негізгі контейнер */
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 60px 20px;
            text-align: center;
        }

        /* Басқы бөлім (Үстіңгі жазу) */
        .header-section {
            margin-bottom: 60px;
            position: relative;
        }

        /* Декоративті сызықтар */
        .header-section::before,
        .header-section::after {
            content: '';
            display: block;
            width: 80px;
            height: 1px;
            background-color: var(--border);
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
        }
        .header-section::before { top: -20px; }
        .header-section::after { bottom: -20px; }

        .main-title {
            font-size: 4.5rem;
            color: var(--gold);
            font-family: 'Great Vibes', cursive;
            margin-bottom: 5px;
            text-shadow: 1px 1px 1px rgba(0,0,0,0.05);
        }

        .event-type {
            text-transform: uppercase;
            letter-spacing: 5px;
            font-size: 1.2rem;
            font-family: 'Montserrat', sans-serif;
            color: var(--gold-dark);
            font-weight: 500;
        }

        /* Эстетикалық Арка (Сурет контейнері) */
        .arch-container {
            width: 320px;
            height: 480px;
            margin: 50px auto;
            border: 3px double var(--gold); /* Қос алтын жиек */
            border-radius: 160px 160px 20px 20px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 15px 40px rgba(184, 147, 93, 0.2);
            padding: 5px; /* Ішкі шегініс */
            background-color: var(--white);
        }

        .arch-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 155px 155px 15px 15px;
        }

        /* Басты мәтін блогы */
        .invite-content {
            margin-bottom: 70px;
        }

        .invite-content h2 {
            font-size: 2.4rem;
            margin-bottom: 30px;
            color: var(--dark);
            font-weight: normal;
        }

        .invite-text {
            font-size: 1.35rem;
            padding: 0 10px;
            font-style: italic;
        }

        /* Күнтізбе бөлімі */
        .calendar-box {
            margin: 70px 0;
            padding: 40px 20px;
            background-color: var(--white);
            border-radius: 20px;
            border: 1px solid var(--border);
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .calendar-month-title {
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 1rem;
            color: var(--gold-dark);
            font-weight: bold;
            margin-bottom: 20px;
            font-family: 'Montserrat', sans-serif;
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            max-width: 340px;
            margin: 0 auto;
            font-family: 'Montserrat', sans-serif;
        }

        .day-name { font-weight: 600; color: #aaa; font-size: 0.85rem; padding-bottom: 15px; }
        .day { padding: 12px 0; font-size: 1.1rem; color: #555; }
        
        /* Ерекшеленген күн (28 маусым) */
        .active-day {
            background-color: var(--gold);
            color: var(--white);
            border-radius: 50%;
            font-weight: bold;
            position: relative;
            box-shadow: 0 3px 6px rgba(184, 147, 93, 0.4);
        }

        .exact-time {
            margin-top: 30px;
            font-weight: bold;
            font-size: 1.6rem;
            color: var(--dark);
            border-top: 1px solid var(--border);
            padding-top: 20px;
            display: inline-block;
        }

        /* Таймер стилі */
        .timer-title { margin-top: 60px; font-size: 1.3rem; color: var(--gold-dark); }
        .timer-display {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8rem;
            color: var(--dark);
            margin: 15px 0 70px;
            font-weight: 300;
            letter-spacing: 1px;
        }

        /* Мекен-жай бөлімі */
        .location-box {
            margin-bottom: 80px;
            background-color: var(--white);
            padding: 40px 20px;
            border-radius: 20px;
            border: 1px solid var(--border);
        }

        .location-icon { font-size: 3rem; display: block; margin-bottom: 15px; color: var(--gold); }
        .city-name { font-size: 1.2rem; text-transform: uppercase; letter-spacing: 2px; color: #888; margin-bottom: 5px; font-family: 'Montserrat', sans-serif;}
        .restaurant { font-size: 2.2rem; color: var(--gold); margin: 5px 0 15px; font-weight: normal;}
        
        /* 2ГИС сілтемесін батырма ретінде жасау */
        .gis-link {
            display: inline-block;
            margin-top: 15px;
            color: var(--gold-dark);
            text-decoration: none;
            border: 1px solid var(--gold);
            padding: 10px 25px;
            border-radius: 25px;
            font-family: 'Montserrat', sans-serif;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s;
        }
        .gis-link:hover {
            background-color: var(--gold);
            color: var(--white);
        }

        /* RSVP (Жауап беру) Формасы */
        .rsvp-form {
            background: var(--white);
            padding: 50px 30px;
            border-radius: 30px;
            border: 1px solid var(--border);
            box-shadow: 0 20px 50px rgba(184, 147, 93, 0.15);
        }

        .rsvp-form h3 {
            font-size: 1.6rem;
            margin-bottom: 35px;
            color: var(--dark);
            font-weight: normal;
        }

        .input-group {
            margin-bottom: 25px;
            text-align: left;
        }

        input[type="text"] {
            width: 100%;
            padding: 20px;
            border: 1px solid #e5e5e5;
            background: #fcfcfc;
            border-radius: 15px;
            outline: none;
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
            transition: 0.3s;
        }

        input[type="text"]:focus { border-color: var(--gold); background: var(--white); }

        .radio-options {
            margin-top: 18px;
            font-family: 'Montserrat', sans-serif;
        }

        .radio-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            font-size: 1rem;
            cursor: pointer;
            color: #555;
        }

        .radio-item input { margin-right: 15px; accent-color: var(--gold); width: 18px; height: 18px;}

        .btn-submit {
            width: 100%;
            background-color: var(--soft-green);
            color: var(--white);
            border: none;
            padding: 20px;
            border-radius: 15px;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 600;
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
            cursor: pointer;
            margin-top: 15px;
            transition: background 0.3s;
        }
        .btn-submit:hover { background-color: #616e61; }

        /* Футер (Төменгі жағы) */
        .footer-hosts {
            margin-top: 60px;
            color: #888;
            font-size: 0.95rem;
            font-style: italic;
            border-top: 1px solid var(--border);
            padding-top: 30px;
        }

    </style>
</head>
<body>

    <div class="container">
        
        <div class="header-section reveal">
            <h1 class="main-title">Зарина</h1>
            <p class="event-type">Қыз ұзату</p>
        </div>

        <div class="arch-container reveal">
            <img src="https://images.unsplash.com/photo-1523438885200-e635ba2c371e?q=80&w=600" alt="Kyz Uzatu Dina">
        </div>

        <div class="invite-content reveal">
            <h2>Құрметті қонақтар!</h2>
            <p class="invite-text">
                Аяулы қызымыз Заринаны аялы алақанымыздан - құтты босағасына шығарып салу рәсіміне арналған салтанатты дастарханымыздың қадірлі қонағы болуға шақырамыз!
            </p>
        </div>

        <div class="calendar-box reveal">
            <p class="calendar-month-title">Маусым 2026</p>
            <div class="calendar-grid">
                <div class="day-name">Дс</div><div class="day-name">Сс</div><div class="day-name">Ср</div><div class="day-name">Бс</div><div class="day-name">Жм</div><div class="day-name">Сб</div><div class="day-name">Жс</div>
                
                <div class="day">1</div><div class="day">2</div><div class="day">3</div><div class="day">4</div><div class="day">5</div><div class="day">6</div><div class="day">7</div>
                <div class="day">8</div><div class="day">9</div><div class="day">10</div><div class="day">11</div><div class="day">12</div><div class="day">13</div><div class="day">14</div>
                <div class="day">15</div><div class="day">16</div><div class="day">17</div><div class="day">18</div><div class="day">19</div><div class="day">20</div><div class="day">21</div>
                <div class="day">22</div><div class="day">23</div><div class="day">24</div><div class="day">25</div><div class="day">26</div><div class="day">27</div>
                <div class="day active-day">28</div>
                <div class="day">29</div><div class="day">30</div>
            </div>
            <p class="exact-time">28 МАУСЫМ | САҒАТ 15:00</p>
        </div>

        <p class="timer-title reveal">Тойға дейін қалды:</p>
        <div id="timer" class="timer-display reveal">...күн ...сағат ...минут</div>

        <div class="location-box reveal">
            <span class="location-icon">📍</span>
            <p class="city-name">Көкшетау қаласы</p>
            <h3 class="restaurant">"Ақмол"</h3>
            <p>мейрамханасы</p>
            <p>Абай көшесі, 137Б</p>
            <br>
            <a href="https://go.2gis.com/roXz3" target="_blank" class="gis-link">2ГИС картамен ашу</a>
        </div>

        <div class="rsvp-form reveal">
            <h3>Тойға келетініңізді растауыңызды сұраймыз:</h3>
            
            <div class="input-group">
                <input type="text" id="guestName" placeholder="Аты-жөніңізді жазыңыз">
            </div>

            <div class="input-group">
                <div class="radio-options">
                    <label class="radio-item"><input type="radio" name="rsvp" value="yes"> Иә, келемін</label>
                    <label class="radio-item"><input type="radio" name="rsvp" value="pair"> Жұбайыммен келемін</label>
                    <label class="radio-item"><input type="radio" name="rsvp" value="no"> Өкінішке орай, келе алмаймын</label>
                </div>
            </div>

            <button class="btn-submit" onclick="sendToWhatsApp()">Жіберу</button>
        </div>

        <p class="footer-hosts reveal">Той иелері: Әкесі - Аслан, анасы - Марал</p>

    </div>

    <script>
        // СКРОЛЛ АНИМАЦИЯСЫ: Блоктар экранға шыққанда көрінеді
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.reveal').forEach((el) => observer.observe(el));

        // ТАЙМЕР ФУНКЦИЯСЫ (Жаңа дата: 28 маусым 2026, 15:00)
        function updateTimer() {
            const eventDate = new Date("June 28, 2026 15:00:00").getTime();
            const now = new Date().getTime();
            const diff = eventDate - now;

            if (diff <= 0) {
                document.getElementById("timer").innerHTML = "Той басталды! 🎉";
                return;
            }

            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const mins = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));

            // Нөлдік мәндерді көрсетпеу (күн сөзін дұрыс септеуді қоспағанда)
            document.getElementById("timer").innerHTML = `${days} күн ${hours} сағат ${mins} минут`;
        }
        setInterval(updateTimer, 1000);
        updateTimer();

        // WHATSAPP-ҚА ЖІБЕРУ ФУНКЦИЯСЫ
        function sendToWhatsApp() {
            const name = document.getElementById('guestName').value;
            const status = document.querySelector('input[name="rsvp"]:checked')?.value;
            
            if(!name || !status) {
                alert("Өтінеміз, атыңызды жазып, таңдау жасаңыз.");
                return;
            }

            let statusText = "";
            if(status === 'yes') statusText = "Келемін! ✅";
            if(status === 'pair') statusText = "Жұбайыммен келемін! 👨‍👩‍👧";
            if(status === 'no') statusText = "Өкінішке орай, келе алмаймын. ❌";

            const text = `Сәлеметсіз бе! Мен ${name}. Заринаның ұзату тойына шақыртуыңызды алдым. Жауабым: ${statusText}`;

            // Осы жерге жауаптарды алатын WhatsApp нөмірін жазыңыз (мысалы: 77071234567)
            const phone = "77071234567"; 
            window.open(`https://wa.me/${phone}?text=${encodeURIComponent(text)}`, '_blank');
        }
    </script>
</body>
</html>

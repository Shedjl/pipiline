<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>pipeline — Официальный клан на ZLP.ONL</title>

  <!-- Tailwind + font -->
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#ff6600',
            card: '#1a1a1a',
            secondary: '#333333'
          },
          fontFamily: { sans: ['Montserrat','sans-serif'] },
          borderRadius: { xl: '0.75rem', '2xl': '1rem' }
        }
      }
    }
  </script>

  <style>
    :root {
      --primary: #ff6600;
      --card: #1a1a1a;
    }
    * { font-family: 'Montserrat', sans-serif; }
    body { background:#000; color:#fff; }

    /* Loader */
    .loader {
      position: fixed; inset: 0;
      background: rgba(0,0,0,0.9);
      backdrop-filter: blur(8px);
      display: flex; align-items: center; justify-content: center;
      z-index: 50; opacity: 0; visibility: hidden; transition: .3s;
    }
    .loader.show { opacity: 1; visibility: visible; }
    .progress-bar{width:16rem;height:4px;background:#374151;border-radius:9999px;overflow:hidden}
    .progress-fill{height:100%;background:var(--primary);width:0;border-radius:9999px;transition:width 1.2s ease}

    /* Hero fade (без видео) */
    .hero-fade{position:relative}
    .hero-fade::after{
      content:'';position:absolute;bottom:0;left:0;right:0;height:60px;
      background:linear-gradient(to bottom, rgba(0,0,0,0) 0%, #000 100%);
      pointer-events:none
    }

    /* Buttons */
    .btn-minimal{position:relative;transition:.2s;overflow:hidden;cursor:pointer}
    .btn-minimal::before{
      content:'';position:absolute;top:50%;left:50%;width:0;height:0;
      background:rgba(255,255,255,.1);border-radius:50%;
      transform:translate(-50%,-50%);transition:width .3s,height .3s
    }
    .btn-minimal:hover{transform:scale(1.02);box-shadow:0 4px 20px rgba(255,102,0,.3)}
    .btn-minimal:hover::before{width:200%;height:200%}
    .btn-minimal:active{transform:scale(.98)}
  </style>
</head>
<body class="bg-black text-white overflow-x-hidden">

  <!-- Loader -->
  <div class="loader" id="loader">
    <div class="text-center">
      <div class="mb-8">
        <h1 class="text-5xl font-extrabold">
          <span class="text-primary">pipeline</span>
        </h1>
      </div>
      <div class="w-64 mx-auto">
        <div class="progress-bar">
          <div class="progress-fill" id="progressFill"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- Page -->
  <div class="min-h-screen bg-black">

    <!-- Hero (без видео) -->
    <section id="home" class="relative min-h-screen flex items-center justify-center overflow-hidden hero-fade">
      <div class="absolute inset-0 bg-black/60 z-0"></div>
      <div class="relative z-10 text-center max-w-4xl mx-auto px-4">
        <h1 class="text-6xl md:text-8xl font-extrabold mb-6">
          <span class="text-primary">pipeline</span>
        </h1>
        <p class="text-lg text-gray-400 mb-8">
          Добро пожаловать на сайт клана pipeline. Следите за новостями клана и всего сервера!
        </p>
        <button onclick="scrollToJoin()" class="bg-primary text-white hover:bg-primary/90 px-8 py-3 text-lg btn-minimal rounded-md font-medium">
          Вступить в клан
        </button>
      </div>
    </section>

    <!-- Team -->
    <section id="team" class="py-20 bg-black">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-4xl md:text-5xl font-extrabold mb-6">Команда <span class="text-primary">pipeline</span></h2>
          <p class="text-xl text-gray-400 max-w-2xl mx-auto">
            Познакомьтесь с руководством нашего клана.
          </p>
        </div>

        <!-- Leader -->
        <div class="mb-20">
          <div class="max-w-md mx-auto text-center bg-card border border-primary/20 rounded-2xl p-8">
            <div class="mx-auto w-40 h-40 mb-6 rounded-full overflow-hidden border-4 border-primary/30">
              <img src="https://minecraftpfp.com/PFP/tommyinnit.png" alt="mgcode" class="w-full h-full object-cover">
            </div>
            <h3 class="text-3xl font-bold mb-3">mgcode</h3>
            <h4 class="text-primary font-semibold mb-2 text-xl">Лидер клана</h4>
            <p class="text-gray-400 leading-relaxed">
              Основатель и главный организатор клана pipeline. Отвечает за стратегическое развитие и ключевые решения.
            </p>
          </div>
        </div>

        <!-- Deputies -->
        <div class="mb-20">
          <div class="grid md:grid-cols-3 gap-8 max-w-5xl mx-auto">
            <!-- vixip -->
            <div class="text-center bg-card border border-primary/20 rounded-2xl p-8">
              <div class="mx-auto w-32 h-32 mb-6 rounded-full overflow-hidden border-3 border-primary/30">
                <img src="https://minecraftpfp.com/PFP/tommyinnit.png" alt="vixip" class="w-full h-full object-cover">
              </div>
              <h3 class="text-2xl font-bold mb-2">vixip</h3>
              <h4 class="text-primary font-semibold">Заместитель лидера</h4>
            </div>
            <!-- Mafry_D -->
            <div class="text-center bg-card border border-primary/20 rounded-2xl p-8">
              <div class="mx-auto w-32 h-32 mb-6 rounded-full overflow-hidden border-3 border-primary/30">
                <img src="https://minecraftpfp.com/PFP/tommyinnit.png" alt="Mafry_D" class="w-full h-full object-cover">
              </div>
              <h3 class="text-2xl font-bold mb-2">Mafry_D</h3>
              <h4 class="text-primary font-semibold">Заместитель лидера</h4>
            </div>
            <!-- Kinlayz -->
            <div class="text-center bg-card border border-primary/20 rounded-2xl p-8">
              <div class="mx-auto w-32 h-32 mb-6 rounded-full overflow-hidden border-3 border-primary/30">
                <img src="https://minecraftpfp.com/PFP/tommyinnit.png" alt="Kinlayz" class="w-full h-full object-cover">
              </div>
              <h3 class="text-2xl font-bold mb-2">Kinlayz</h3>
              <h4 class="text-primary font-semibold">Заместитель лидера</h4>
            </div>
          </div>
        </div>

        <!-- Staff placeholder -->
        <div>
          <h3 class="text-2xl font-bold text-center mb-6">Руководящий состав</h3>
          <p class="text-center text-gray-400 text-lg">В скором времени тут будет информация!</p>
        </div>
      </div>
    </section>

    <!-- News (placeholder only) -->
    <section id="news" class="py-20 bg-secondary/10">
      <div class="container mx-auto px-4">
        <div class="text-center mb-6">
          <h2 class="text-4xl md:text-5xl font-extrabold mb-6">
            <span class="text-primary">Единый</span> новостной портал
          </h2>
          <p class="text-xl text-gray-400 max-w-2xl mx-auto">
            В скором времени появится информация!
          </p>
        </div>

        <!--
          Если понадобится включить новости назад:
          - Обновите автора на "kinlayz" в карточках и/или данных.
          Пример (скрыт):
          <div class="hidden">Автор: kinlayz</div>
        -->
      </div>
    </section>

    <!-- Join -->
    <section id="join" class="py-20 bg-secondary/10">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-4xl md:text-5xl font-extrabold mb-6">
            Хотите вступить в <span class="text-primary">pipeline</span>?
          </h2>
          <p class="text-xl text-gray-400 max-w-2xl mx-auto">
            Станьте частью нашего дружного клана. Подайте заявку уже прямо сейчас!
          </p>
        </div>

        <div class="max-w-4xl mx-auto">
          <div class="grid lg:grid-cols-2 gap-12 items-start">
            <!-- Info -->
            <div class="space-y-6">
              <h3 class="text-2xl font-bold mb-2">Что нужно знать</h3>
              <div>
                <h4 class="text-lg font-semibold text-primary mb-2">Требования</h4>
                <ul class="space-y-2 text-gray-400">
                  <li>Активность в игре</li>
                  <li>Знание правил ZLP.ONL</li>
                </ul>
              </div>
              <div>
                <h4 class="text-lg font-semibold text-primary mb-2">Что вы получите</h4>
                <ul class="space-y-2 text-gray-400">
                  <li>Доступ к территориям клана</li>
                  <li>Участие в клановых мероприятиях</li>
                  <li>Поддержка новичков</li>
                </ul>
              </div>
            </div>

            <!-- CTA -->
            <div>
              <div class="bg-primary/10 border border-primary/30 rounded-2xl p-8 text-center">
                <div class="w-20 h-20 bg-primary rounded-full flex items-center justify-center mx-auto mb-6">
                  <svg class="w-10 h-10 text-white" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                    <path d="M20.317 4.37a19.8 19.8 0 0 0-4.885-1.515a.074.074 0 0 0-.079.037c-.211.375-.445.865-.608 1.25a17.9 17.9 0 0 0-5.487 0c-.164-.393-.406-.874-.618-1.25a.077.077 0 0 0-.079-.037A19.74 19.74 0 0 0 3.677 4.37a.07.07 0 0 0-.032.028C.533 9.046-.319 13.58.099 18.058a.082.082 0 0 0 .03.056c2.053 1.507 4.042 2.423 5.994 3.029a.078.078 0 0 0 .084-.028c.461-.63.873-1.294 1.226-1.993a.076.076 0 0 0-.042-.106a12.3 12.3 0 0 1-1.872-.892a.077.077 0 0 1-.008-.128l.372-.291a.074.074 0 0 1 .078-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01l.373.292a.077.077 0 0 1-.007.128a12.3 12.3 0 0 1-1.873.891a.077.077 0 0 0-.04.107c.36.698.772 1.363 1.225 1.993a.076.076 0 0 0 .084.029c1.96-.607 3.95-1.522 6.002-3.029a.077.077 0 0 0 .032-.055c.5-5.177-.838-9.674-3.549-13.661a.061.061 0 0 0-.031-.029Z"/>
                  </svg>
                </div>
                <h3 class="text-2xl font-bold mb-4">Присоединяйтесь к Discord</h3>
                <p class="text-gray-400 mb-6">
                  Начните свой путь в клане pipeline с подачи заявки в нашем Discord сервере.
                </p>
                <button
                  onclick="window.open('https://discord.gg/9Gp4ZrumSs', '_blank')"
                  class="bg-primary text-white hover:bg-primary/90 w-full btn-minimal px-6 py-3 rounded-md font-medium">
                  Перейти в Discord
                </button>
              </div>
            </div>

          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black border-t border-primary/20 py-8">
      <div class="container mx-auto px-4">
        <p class="text-center text-gray-400">made by Kinlayz</p>
      </div>
    </footer>

  </div>

  <script>
    // Smooth scroll to join
    function scrollToJoin() {
      const el = document.getElementById('join');
      if (el) el.scrollIntoView({ behavior: 'smooth' });
    }

    // Loader
    function showLoader(){
      const loader=document.getElementById('loader');
      const fill=document.getElementById('progressFill');
      if(!loader||!fill) return;
      loader.classList.add('show');
      setTimeout(()=>{ fill.style.width='100%'; }, 100);
      setTimeout(()=>{ loader.classList.remove('show'); fill.style.width='0'; }, 1200);
    }

    // On load
    window.addEventListener('DOMContentLoaded', ()=> {
      showLoader();
    });
  </script>
</body>
</html>

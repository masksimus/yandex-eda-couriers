<!DOCTYPE html>
<html lang="ru">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Стань курьером Яндекс.Еды — Зарабатывай до 80 000 ₽ в месяц</title>
    <meta name="description" content="Работа курьером в Яндекс.Еде — высокий доход, гибкий график, бонусы. Подключись за 5 минут и начни зарабатывать уже сегодня!" />
    <meta name="keywords" content="курьер Яндекс.Еда, работа курьером, заработок курьером, доставка еды, подработка, Яндекс.Еда курьер" />
    <meta name="robots" content="index, follow" />

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          extend: {
            colors: {
              primary: '#FFA500',
              accent: '#FF4500',
            }
          }
        }
      }
    </script>

    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <!-- Framer Motion (для анимаций) -->
    <script src="https://unpkg.com/framer-motion@10.16.4/dist/framer-motion.min.js"></script>

    <style>
      @keyframes float {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-10px); }
      }
      .animate-float {
        animation: float 3s ease-in-out infinite;
      }
      .glow-button {
        box-shadow: 0 0 20px rgba(255, 165, 0, 0.3);
        transition: all 0.3s ease;
      }
      .glow-button:hover {
        transform: translateY(-2px) scale(1.02);
        box-shadow: 0 0 30px rgba(255, 165, 0, 0.5);
      }
    </style>
  </head>
  <body class="min-h-screen bg-gradient-to-br from-white to-gray-50 text-gray-800">

    <!-- Header -->
    <header class="bg-white shadow-sm border-b sticky top-0 z-50 backdrop-blur-md bg-white/90">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
        <div class="flex items-center space-x-2">
          <div class="w-10 h-10 bg-gradient-to-r from-yellow-400 to-orange-500 rounded-lg flex items-center justify-center shadow-md">
            <span class="text-white font-bold text-lg">YE</span>
          </div>
          <span class="text-xl font-bold text-gray-900">Яндекс.Еда</span>
        </div>
        <a href="https://trk.ppdu.ru/click/qV4BiHju?erid=Kra23uVC3&landingId=563" class="glow-button bg-gradient-to-r from-yellow-400 to-orange-500 hover:from-yellow-500 hover:to-orange-600 text-white font-semibold px-6 py-2 rounded-lg shadow-md">Подключиться</a>
      </div>
    </header>

    <!-- Hero -->
    <section class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24 relative">
      <div class="absolute top-10 right-10 w-32 h-32 bg-orange-200 rounded-full opacity-30 blur-3xl"></div>
      <div class="absolute bottom-10 left-10 w-40 h-40 bg-yellow-200 rounded-full opacity-20 blur-3xl"></div>

      <div class="flex flex-col md:flex-row items-center gap-12">
        <div class="flex-1 text-center md:text-left">
          <h1 class="text-3xl md:text-5xl font-extrabold text-gray-900 leading-tight mb-6">
            Зарабатывай до 
            <span class="bg-gradient-to-r from-orange-500 to-red-600 text-transparent bg-clip-text font-extrabold"> 80 000 ₽</span> в месяц
            <br />
            <span class="text-lg md:text-xl font-normal text-gray-600 mt-2 block">как курьер Яндекс.Еды</span>
          </h1>
          <p class="text-lg text-gray-600 mb-10 max-w-xl mx-auto md:mx-0">
            Работай в удобное время, выбирай район доставки и получай выплаты каждый день. 
            Подключись за 5 минут — без опыта и документов!
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
            <a href="https://trk.ppdu.ru/click/qV4BiHju?erid=Kra23uVC3&landingId=563" class="inline-flex items-center justify-center glow-button bg-gradient-to-r from-yellow-400 to-orange-500 text-white font-semibold px-8 py-4 rounded-xl text-lg shadow-lg">
              Начать зарабатывать <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" class="ml-2"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
            </a>
            <a href="#benefits" class="inline-flex items-center justify-center glow-button border-2 border-gray-300 hover:border-orange-400 text-gray-700 font-semibold px-8 py-4 rounded-xl text-lg">
              Узнать больше
            </a>
          </div>
        </div>
        <div class="flex-1 flex justify-center">
          <div class="relative animate-float">
            <img src="https://placehold.co/500x600/FFA500/FFFFFF?text=Курьер+на+самокате" alt="Курьер Яндекс.Еды" class="rounded-2xl shadow-2xl max-w-sm">
            <div class="absolute -bottom-4 -right-4 bg-white p-3 rounded-xl shadow-lg flex items-center space-x-2">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="text-green-500"><path d="M5 13l4 4L19 7"></path></svg>
              <span class="text-sm font-medium text-gray-700">Одобрен!</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Benefits -->
    <section id="benefits" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
      <h2 class="text-3xl font-bold text-center text-gray-900 mb-12">Почему курьеры выбирают нас?</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 text-center">
          <div class="w-14 h-14 bg-gradient-to-r from-orange-400 to-yellow-400 rounded-full flex items-center justify-center mb-4 text-white mx-auto">
            <i data-lucide="wallet" class="lucide-icon"></i>
          </div>
          <h3 class="text-xl font-semibold mb-2 text-gray-900">Высокий доход</h3>
          <p class="text-gray-600">От 80 000 ₽ в месяц. Чем больше заказов — тем больше заработок.</p>
        </div>
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 text-center">
          <div class="w-14 h-14 bg-gradient-to-r from-orange-400 to-yellow-400 rounded-full flex items-center justify-center mb-4 text-white mx-auto">
            <i data-lucide="clock" class="lucide-icon"></i>
          </div>
          <h3 class="text-xl font-semibold mb-2 text-gray-900">Гибкий график</h3>
          <p class="text-gray-600">Работай 2, 5 или 12 часов — выбирай сам, когда и сколько.</p>
        </div>
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 text-center">
          <div class="w-14 h-14 bg-gradient-to-r from-orange-400 to-yellow-400 rounded-full flex items-center justify-center mb-4 text-white mx-auto">
            <i data-lucide="map-pin" class="lucide-icon"></i>
          </div>
          <h3 class="text-xl font-semibold mb-2 text-gray-900">Удобный район</h3>
          <p class="text-gray-600">Выбирай зону доставки: дом, центр или вокзал — как тебе удобно.</p>
        </div>
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 text-center">
          <div class="w-14 h-14 bg-gradient-to-r from-orange-400 to-yellow-400 rounded-full flex items-center justify-center mb-4 text-white mx-auto">
            <i data-lucide="smartphone" class="lucide-icon"></i>
          </div>
          <h3 class="text-xl font-semibold mb-2 text-gray-900">Простое приложение</h3>
          <p class="text-gray-600">Все заказы, маршруты и оплата — в одном приложении.</p>
        </div>
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 text-center">
          <div class="w-14 h-14 bg-gradient-to-r from-orange-400 to-yellow-400 rounded-full flex items-center justify-center mb-4 text-white mx-auto">
            <i data-lucide="shield" class="lucide-icon"></i>
          </div>
          <h3 class="text-xl font-semibold mb-2 text-gray-900">Безопасность</h3>
          <p class="text-gray-600">Страховка, поддержка 24/7 и защита от мошенников.</p>
        </div>
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 text-center">
          <div class="w-14 h-14 bg-gradient-to-r from-orange-400 to-yellow-400 rounded-full flex items-center justify-center mb-4 text-white mx-auto">
            <i data-lucide="star" class="lucide-icon"></i>
          </div>
          <h3 class="text-xl font-semibold mb-2 text-gray-900">Бонусы и премии</h3>
          <p class="text-gray-600">Доплата за плохую погоду, праздники и высокую активность.</p>
        </div>
      </div>
    </section>

    <!-- CTA Final -->
    <section class="bg-gradient-to-r from-orange-500 to-red-500 text-white py-16 text-center">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl font-bold mb-6">Готов начать зарабатывать уже завтра?</h2>
        <p class="text-xl mb-8 opacity-90">Подключись к Яндекс.Еде — получи первую выплату уже через 3 дня!</p>
        <a href="https://trk.ppdu.ru/click/qV4BiHju?erid=Kra23uVC3&landingId=563" class="inline-flex items-center justify-center glow-button bg-white text-orange-600 font-bold px-10 py-4 rounded-xl text-lg shadow-lg">
          Начать сейчас <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" class="ml-2"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        </a>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12 text-center">
      <div class="max-w-6xl mx-auto px-4">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="flex items-center space-x-2 mb-4 md:mb-0">
            <div class="w-8 h-8 bg-gradient-to-r from-yellow-400 to-orange-500 rounded-md flex items-center justify-center">
              <span class="text-white font-bold">YE</span>
            </div>
            <span class="text-lg font-semibold">Яндекс.Еда</span>
          </div>
          <div class="text-sm text-gray-400">
            © 2025 Яндекс.Еда — платформа доставки еды и подработка для курьеров
          </div>
        </div>
      </div>
    </footer>

    <!-- Инициализация иконок -->
    <script>
      document.addEventListener("DOMContentLoaded", () => {
        lucide.createIcons();
      });
    </script>
  </body>
</html>

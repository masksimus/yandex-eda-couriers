# yandex-eda-couriers
main
import { Smartphone, MapPin, Wallet, Clock, Star, Shield, ArrowRight, Check } from 'lucide-react';
import { motion, useAnimation, useInView } from 'framer-motion';
import { useEffect, useRef } from 'react';

// Animated Card Component
const AnimatedCard = ({ children, delay = 0 }) => {
  const controls = useAnimation();
  const ref = useRef(null);
  const inView = useInView({ threshold: 0.1 });

  useEffect(() => {
    if (inView) {
      controls.start('visible');
    }
  }, [controls, inView]);

  return (
    <motion.div
      ref={ref}
      initial="hidden"
      animate={controls}
      variants={{
        visible: { opacity: 1, y: 0, scale: 1 },
        hidden: { opacity: 0, y: 20, scale: 0.95 }
      }}
      transition={{ duration: 0.6, ease: "easeOut", delay }}
    >
      {children}
    </motion.div>
  );
};

// Glow Button
const GlowButton = ({ children, href, variant = "primary" }) => {
  const isPrimary = variant === "primary";
  return (
    <a
      href={href}
      className={`inline-flex items-center space-x-2 px-7 py-3 rounded-xl font-semibold transition-all duration-300 transform hover:-translate-y-1 focus:outline-none focus:ring-4 ${
        isPrimary
          ? 'bg-gradient-to-r from-yellow-400 via-orange-500 to-red-500 text-white shadow-lg hover:shadow-2xl'
          : 'bg-white text-orange-600 shadow-md hover:shadow-lg'
      } hover:scale-105 relative overflow-hidden group`}
    >
      <span className="relative z-10">{children}</span>
      <span className="absolute inset-0 bg-gradient-to-r from-yellow-300 to-orange-400 opacity-0 group-hover:opacity-30 transition-opacity duration-300 rounded-xl"></span>
      <ArrowRight size={18} className="relative z-10" />
    </a>
  );
};

export default function YandexEdaCouriersLanding() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-white to-gray-50 text-gray-800">
      {/* Meta Tags for SEO */}
      <head>
        <title>Стань курьером Яндекс.Еды — Зарабатывай от 80 000 ₽ в месяц | Гибкий график</title>
        <meta name="description" content="Работа курьером в Яндекс.Еде — высокий доход, гибкий график, бонусы и поддержка. Подключайся за 5 минут и начни зарабатывать уже сегодня!" />
        <meta name="keywords" content="курьер Яндекс.Еда, работа курьером, заработок курьером, доставка еды, подработка курьер, Яндекс.Еда курьер" />
        <meta name="robots" content="index, follow" />
      </head>

      {/* Header */}
      <header className="bg-white shadow-sm border-b sticky top-0 z-50 backdrop-blur-md bg-white/90">
        <div className="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
          <div className="flex items-center space-x-2">
            <div className="w-10 h-10 bg-gradient-to-r from-yellow-400 to-orange-500 rounded-lg flex items-center justify-center shadow-md">
              <span className="text-white font-bold text-lg">YE</span>
            </div>
            <span className="text-xl font-bold text-gray-900">Яндекс.Еда</span>
          </div>
          <GlowButton href="https://trk.ppdu.ru/click/qV4BiHju?erid=Kra23uVC3&landingId=563" variant="primary">
            Подключиться
          </GlowButton>
        </div>
      </header>

      {/* Hero Section */}
      <section className="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24 relative overflow-hidden">
        <div className="absolute top-10 right-10 w-32 h-32 bg-orange-200 rounded-full opacity-30 blur-3xl"></div>
        <div className="absolute bottom-10 left-10 w-40 h-40 bg-yellow-200 rounded-full opacity-20 blur-3xl"></div>

        <div className="flex flex-col md:flex-row items-center gap-12">
          <div className="flex-1 text-center md:text-left">
            <AnimatedCard delay={0.2}>
              <h1 className="text-3xl md:text-5xl font-extrabold text-gray-900 leading-tight mb-6">
                Зарабатывай до{' '}
                <span className="bg-gradient-to-r from-orange-500 to-red-600 text-transparent bg-clip-text font-extrabold">
                  80 000 ₽
                </span>{' '}
                в месяц
                <br />
                <span className="text-lg md:text-xl font-normal text-gray-600 mt-2 block">
                  как курьер Яндекс.Еды
                </span>
              </h1>
            </AnimatedCard>

            <AnimatedCard delay={0.4}>
              <p className="text-lg text-gray-600 mb-10 max-w-xl mx-auto md:mx-0">
                Работай в удобное время, выбирай район доставки и получай выплаты каждый день. 
                Подключись за 5 минут — без опыта и документов!
              </p>
            </AnimatedCard>

            <div className="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
              <AnimatedCard delay={0.6}>
                <GlowButton href="https://trk.ppdu.ru/click/qV4BiHju?erid=Kra23uVC3&landingId=563" variant="primary">
                  Начать зарабатывать
                </GlowButton>
              </AnimatedCard>
              <AnimatedCard delay={0.8}>
                <GlowButton href="#benefits" variant="secondary">
                  Узнать больше
                </GlowButton>
              </AnimatedCard>
            </div>
          </div>

          <div className="flex-1 flex justify-center">
            <AnimatedCard delay={0.5}>
              <div className="relative">
                <img
                  src="https://placehold.co/500x600/FFA500/FFFFFF?text=Курьер+на+самокате"
                  alt="Курьер Яндекс.Еды на самокате"
                  className="rounded-2xl shadow-2xl w-full max-w-sm md:max-w-md"
                />
                <div className="absolute -bottom-4 -right-4 bg-white p-3 rounded-xl shadow-lg flex items-center space-x-2">
                  <Check size={18} className="text-green-500" />
                  <span className="text-sm font-medium text-gray-700">Одобрен!</span>
                </div>
              </div>
            </AnimatedCard>
          </div>
        </div>
      </section>

      {/* Benefits Section */}
      <section id="benefits" className="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
        <AnimatedCard>
          <h2 className="text-3xl font-bold text-center text-gray-900 mb-12">Почему курьеры выбирают нас?</h2>
        </AnimatedCard>
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          {[
            { icon: Wallet, title: "Высокий доход", desc: "От 80 000 ₽ в месяц. Чем больше заказов — тем больше заработок." },
            { icon: Clock, title: "Гибкий график", desc: "Работай 2, 5 или 12 часов — выбирай сам, когда и сколько." },
            { icon: MapPin, title: "Удобный район", desc: "Выбирай зону доставки: дом, центр или вокзал — как тебе удобно." },
            { icon: Smartphone, title: "Простое приложение", desc: "Все заказы, маршруты и оплата — в одном приложении." },
            { icon: Shield, title: "Безопасность", desc: "Страховка, поддержка 24/7 и защита от мошенников." },
            { icon: Star, title: "Бонусы и премии", desc: "Доплата за плохую погоду, праздники и высокую активность." },
          ].map((item, index) => (
            <AnimatedCard key={index} delay={0.2 + index * 0.1}>
              <div className="bg-white p-6 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 text-center group">
                <div className="w-14 h-14 bg-gradient-to-r from-orange-400 to-yellow-400 rounded-full flex items-center justify-center mb-4 text-white mx-auto group-hover:scale-110 transition-transform">
                  <item.icon size={28} />
                </div>
                <h3 className="text-xl font-semibold mb-2 text-gray-900 group-hover:text-orange-600">{item.title}</h3>
                <p className="text-gray-600">{item.desc}</p>
              </div>
            </AnimatedCard>
          ))}
        </div>
      </section>

      {/* How It Works */}
      <section className="bg-white py-16 relative overflow-hidden">
        <div className="absolute left-10 top-10 w-20 h-20 bg-yellow-100 rounded-full opacity-40 blur-xl"></div>
        <div className="absolute right-10 bottom-10 w-24 h-24 bg-orange-100 rounded-full opacity-50 blur-xl"></div>

        <div className="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
          <AnimatedCard>
            <h2 className="text-3xl font-bold text-gray-900 mb-12">Как начать работать?</h2>
          </AnimatedCard>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {[
              { step: "1", text: "Оставь заявку на сайте" },
              { step: "2", text: "Загрузи документы (паспорт, права)" },
              { step: "3", text: "Получи доступ к приложению и начни доставлять" },
            ].map((item, index) => (
              <AnimatedCard key={index} delay={0.3 + index * 0.2}>
                <div className="flex flex-col items-center">
                  <div className="w-12 h-12 bg-orange-500 text-white rounded-full flex items-center justify-center text-lg font-bold mb-4 shadow-lg">
                    {item.step}
                  </div>
                  <p className="text-gray-700 font-medium">{item.text}</p>
                </div>
              </AnimatedCard>
            ))}
          </div>
          <AnimatedCard delay={1}>
            <div className="mt-12">
              <GlowButton href="https://trk.ppdu.ru/click/qV4BiHju?erid=Kra23uVC3&landingId=563">
                Подать заявку
              </GlowButton>
            </div>
          </AnimatedCard>
        </div>
      </section>

      {/* Testimonials */}
      <section className="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
        <AnimatedCard>
          <h2 className="text-3xl font-bold text-center text-gray-900 mb-12">Отзывы курьеров</h2>
        </AnimatedCard>
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          {[
            { name: "Алексей, Москва", role: "Курьер 8 месяцев", text: "Зарабатываю стабильно по 2 500 в день. График сам выбираю — удобно совмещать с учёбой.", img: "https://placehold.co/100x100/FFB6C1/000000?text=А" },
            { name: "Дарья, Санкт-Петербург", role: "Курьер 1.5 года", text: "Лучшая подработка! Выплаты каждый день, бонусы за дождь — реально помогает.", img: "https://placehold.co/100x100/87CEEB/000000?text=Д" },
            { name: "Руслан, Казань", role: "Курьер 3 месяца", text: "Подключился за 2 дня. Уже в первый месяц вышел на 70 тысяч. Рекомендую!", img: "https://placehold.co/100x100/98FB98/000000?text=Р" },
          ].map((review, index) => (
            <AnimatedCard key={index} delay={0.2 + index * 0.2}>
              <div className="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div className="flex items-center mb-4">
                  <img src={review.img} alt={review.name} className="w-12 h-12 rounded-full mr-4" />
                  <div>
                    <p className="font-semibold text-gray-900">{review.name}</p>
                    <p className="text-sm text-gray-500">{review.role}</p>
                  </div>
                </div>
                <p className="text-gray-600 italic">"{review.text}"</p>
              </div>
            </AnimatedCard>
          ))}
        </div>
      </section>

      {/* CTA Final */}
      <section className="bg-gradient-to-r from-orange-500 to-red-500 text-white py-16 relative overflow-hidden">
        <div className="absolute inset-0 bg-black opacity-10"></div>
        <div className="max-w-4xl mx-auto text-center px-4 sm:px-6 lg:px-8 relative z-10">
          <AnimatedCard>
            <h2 className="text-3xl md:text-4xl font-bold mb-6">Готов начать зарабатывать уже завтра?</h2>
          </AnimatedCard>
          <AnimatedCard delay={0.2}>
            <p className="text-xl mb-8 opacity-90">Подключись к Яндекс.Еде — получи первую выплату уже через 3 дня!</p>
          </AnimatedCard>
          <AnimatedCard delay={0.4}>
            <GlowButton href="https://trk.ppdu.ru/click/qV4BiHju?erid=Kra23uVC3&landingId=563" variant="secondary">
              Начать сейчас
            </GlowButton>
          </AnimatedCard>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white py-12">
        <div className="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex flex-col md:flex-row justify-between items-center">
            <div className="flex items-center space-x-2 mb-4 md:mb-0">
              <div className="w-8 h-8 bg-gradient-to-r from-yellow-400 to-orange-500 rounded-md flex items-center justify-center shadow-md">
                <span className="text-white font-bold">YE</span>
              </div>
              <span className="text-lg font-semibold">Яндекс.Еда</span>
            </div>
            <div className="text-sm text-gray-400 text-center md:text-right">
              © 2025 Яндекс.Еда — платформа доставки еды и подработка для курьеров
            </div>
          </div>
        </div>
      </footer>
    </div>
  );
}

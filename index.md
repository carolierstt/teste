<!DOCTYPE html>
<html lang="pt-br" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Consultoria de Currículo - Destrave sua Carreira</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Animate On Scroll Library (AOS) -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
    
    <!-- Alpine.js for interactions -->
    <script src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Space Grotesk', 'sans-serif'],
                    },
                    colors: {
                        'brand-blue': '#00BFFF',
                        'brand-purple': '#8A2BE2',
                        'dark-bg': '#0D0C1D',
                        'dark-card': '#161A30',
                    },
                    animation: {
                        'gradient-x': 'gradient-x 15s ease infinite',
                        'text-reveal': 'text-reveal 1.5s cubic-bezier(0.77, 0, 0.175, 1) 0.5s forwards',
                    },
                    keyframes: {
                        'gradient-x': {
                            '0%, 100%': { 'background-position': '0% 50%' },
                            '50%': { 'background-position': '100% 50%' },
                        },
                        'text-reveal': {
                            '0%': {
                                transform: 'translate(0, 100%)',
                            },
                            '100%': {
                                transform: 'translate(0, 0)',
                            },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        .gradient-text {
            background: linear-gradient(90deg, #00BFFF, #8A2BE2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-fill-color: transparent;
        }
        
        .hero-bg {
            background-color: #0D0C1D;
            background-image: radial-gradient(circle at 1px 1px, rgba(255,255,255,0.05) 1px, transparent 0);
            background-size: 40px 40px;
        }

        .cta-button-glow {
            background: linear-gradient(90deg, #00BFFF, #8A2BE2);
            background-size: 200% 200%;
            animation: gradient-x 5s ease infinite;
            transition: all 0.3s ease;
            box-shadow: 0 0 20px rgba(0, 191, 255, 0.5), 0 0 30px rgba(138, 43, 226, 0.3);
        }
        .cta-button-glow:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 0 30px rgba(0, 191, 255, 0.7), 0 0 40px rgba(138, 43, 226, 0.5);
        }
        
        .clip-reveal {
            clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
            transition: clip-path 0.8s cubic-bezier(0.19, 1, 0.22, 1);
        }
        
        [data-aos="reveal-up"].aos-animate .clip-reveal {
            clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
        }
        
    </style>
</head>
<body class="bg-dark-bg font-sans text-gray-300">

    <!-- Header com Efeito Glassmorphism -->
    <header x-data="{ scrolled: false }" @scroll.window="scrolled = (window.pageYOffset > 50)" class="fixed top-0 left-0 right-0 z-50 transition-all duration-300" :class="{ 'bg-dark-bg/70 backdrop-blur-lg shadow-lg shadow-brand-blue/10': scrolled, 'bg-transparent': !scrolled }">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="font-display font-bold text-2xl text-white">CV<span class="gradient-text">Boost</span></a>
            <nav class="hidden md:flex items-center space-x-8">
                <a href="#problem" class="text-gray-300 hover:text-brand-blue transition">A Realidade</a>
                <a href="#solution" class="text-gray-300 hover:text-brand-blue transition">A Virada</a>
                <a href="#pricing" class="text-gray-300 hover:text-brand-blue transition">Sua Decisão</a>
                <a href="#faq" class="text-gray-300 hover:text-brand-blue transition">Dúvidas</a>
            </nav>
            <a href="#pricing" class="hidden md:block bg-brand-blue hover:bg-opacity-80 text-white font-bold py-2 px-6 rounded-lg transition">Destravar Carreira</a>
        </div>
    </header>

    <main>
        <!-- Seção Hero -->
        <section class="hero-bg pt-32 pb-20 md:pt-48 md:pb-32">
            <div class="container mx-auto px-6 text-center">
                <div class="font-display font-bold text-4xl md:text-6xl lg:text-7xl text-white leading-tight" data-aos="reveal-up">
                    <div class="relative inline-block overflow-hidden">
                       <span class="clip-reveal">A entrevista que você</span>
                    </div>
                    <div class="relative inline-block overflow-hidden">
                       <span class="gradient-text clip-reveal">merece, finalmente.</span>
                    </div>
                </div>
                
                <p class="mt-6 text-lg md:text-xl max-w-3xl mx-auto text-gray-400" data-aos="fade-up" data-aos-delay="300">Chega de se sentir invisível. Chega de ansiedade a cada e-mail enviado. É hora de transformar seu potencial em uma proposta irrecusável e fazer os recrutadores virem até você.</p>
                <div data-aos="fade-up" data-aos-delay="500">
                    <a href="#pricing" class="cta-button-glow mt-10 inline-block text-white font-bold rounded-full py-4 px-10 uppercase text-lg">Destrave minha carreira agora</a>
                </div>
            </div>
        </section>

        <!-- Seção: O Problema (A Realidade) -->
        <section id="problem" class="py-16 md:py-24">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="font-display text-3xl md:text-4xl font-bold text-white" data-aos="fade-up">O silêncio depois do "Enviar". Você conhece.</h2>
                    <p class="mt-4 text-gray-400 max-w-2xl mx-auto" data-aos="fade-up" data-aos-delay="100">Aquela angústia de atualizar a caixa de entrada, a dúvida sobre o seu próprio valor, a frustração de saber que você é perfeito para a vaga. Você não está sozinho nisso.</p>
                </div>
                <div class="grid md:grid-cols-3 gap-8">
                    <!-- Card 1 -->
                    <div class="bg-dark-card p-8 rounded-2xl border border-gray-700/50 shadow-lg shadow-brand-purple/10" data-aos="fade-up" data-aos-delay="200">
                        <div class="text-4xl mb-4">🧱</div>
                        <h3 class="font-display font-bold text-xl text-white mb-2">A Barreira dos Robôs</h3>
                        <p class="text-gray-400">Seu talento e experiência são barrados por um software impessoal (ATS) antes mesmo que uma pessoa possa te conhecer. É como gritar em uma sala vazia.</p>
                    </div>
                    <!-- Card 2 -->
                    <div class="bg-dark-card p-8 rounded-2xl border border-gray-700/50 shadow-lg shadow-brand-purple/10" data-aos="fade-up" data-aos-delay="300">
                        <div class="text-4xl mb-4">👤</div>
                        <h3 class="font-display font-bold text-xl text-white mb-2">Apenas Mais Um na Pilha</h3>
                        <p class="text-gray-400">Sem uma narrativa poderosa, seu currículo se mistura a centenas de outros. Suas conquistas se perdem, e você se torna apenas mais um número.</p>
                    </div>
                    <!-- Card 3 -->
                    <div class="bg-dark-card p-8 rounded-2xl border border-gray-700/50 shadow-lg shadow-brand-purple/10" data-aos="fade-up" data-aos-delay="400">
                        <div class="text-4xl mb-4">⏳</div>
                        <h3 class="font-display font-bold text-xl text-white mb-2">O Custo da Espera</h3>
                        <p class="text-gray-400">Cada "não", cada silêncio, não é apenas uma vaga perdida. É a sua confiança diminuindo, oportunidades passando e a carreira estagnada.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Seção: A Solução (A Virada) -->
        <section id="solution" class="py-16 md:py-24 bg-dark-card/50">
            <div class="container mx-auto px-6">
                <div class="flex flex-col md:flex-row items-center gap-12">
                    <div class="w-full md:w-1/2" data-aos="zoom-in-right">
                        <img src="https://placehold.co/600x450/161A30/00BFFF?text=Sua+Virada+de+Jogo" alt="Imagem representando análise de currículo" class="rounded-2xl shadow-2xl shadow-brand-blue/20 w-full">
                    </div>
                    <div class="w-full md:w-1/2" data-aos="fade-left">
                        <h2 class="font-display text-3xl md:text-4xl font-bold text-white mb-4">É hora da virada. Apresentando o CV<span class="gradient-text">Boost</span>.</h2>
                        <p class="text-gray-300 mb-6 text-lg">Nós somos a ponte entre o seu talento e a oportunidade que você busca. Transformamos frustração em confiança, e silêncio em convites para entrevistas.</p>
                        <ul class="space-y-4 text-gray-300">
                            <li class="flex items-start"><span class="text-brand-blue mr-3 mt-1">✓</span> <strong>Decodificador de Robôs (ATS):</strong> Nós falamos a língua das máquinas para que os humanos possam ouvir a sua voz e conhecer seu potencial.</li>
                            <li class="flex items-start"><span class="text-brand-blue mr-3 mt-1">✓</span> <strong>Sua Carreira Como Uma História de Sucesso:</strong> Deixamos de lado a lista de tarefas e transformamos suas experiências em conquistas que brilham aos olhos dos recrutadores.</li>
                            <li class="flex items-start"><span class="text-brand-blue mr-3 mt-1">✓</span> <strong>Design que Comunica Confiança:</strong> Uma primeira impressão visual que reflete a qualidade e o calibre do profissional que você é.</li>
                             <li class="flex items-start"><span class="text-brand-blue mr-3 mt-1">✓</span> <strong>O Fator Humano e Estratégico:</strong> Não é sobre um papel, é sobre você. Em nossa sessão, alinhamos sua essência com a sua ambição para um resultado autêntico e poderoso.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- NOVA SEÇÃO: Para Quem é -->
        <section id="for-who" class="py-16 md:py-24">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="font-display text-3xl md:text-4xl font-bold text-white" data-aos="fade-up">Se você se vê aqui, nós podemos ajudar.</h2>
                </div>
                <div class="grid md:grid-cols-3 gap-8 text-center">
                    <div data-aos="fade-up" data-aos-delay="100">
                        <div class="bg-dark-card p-8 rounded-2xl h-full border border-gray-700/30">
                            <h3 class="font-display text-xl font-bold text-brand-blue mb-2">Profissional Experiente</h3>
                            <p class="text-gray-400">Buscando o próximo grande salto na carreira, mas sente que seu currículo não reflete mais seu nível de senioridade e impacto.</p>
                        </div>
                    </div>
                    <div data-aos="fade-up" data-aos-delay="200">
                        <div class="bg-dark-card p-8 rounded-2xl h-full border border-gray-700/30">
                            <h3 class="font-display text-xl font-bold text-brand-blue mb-2">Transição de Carreira</h3>
                            <p class="text-gray-400">Precisando recontar sua história profissional de forma coesa e convincente para uma nova área de atuação.</p>
                        </div>
                    </div>
                    <div data-aos="fade-up" data-aos-delay="300">
                        <div class="bg-dark-card p-8 rounded-2xl h-full border border-gray-700/30">
                            <h3 class="font-display text-xl font-bold text-brand-blue mb-2">Recém-Formado</h3>
                            <p class="text-gray-400">Ansioso para entrar no mercado com o pé direito, mas não sabe como destacar seu potencial com pouca experiência.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Seção: Preços (Sua Decisão) -->
        <section id="pricing" class="py-16 md:py-24 bg-dark-card/50">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="font-display text-3xl md:text-4xl font-bold text-white" data-aos="fade-up">Chega de esperar. A decisão é sua.</h2>
                    <p class="mt-4 text-gray-400 max-w-2xl mx-auto" data-aos="fade-up" data-aos-delay="100">Quanto vale receber o "sim" para a vaga dos seus sonhos? O investimento em você é sempre o que traz o maior retorno.</p>
                </div>
                <div class="flex justify-center">
                    <div class="bg-dark-card w-full max-w-md rounded-2xl p-8 border-2 border-brand-blue shadow-2xl shadow-brand-blue/20 transform hover:scale-105 transition-transform duration-300" data-aos="zoom-in-up">
                        <h3 class="font-display text-2xl font-bold text-center text-white">Consultoria Completa CV<span class="gradient-text">Boost</span></h3>
                        <p class="text-center text-gray-400 mt-2">O plano definitivo para transformar sua carreira.</p>
                        <div class="text-center my-8">
                            <span class="font-display text-6xl font-bold text-white">R$247</span>
                            <span class="text-gray-500">pagamento único</span>
                        </div>
                        <ul class="space-y-4 text-gray-300 mb-8">
                            <li class="flex items-center"><span class="text-brand-blue mr-3">✓</span> Análise completa do CV atual</li>
                            <li class="flex items-center"><span class="text-brand-blue mr-3">✓</span> Otimização para palavras-chave e ATS</li>
                            <li class="flex items-center"><span class="text-brand-blue mr-3">✓</span> Redação e reestruturação de conteúdo</li>
                            <li class="flex items-center"><span class="text-brand-blue mr-3">✓</span> Design moderno e profissional (2 templates)</li>
                            <li class="flex items-center"><span class="text-brand-blue mr-3">✓</span> Sessão estratégica de 30 minutos</li>
                            <li class="flex items-center"><span class="text-brand-blue mr-3">✓</span> Bônus: Guia para LinkedIn Campeão</li>
                        </ul>
                        <a href="#" class="cta-button-glow w-full block text-center text-white font-bold rounded-full py-4 px-10 uppercase text-lg">Quero minha vaga dos sonhos</a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Seção: FAQ -->
        <section id="faq" class="py-16 md:py-24">
            <div class="container mx-auto px-6 max-w-3xl">
                <h2 class="font-display text-3xl md:text-4xl font-bold text-center text-white mb-12" data-aos="fade-up">Suas últimas dúvidas antes da transformação.</h2>
                <div class="space-y-4">
                    <div x-data="{ open: true }" class="bg-dark-card rounded-lg border border-gray-700/50" data-aos="fade-up" data-aos-delay="100">
                        <button @click="open = !open" class="w-full flex justify-between items-center text-left p-6">
                            <span class="font-display font-semibold text-lg text-white">Em quanto tempo verei a transformação?</span>
                            <span class="text-brand-blue text-2xl transform transition-transform" :class="{ 'rotate-45': open }">+</span>
                        </button>
                        <div x-show="open" x-collapse class="px-6 pb-6 text-gray-400">
                            <p>Após a confirmação do pagamento e o envio de suas informações, o prazo é de 5 dias úteis para a entrega da primeira versão do seu novo currículo. A sessão estratégica será agendada nesse período para acelerar seus resultados.</p>
                        </div>
                    </div>
                    <div x-data="{ open: false }" class="bg-dark-card rounded-lg border border-gray-700/50" data-aos="fade-up" data-aos-delay="200">
                        <button @click="open = !open" class="w-full flex justify-between items-center text-left p-6">
                            <span class="font-display font-semibold text-lg text-white">E se não funcionar para mim?</span>
                            <span class="text-brand-blue text-2xl transform transition-transform" :class="{ 'rotate-45': open }">+</span>
                        </button>
                        <div x-show="open" x-collapse class="px-6 pb-6 text-gray-400">
                            <p>Nosso sucesso depende do seu. Por isso, oferecemos uma garantia de satisfação. Se, após o processo e os ajustes, você não sentir a confiança e o impacto que prometemos, conversaremos para encontrar a melhor solução. O risco é todo nosso.</p>
                        </div>
                    </div>
                     <div x-data="{ open: false }" class="bg-dark-card rounded-lg border border-gray-700/50" data-aos="fade-up" data-aos-delay="300">
                        <button @click="open = !open" class="w-full flex justify-between items-center text-left p-6">
                            <span class="font-display font-semibold text-lg text-white">Como funciona a sessão estratégica?</span>
                            <span class="text-brand-blue text-2xl transform transition-transform" :class="{ 'rotate-45': open }">+</span>
                        </button>
                        <div x-show="open" x-collapse class="px-6 pb-6 text-gray-400">
                            <p>É uma chamada de vídeo de 30 minutos com um de nossos especialistas. Usaremos esse tempo para entender profundamente suas metas, tirar dúvidas e coletar as jóias da sua carreira para garantir que seu currículo seja tão único quanto você.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="hero-bg py-12">
        <div class="container mx-auto px-6 text-center text-gray-400">
            <p>&copy; 2024 CVBoost. Todos os direitos reservados.</p>
            <p class="text-sm mt-2">Sua próxima grande oportunidade está a um currículo de distância.</p>
        </div>
    </footer>

    <!-- Scripts no final do body para melhor performance -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        AOS.init({
            duration: 800,
            once: true,
        });
    </script>
</body>
</html>

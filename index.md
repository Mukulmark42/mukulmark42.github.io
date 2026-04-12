<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CardVault • Never Miss a Payment</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;family=Space+Grotesk:wght@500;600&amp;display=swap');
        
        :root {
            --primary: 234 179 8;
        }
        
        .tail-container {
            font-family: 'Inter', system_ui, sans-serif;
        }
        
        .logo-font {
            font-family: 'Space Grotesk', sans-serif;
        }

        .hero-bg {
            background: linear-gradient(135deg, #0f172a 0%, #1e2937 100%);
        }

        .card-gradient {
            background: linear-gradient(135deg, #1e2937, #334155);
        }

        .nav-link {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .nav-link:hover {
            color: rgb(234 179 8);
            transform: translateY(-2px);
        }

        .feature-card {
            transition: all 0.4s cubic-bezier(0.4, 0.0, 0.2, 1);
        }
        
        .feature-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 25px 50px -12px rgb(0 0 0);
        }

        .bill-card {
            transition: all 0.5s cubic-bezier(0.4, 0.0, 0.2, 1);
        }
        
        .bill-card:hover {
            transform: scale(1.05) rotate(2deg);
        }

        .scan-line {
            animation: scan 4s linear infinite;
        }

        @keyframes scan {
            0% { transform: translateY(-100%); }
            100% { transform: translateY(400%); }
        }

        .hero-glow {
            animation: pulse-glow 3s ease-in-out infinite;
        }

        @keyframes pulse-glow {
            0%, 100% { opacity: 0.6; }
            50% { opacity: 1; }
        }

        .credit-card {
            background: linear-gradient(135deg, #1e3a8a, #3b82f6);
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.3),
                        0 0 0 1px rgb(234 179 8 / 0.2);
        }
    </style>
</head>
<body class="tail-container bg-slate-950 text-slate-200">
    <!-- NAVBAR -->
    <nav class="bg-slate-950 border-b border-slate-800 fixed w-full z-50">
        <div class="max-w-screen-2xl mx-auto">
            <div class="px-8 py-5 flex items-center justify-between">
                <!-- Logo -->
                <div class="flex items-center gap-x-3">
                    <div class="w-9 h-9 bg-yellow-400 rounded-2xl flex items-center justify-center shadow-inner">
                        <i class="fa-solid fa-vault text-slate-950 text-2xl"></i>
                    </div>
                    <div>
                        <span class="logo-font text-3xl font-semibold tracking-tighter text-white">CardVault</span>
                    </div>
                </div>

                <!-- Desktop Menu -->
                <div class="hidden md:flex items-center gap-x-8 text-sm font-medium">
                    <a href="#features" onclick="smoothScrollTo('features')" class="nav-link text-slate-300 hover:text-yellow-300">Features</a>
                    <a href="#how" onclick="smoothScrollTo('how')" class="nav-link text-slate-300 hover:text-yellow-300">How it Works</a>
                    <a href="#security" onclick="smoothScrollTo('security')" class="nav-link text-slate-300 hover:text-yellow-300">Security</a>
                    <a href="#demo" onclick="smoothScrollTo('demo')" class="nav-link text-slate-300 hover:text-yellow-300">Demo</a>
                </div>

                <div class="hidden md:flex items-center gap-x-4">
                    <a href="https://mukulmark42.github.io/cardvault-privacy" 
                       target="_blank"
                       class="px-5 py-2 text-xs font-medium tracking-widest border border-slate-700 hover:border-slate-400 rounded-3xl transition-colors">
                        PRIVACY
                    </a>
                    <a href="https://mukulmark42.github.io/Terms-of-Service" 
                       target="_blank"
                       class="px-5 py-2 text-xs font-medium tracking-widest border border-slate-700 hover:border-slate-400 rounded-3xl transition-colors">
                        TERMS
                    </a>
                    <button onclick="showLoginModal()"
                            class="px-6 py-2.5 text-sm font-semibold text-white bg-slate-800 hover:bg-slate-700 rounded-3xl transition-all active:scale-95">
                        Sign in
                    </button>
                    <button onclick="showGetStartedModal()"
                            class="px-6 py-2.5 text-sm font-semibold bg-yellow-400 hover:bg-amber-300 text-slate-950 rounded-3xl transition-all active:scale-95 flex items-center gap-x-2">
                        <span>Get started</span>
                        <i class="fa-solid fa-arrow-right text-xs"></i>
                    </button>
                </div>

                <!-- Mobile Hamburger -->
                <button id="mobile-menu-button"
                        class="md:hidden w-10 h-10 flex items-center justify-center text-2xl text-slate-200">
                    <i class="fa-solid fa-bars"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-slate-900 border-t border-slate-800 py-4">
            <div class="px-6 flex flex-col gap-y-6 text-lg">
                <a href="#features" onclick="toggleMobileMenu()" class="font-medium">Features</a>
                <a href="#how" onclick="toggleMobileMenu()" class="font-medium">How it Works</a>
                <a href="#security" onclick="toggleMobileMenu()" class="font-medium">Security</a>
                <a href="#demo" onclick="toggleMobileMenu()" class="font-medium">Live Demo</a>
                
                <div class="pt-6 border-t border-slate-700 flex flex-col gap-y-3">
                    <a href="https://mukulmark42.github.io/cardvault-privacy" 
                       target="_blank"
                       class="flex items-center gap-x-3 text-slate-400">
                        <i class="fa-solid fa-shield-halved w-4"></i>
                        <span class="text-sm">Privacy Policy</span>
                    </a>
                    <a href="https://mukulmark42.github.io/Terms-of-Service" 
                       target="_blank"
                       class="flex items-center gap-x-3 text-slate-400">
                        <i class="fa-solid fa-file-contract w-4"></i>
                        <span class="text-sm">Terms of Service</span>
                    </a>
                </div>
                
                <div class="flex flex-col gap-y-3 pt-4">
                    <button onclick="toggleMobileMenu();showLoginModal()" 
                            class="py-4 bg-slate-800 hover:bg-slate-700 rounded-3xl text-white font-medium">
                        Sign in
                    </button>
                    <button onclick="toggleMobileMenu();showGetStartedModal()" 
                            class="py-4 bg-yellow-400 text-slate-950 font-semibold rounded-3xl">
                        Start protecting your cards
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- HERO -->
    <header class="hero-bg pt-20 min-h-screen flex items-center relative overflow-hidden">
        <!-- Background elements -->
        <div class="absolute top-0 right-0 w-96 h-96 bg-yellow-300/10 rounded-full blur-3xl -translate-y-1/3 translate-x-1/3 hero-glow"></div>
        <div class="absolute bottom-0 left-20 w-80 h-80 bg-cyan-400/10 rounded-full blur-3xl translate-y-1/3 hero-glow" style="animation-delay: 1500ms"></div>
        
        <div class="max-w-screen-2xl mx-auto px-6 pt-12 md:pt-20 grid md:grid-cols-12 gap-12 items-center">
            <!-- Left content -->
            <div class="md:col-span-7 z-10">
                <div class="inline-flex items-center gap-x-2 bg-white/10 backdrop-blur-md px-5 h-8 rounded-3xl text-xs font-medium tracking-[0.125em] mb-6 border border-white/20">
                    <div class="w-2 h-2 bg-emerald-400 rounded-full animate-pulse"></div>
                    NOW IN PUBLIC BETA
                </div>
                
                <h1 class="text-6xl md:text-7xl font-semibold tracking-tighter leading-none logo-font text-white mb-4">
                    NEVER MISS<br>A CREDIT CARD<br>PAYMENT
                </h1>
                
                <p class="max-w-lg text-xl text-slate-400 mb-10">
                    CardVault scans your emails, detects bills automatically, 
                    and sends smart reminders so you stay on top of your finances.
                </p>
                
                <div class="flex items-center gap-x-4">
                    <button onclick="showGetStartedModal()" 
                            class="flex-1 md:flex-none h-14 px-8 bg-yellow-400 hover:bg-amber-300 transition-all text-slate-950 rounded-3xl font-semibold flex items-center justify-center gap-x-3 shadow-xl shadow-yellow-500/30">
                        <i class="fa-solid fa-envelope text-lg"></i>
                        <span>Connect email securely</span>
                    </button>
                    
                    <button onclick="watchDemo()" 
                            class="flex-1 md:flex-none h-14 px-8 border border-white/30 hover:border-white/60 rounded-3xl font-medium flex items-center justify-center gap-x-2 transition-colors">
                        <i class="fa-solid fa-play text-yellow-300"></i>
                        <span class="hidden sm:inline">Watch 45s demo</span>
                    </button>
                </div>
                
                <div class="mt-12 flex items-center gap-x-8 text-xs">
                    <div class="flex items-center">
                        <div class="flex -space-x-4">
                            <div class="w-6 h-6 bg-slate-700 border-2 border-slate-900 rounded-2xl flex items-center justify-center text-[10px]">🇮🇳</div>
                            <div class="w-6 h-6 bg-blue-600 border-2 border-slate-900 rounded-2xl flex items-center justify-center text-[10px]">💳</div>
                        </div>
                    </div>
                    <div class="text-slate-400 text-sm">
                        Trusted by <span class="text-white font-medium">2,847</span> cardholders
                    </div>
                    <div class="h-3 w-px bg-slate-700"></div>
                    <div onclick="window.location.href='#demo'" 
                         class="flex items-center gap-x-1.5 text-emerald-400 text-xs cursor-pointer hover:text-emerald-300">
                        <i class="fa-solid fa-circle-check"></i>
                        <span class="uppercase tracking-widest font-medium">Live sync active</span>
                    </div>
                </div>
                
                <!-- Trust logos -->
                <div class="mt-16 flex items-center gap-x-8 opacity-40">
                    <i class="fa-brands fa-google text-3xl"></i>
                    <i class="fa-solid fa-gem text-3xl"></i>
                    <div class="text-xs font-mono tracking-widest">GMAIL</div>
                    <div class="text-xs font-mono tracking-widest">FIREBASE</div>
                </div>
            </div>
            
            <!-- Right visual -->
            <div class="md:col-span-5 relative">
                <div class="relative mx-auto max-w-xs md:max-w-none">
                    <!-- Phone mock -->
                    <div class="bg-slate-900 border-8 border-slate-700 rounded-[3rem] p-3 shadow-2xl mx-auto w-72 overflow-hidden">
                        <!-- Phone header -->
                        <div class="h-6 bg-slate-950 rounded-t-3xl flex items-center px-4 gap-2">
                            <div class="flex-1 h-2 bg-slate-700 rounded"></div>
                        </div>
                        
                        <!-- App header -->
                        <div class="bg-gradient-to-r from-slate-800 to-slate-700 h-11 flex items-center px-4 text-xs font-medium">
                            <div class="flex items-center gap-x-2 text-white">
                                <i class="fa-solid fa-vault"></i>
                                <span class="logo-font tracking-tighter">CardVault</span>
                            </div>
                            <div class="flex-1"></div>
                            <div class="bg-emerald-400 text-[10px] text-slate-950 px-3 rounded-3xl h-5 flex items-center font-bold">3 cards</div>
                        </div>
                        
                        <!-- Fake app content -->
                        <div class="bg-slate-950 h-96 p-4 space-y-6 overflow-hidden relative">
                            <!-- Bill cards inside phone -->
                            <div onclick="fakeBillClick(this)" 
                                 class="bill-card bg-slate-800 rounded-3xl p-4 cursor-pointer">
                                <div class="flex justify-between items-start">
                                    <div>
                                        <div class="flex items-center gap-x-2">
                                            <div class="w-6 h-4 bg-blue-500 rounded"></div>
                                            <span class="text-xs text-slate-400">HDFC Bank</span>
                                        </div>
                                        <div class="text-2xl font-semibold text-white mt-1">₹14,750</div>
                                        <div class="text-xs text-amber-300 flex items-center gap-x-1 mt-4">
                                            <i class="fa-solid fa-clock"></i>
                                            <span>Due in 3 days</span>
                                        </div>
                                    </div>
                                    <div class="text-right">
                                        <div class="px-4 py-1 text-[10px] bg-slate-700 text-slate-400 rounded-3xl">VISA</div>
                                        <div class="mt-8 text-emerald-400 text-xs font-medium">PAID</div>
                                    </div>
                                </div>
                            </div>
                            
                            <!-- Second card -->
                            <div onclick="fakeBillClick(this)" 
                                 class="bill-card bg-slate-800 rounded-3xl p-4 cursor-pointer opacity-80">
                                <div class="flex justify-between">
                                    <div>
                                        <div class="text-xs text-slate-400">AXIS Bank •••••4242</div>
                                        <div class="font-medium text-white">₹8,299 due</div>
                                    </div>
                                    <div class="text-rose-400 text-xs pt-1">
                                        <i class="fa-solid fa-bell"></i>
                                    </div>
                                </div>
                            </div>
                            
                            <!-- Status bar -->
                            <div class="absolute bottom-6 left-6 right-6 bg-slate-900 border border-slate-700 rounded-3xl p-3 text-center text-xs flex items-center justify-center gap-x-2">
                                <div class="w-3 h-3 bg-yellow-400 rounded-full animate-ping"></div>
                                <span class="font-medium text-slate-300">All emails synced • 2m ago</span>
                            </div>
                            
                            <!-- Scanning animation overlay -->
                            <div id="scan-overlay" 
                                 onclick="this.style.display='none'"
                                 class="absolute inset-0 bg-black/60 hidden flex items-center justify-center">
                                <div class="text-center">
                                    <div class="w-16 h-16 border-4 border-dashed border-yellow-400 border-t-transparent rounded-full animate-spin mx-auto mb-4"></div>
                                    <div class="text-xs uppercase tracking-widest text-yellow-400">Scanning inbox...</div>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Phone footer -->
                        <div class="h-7 bg-slate-900 flex justify-center">
                            <div class="w-28 h-1 bg-slate-700 rounded-full mt-2"></div>
                        </div>
                    </div>
                    
                    <!-- Floating badge -->
                    <div class="absolute -top-4 -left-4 bg-slate-900 border border-yellow-400 text-yellow-400 text-[10px] font-medium px-4 py-2 rounded-3xl shadow-2xl flex items-center gap-x-2 rotate-[-8deg]">
                        <i class="fa-solid fa-lock text-xs"></i>
                        <span>READ-ONLY</span>
                    </div>
                    
                    <!-- Floating notification -->
                    <div onclick="showNotificationToast()" 
                         class="absolute -bottom-8 right-8 bg-slate-800 border border-slate-600 shadow-2xl rounded-3xl px-5 py-3 flex items-center gap-x-3 cursor-pointer">
                        <div class="w-7 h-7 bg-rose-500 rounded-2xl flex items-center justify-center text-xs">3</div>
                        <div>
                            <div class="text-xs text-slate-400">3 bills due soon</div>
                            <div class="text-white text-sm font-medium">Reminder sent</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Scroll prompt -->
        <div class="hidden xl:flex absolute bottom-10 left-1/2 flex-col items-center gap-y-1 text-[10px] text-slate-400">
            <div class="uppercase tracking-widest">Scroll for more</div>
            <i class="fa-solid fa-chevron-down text-lg animate-bounce"></i>
        </div>
        
        <div class="absolute bottom-0 left-0 right-0 h-px bg-gradient-to-r from-transparent via-yellow-300/30 to-transparent"></div>
    </header>

    <!-- STATS BAR -->
    <div class="bg-slate-900 py-5 border-b border-slate-800">
        <div class="max-w-screen-2xl mx-auto px-8">
            <div class="grid grid-cols-3 md:grid-cols-6 gap-6 text-center">
                <div>
                    <div class="text-emerald-400 text-xl font-semibold">98%</div>
                    <div class="text-xs text-slate-400 tracking-widest">BILLS DETECTED</div>
                </div>
                <div>
                    <div class="text-emerald-400 text-xl font-semibold">₹4.2cr</div>
                    <div class="text-xs text-slate-400 tracking-widest">PAYMENTS TRACKED</div>
                </div>
                <div>
                    <div class="text-emerald-400 text-xl font-semibold">14k</div>
                    <div class="text-xs text-slate-400 tracking-widest">REMINDERS SENT</div>
                </div>
                <div>
                    <div class="text-emerald-400 text-xl font-semibold">47</div>
                    <div class="text-xs text-slate-400 tracking-widest">BANKS SUPPORTED</div>
                </div>
                <div class="hidden md:block">
                    <div class="text-emerald-400 text-xl font-semibold">0</div>
                    <div class="text-xs text-slate-400 tracking-widest">LATE FEES</div>
                </div>
                <div>
                    <div onclick="window.open('https://mukulmark42.github.io/cardvault-privacy', '_blank')" 
                         class="cursor-pointer inline-flex items-center gap-x-2 text-xs border border-slate-600 hover:border-yellow-400 transition-colors rounded-3xl px-5 py-2">
                        <i class="fa-solid fa-shield"></i>
                        <span>PRIVACY FIRST</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- FEATURES -->
    <section id="features" class="max-w-screen-2xl mx-auto px-8 py-24">
        <div class="flex justify-center mb-6">
            <span onclick="document.getElementById('features').scrollIntoView({ behavior: 'smooth' })" 
                  class="px-5 py-2 bg-slate-900 text-yellow-400 text-xs rounded-3xl border border-yellow-400/30 cursor-pointer">FEATURES</span>
        </div>
        
        <h2 class="text-center text-5xl font-semibold tracking-tight text-white mb-4">Everything you need to manage cards</h2>
        <p class="text-center text-slate-400 max-w-md mx-auto">Smart automation meets rock-solid privacy</p>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mt-16">
            <!-- Feature 1 -->
            <div class="feature-card bg-slate-900 border border-slate-800 rounded-3xl p-8">
                <div class="w-12 h-12 bg-blue-500/10 flex items-center justify-center rounded-2xl mb-8">
                    <i class="fa-solid fa-envelope text-blue-400 text-3xl"></i>
                </div>
                <div class="text-2xl font-semibold mb-3">Email Sync</div>
                <div class="text-slate-400">Read-only Gmail access to detect credit card bills automatically. Never forward anything manually again.</div>
                <ul class="mt-8 space-y-4 text-sm">
                    <li class="flex items-center gap-x-3">
                        <i class="fa-solid fa-check text-emerald-400"></i>
                        <span>Multiple Gmail accounts</span>
                    </li>
                    <li class="flex items-center gap-x-3">
                        <i class="fa-solid fa-check text-emerald-400"></i>
                        <span>Smart keyword detection</span>
                    </li>
                    <li class="flex items-center gap-x-3">
                        <i class="fa-solid fa-check text-emerald-400"></i>
                        <span>Instant parsing</span>
                    </li>
                </ul>
            </div>
            
            <!-- Feature 2 -->
            <div class="feature-card bg-slate-900 border border-slate-800 rounded-3xl p-8">
                <div class="w-12 h-12 bg-purple-500/10 flex items-center justify-center rounded-2xl mb-8">
                    <i class="fa-solid fa-credit-card text-purple-400 text-3xl"></i>
                </div>
                <div class="text-2xl font-semibold mb-3">Multi-card dashboard</div>
                <div class="text-slate-400">All your credit cards in one beautiful place. Track balances, due dates and payment history.</div>
                
                <div class="mt-10 grid grid-cols-2 gap-4">
                    <div class="credit-card text-white p-4 rounded-2xl text-xs">
                        <div class="flex justify-between text-[10px]">
                            <div>VISA</div>
                            <div>•••• 4242</div>
                        </div>
                        <div class="mt-12 text-amber-200 text-lg font-medium">₹29,450</div>
                    </div>
                    <div class="text-xs space-y-6 pt-3">
                        <div class="flex items-center justify-between">
                            <div class="text-slate-400">Due date</div>
                            <div class="font-medium">Mar 12</div>
                        </div>
                        <div class="flex items-center justify-between">
                            <div class="text-slate-400">Minimum due</div>
                            <div class="font-medium text-emerald-400">₹1,500</div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Feature 3 -->
            <div class="feature-card bg-slate-900 border border-slate-800 rounded-3xl p-8">
                <div class="w-12 h-12 bg-rose-500/10 flex items-center justify-center rounded-2xl mb-8">
                    <i class="fa-solid fa-bell text-rose-400 text-3xl"></i>
                </div>
                <div class="text-2xl font-semibold mb-3">Smart reminders</div>
                <div class="text-slate-400">Receive timely push notifications before your bill is due. Never incur a late fee again.</div>
                <div class="mt-16 bg-slate-950 border border-dashed border-slate-700 rounded-3xl p-5 text-center">
                    <div class="text-xs text-slate-400 mb-2">NEXT REMINDER IN</div>
                    <div class="text-5xl font-semibold text-white tabular-nums" id="countdown">42</div>
                    <div class="text-xs text-slate-400">hours</div>
                </div>
            </div>
            
            <!-- Feature 4 -->
            <div class="feature-card bg-slate-900 border border-slate-800 rounded-3xl p-8">
                <div class="w-12 h-12 bg-cyan-400/10 flex items-center justify-center rounded-2xl mb-8">
                    <i class="fa-solid fa-cloud text-cyan-400 text-3xl"></i>
                </div>
                <div class="text-2xl font-semibold mb-3">Cloud sync</div>
                <div class="text-slate-400">All your data is stored securely on Firebase. Access your cards from any device instantly.</div>
                <div class="flex items-center gap-x-6 mt-12 text-xs">
                    <div class="flex-1 h-px bg-gradient-to-r from-transparent to-cyan-400"></div>
                    <span class="uppercase text-cyan-400 font-medium">Synced live</span>
                    <div class="flex-1 h-px bg-gradient-to-l from-transparent to-cyan-400"></div>
                </div>
            </div>
            
            <!-- Feature 5 -->
            <div class="feature-card bg-slate-900 border border-slate-800 rounded-3xl p-8">
                <div class="w-12 h-12 bg-violet-500/10 flex items-center justify-center rounded-2xl mb-8">
                    <i class="fa-solid fa-lock text-violet-400 text-3xl"></i>
                </div>
                <div class="text-2xl font-semibold mb-3">Bank-grade security</div>
                <div class="text-slate-400">Your passwords are never stored. We use industry-standard encryption and Firebase security rules.</div>
                <div class="mt-8 text-[10px] flex items-center gap-x-5 text-slate-400">
                    <div class="px-4 py-2 border border-slate-600 rounded-3xl">TLS</div>
                    <div class="px-4 py-2 border border-slate-600 rounded-3xl">AES-256</div>
                    <div class="px-4 py-2 border border-slate-600 rounded-3xl">OAuth</div>
                </div>
            </div>
            
            <!-- Feature 6 -->
            <div class="feature-card bg-slate-900 border border-slate-800 rounded-3xl p-8 flex flex-col">
                <div class="w-12 h-12 bg-amber-400/10 flex items-center justify-center rounded-2xl mb-8">
                    <i class="fa-solid fa-chart-simple text-amber-400 text-3xl"></i>
                </div>
                <div class="text-2xl font-semibold mb-3">Analytics</div>
                <div class="text-slate-400 flex-1">Beautiful insights into your spending patterns across all cards.</div>
                
                <div class="mt-auto pt-12">
                    <div class="h-2 bg-slate-700 rounded-3xl relative overflow-hidden">
                        <div class="absolute left-0 top-0 h-full bg-gradient-to-r from-yellow-300 to-amber-400 rounded-3xl w-3/4"></div>
                    </div>
                    <div class="flex justify-between text-[10px] text-slate-400 mt-3">
                        <div>Spent this month</div>
                        <div class="font-medium text-white">68%</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- HOW IT WORKS -->
    <section id="how" class="bg-slate-950 py-20 border-t border-b border-slate-800">
        <div class="max-w-screen-2xl mx-auto px-8">
            <div class="grid md:grid-cols-12 gap-x-16 items-center">
                <div class="md:col-span-5">
                    <div class="sticky top-28">
                        <span class="px-4 py-1 text-xs rounded-3xl bg-white/5 text-white">3 STEPS • 30 SECONDS</span>
                        <h2 class="text-5xl font-semibold tracking-tighter leading-none mt-3">This simple. This powerful.</h2>
                        <p class="mt-6 text-slate-400">Connect • Detect • Relax</p>
                        
                        <div class="hidden md:flex gap-x-3 mt-12">
                            <button onclick="prevStep()" 
                                    class="w-10 h-10 flex items-center justify-center border border-slate-600 hover:border-slate-300 rounded-2xl text-xl transition-colors">
                                ←
                            </button>
                            <button onclick="nextStep()" 
                                    class="w-10 h-10 flex items-center justify-center border border-slate-600 hover:border-slate-300 rounded-2xl text-xl transition-colors">
                                →
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Steps -->
                <div class="md:col-span-7 mt-12 md:mt-0">
                    <div id="step-container" class="space-y-6">
                        <!-- Populated by JS -->
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- DEMO / LIVE PREVIEW -->
    <section id="demo" class="max-w-screen-2xl mx-auto px-8 py-20 bg-slate-900">
        <div class="flex flex-col lg:flex-row gap-16">
            <div class="lg:w-5/12">
                <h2 class="text-4xl font-semibold tracking-tight">See your cards come alive</h2>
                <p class="mt-4 text-slate-400">This is what the mobile app looks like. All data is mocked for demo purposes.</p>
                
                <div class="mt-12 space-y-8">
                    <div class="flex gap-5">
                        <div class="shrink-0 w-7 h-7 rounded-2xl bg-white flex items-center justify-center text-slate-900 text-xs font-bold">1</div>
                        <div>
                            <div class="font-medium">Add your Gmail</div>
                            <div class="text-sm text-slate-400">We only request read-only permission. You can revoke anytime.</div>
                        </div>
                    </div>
                    <div class="flex gap-5">
                        <div class="shrink-0 w-7 h-7 rounded-2xl bg-white flex items-center justify-center text-slate-900 text-xs font-bold">2</div>
                        <div>
                            <div class="font-medium">Bills get detected automatically</div>
                            <div class="text-sm text-slate-400">Our AI scans for keywords like “statement”, “due”, “outstanding” etc.</div>
                        </div>
                    </div>
                    <div class="flex gap-5">
                        <div class="shrink-0 w-7 h-7 rounded-2xl bg-white flex items-center justify-center text-slate-900 text-xs font-bold">3</div>
                        <div>
                            <div class="font-medium">Get reminded on time</div>
                            <div class="text-sm text-slate-400">Push notifications, email summaries, and calendar invites.</div>
                        </div>
                    </div>
                </div>
                
                <button onclick="simulateScan()" 
                        class="mt-16 flex items-center justify-center gap-x-4 group border border-dashed border-slate-500 hover:border-yellow-400 transition-colors px-7 h-12 rounded-3xl text-sm font-medium">
                    <span class="group-active:rotate-45 transition-transform inline-block">⟳</span> 
                    <span>SIMULATE NEW BILL SCAN</span>
                </button>
            </div>
            
            <!-- Cards demo -->
            <div class="lg:w-7/12">
                <div class="bg-slate-950 border border-slate-700 rounded-3xl p-6">
                    <div class="flex justify-between items-center pb-6 border-b border-slate-700">
                        <div class="font-medium flex items-center gap-x-2">
                            <span class="text-yellow-400">Your cards</span> 
                            <span class="text-xs bg-slate-800 text-slate-400 px-3 rounded-3xl py-px">4 active</span>
                        </div>
                        <div onclick="addFakeCard()" class="text-xs flex items-center gap-x-2 cursor-pointer hover:text-yellow-300">
                            <i class="fa-solid fa-plus"></i>
                            <span>ADD CARD</span>
                        </div>
                    </div>
                    
                    <div id="demo-cards" class="pt-6 grid grid-cols-1 sm:grid-cols-2 gap-6">
                        <!-- JS injected cards -->
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SECURITY -->
    <section id="security" class="max-w-screen-2xl mx-auto px-8 py-24 bg-black">
        <div class="max-w-2xl mx-auto text-center mb-16">
            <span class="text-xs font-semibold bg-white text-slate-950 px-6 py-3 rounded-3xl">WE TAKE PRIVACY SERIOUSLY</span>
            <h2 class="text-5xl font-semibold tracking-tighter mt-6">Your data is never sold.<br>Your inbox stays private.</h2>
        </div>
        
        <div class="grid md:grid-cols-12 gap-8 max-w-screen-xl mx-auto">
            <div class="md:col-span-4 bg-slate-900 rounded-3xl p-7">
                <i class="fa-solid fa-key text-4xl mb-8 text-yellow-400"></i>
                <h4 class="font-medium mb-2">Read-only access</h4>
                <p class="text-xs leading-relaxed text-slate-400">We only read the emails that look like credit card statements. We cannot send emails or modify your inbox.</p>
                <a href="https://mukulmark42.github.io/cardvault-privacy" target="_blank" 
                   class="inline-flex items-center gap-x-2 text-xs mt-8 text-slate-400 hover:text-white">
                    FULL POLICY 
                    <span class="text-lg leading-none">→</span>
                </a>
            </div>
            <div class="md:col-span-4 bg-slate-900 rounded-3xl p-7">
                <i class="fa-solid fa-fingerprint text-4xl mb-8 text-cyan-400"></i>
                <h4 class="font-medium mb-2">No passwords stored</h4>
                <p class="text-xs leading-relaxed text-slate-400">OAuth2 authentication is used. Your Gmail password is never seen or stored by us.</p>
                <div class="text-[10px] bg-slate-950 text-slate-400 px-5 py-6 rounded-3xl mt-12 font-mono text-center">
                    oauth2.googleapis.com
                </div>
            </div>
            <div class="md:col-span-4 bg-slate-900 rounded-3xl p-7 flex flex-col">
                <i class="fa-solid fa-server text-4xl mb-8 text-violet-400"></i>
                <h4 class="font-medium mb-2">Data encrypted at rest</h4>
                <p class="text-xs leading-relaxed text-slate-400">All your bill metadata is encrypted using Firebase security rules.</p>
                
                <div class="mt-auto pt-12 text-xs flex justify-between items-end">
                    <div>
                        <div class="font-medium">Powered by</div>
                        <div class="text-emerald-300 font-medium">Firebase</div>
                    </div>
                    <div class="text-[42px] font-light text-slate-700">🔒</div>
                </div>
            </div>
        </div>
        
        <!-- Data usage summary -->
        <div class="max-w-2xl mx-auto mt-24 text-xs bg-slate-900/60 border border-slate-700 rounded-3xl p-8">
            <div class="uppercase text-yellow-300 mb-6 flex items-center gap-4">
                <div class="flex-1 h-px bg-yellow-300"></div>
                <span>HOW WE USE YOUR DATA</span>
                <div class="flex-1 h-px bg-yellow-300"></div>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-x-12 gap-y-8 text-slate-400">
                <div class="space-y-6">
                    <div class="flex gap-4">
                        <span class="font-mono text-lg text-slate-300">01</span>
                        <div>Detect credit card statements from your inbox</div>
                    </div>
                    <div class="flex gap-4">
                        <span class="font-mono text-lg text-slate-300">02</span>
                        <div>Extract due dates, amounts and issuer names</div>
                    </div>
                </div>
                <div class="space-y-6">
                    <div class="flex gap-4">
                        <span class="font-mono text-lg text-slate-300">03</span>
                        <div>Send you push notifications 48h before due</div>
                    </div>
                    <div class="flex gap-4">
                        <span class="font-mono text-lg text-slate-300">04</span>
                        <div class="line-through opacity-40">We never read your personal emails</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIAL / QUOTE -->
    <div class="bg-slate-950 py-16">
        <div class="max-w-screen-2xl mx-auto px-8">
            <div class="max-w-xl mx-auto text-center">
                <div class="italic text-2xl leading-tight text-slate-300">
                    “I used to pay late fees every other month. CardVault caught a ₹28,000 bill I almost missed. 
                    Saved me a lot of stress and money.”
                </div>
                <div class="flex items-center justify-center gap-x-4 mt-10">
                    <div class="w-9 h-px bg-slate-600"></div>
                    <div>
                        <div class="text-sm">Rahul Sharma</div>
                        <div class="text-xs text-slate-400">Product designer @ Razorpay</div>
                    </div>
                    <div class="w-9 h-px bg-slate-600"></div>
                </div>
            </div>
        </div>
    </div>

    <!-- FINAL CTA -->
    <div class="bg-gradient-to-b from-transparent to-yellow-300/10 py-20">
        <div class="max-w-2xl mx-auto text-center px-5">
            <span class="px-5 py-2 text-xs bg-yellow-400 text-slate-950 font-semibold rounded-3xl">READY TO GET ORGANIZED?</span>
            
            <h2 class="text-6xl font-semibold text-white tracking-tighter mt-8 leading-none">Start managing your credit cards today</h2>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center mt-12">
                <button onclick="showGetStartedModal()" 
                        class="flex-1 sm:flex-none px-10 py-6 bg-white text-slate-900 rounded-3xl font-semibold flex items-center justify-center gap-x-4 group">
                    <span>Connect Gmail now</span> 
                    <span class="block group-active:rotate-45 transition">→</span>
                </button>
                
                <button onclick="window.open('https://mukulmark42.github.io/cardvault-privacy', '_blank')" 
                        class="flex-1 sm:flex-none px-10 py-6 border border-slate-300 rounded-3xl text-slate-200 font-medium">
                    Learn about our privacy
                </button>
            </div>
            
            <div class="text-xs text-slate-400 mt-8 flex items-center justify-center gap-x-5">
                <div class="flex items-center gap-x-2">
                    <i class="fa-solid fa-lock"></i>
                    <span>Secure OAuth</span>
                </div>
                <div class="h-px w-6 bg-slate-600"></div>
                <div class="text-emerald-400">Cancel anytime</div>
            </div>
        </div>
    </div>

    <!-- FOOTER -->
    <footer class="bg-black pt-20 pb-12">
        <div class="max-w-screen-2xl mx-auto px-8 grid grid-cols-2 md:grid-cols-5 gap-y-14">
            <!-- Col 1 -->
            <div>
                <div class="flex items-center gap-x-3 text-white">
                    <div class="w-7 h-7 bg-yellow-400 text-slate-950 rounded-2xl flex items-center justify-center">
                        <i class="fa-solid fa-vault"></i>
                    </div>
                    <span class="logo-font text-4xl tracking-tighter">CardVault</span>
                </div>
                <p class="text-xs text-slate-400 mt-6 max-w-[190px]">Smart bill reminders for your credit cards.</p>
                
                <div class="mt-12 text-xs font-medium flex items-center gap-x-5">
                    <a href="https://twitter.com" target="_blank" class="hover:text-white transition-colors">𝕏</a>
                    <a href="#" class="hover:text-white transition-colors">IG</a>
                </div>
            </div>
            
            <!-- Col 2 -->
            <div class="text-sm">
                <div class="uppercase text-slate-400 text-xs mb-6 tracking-wider">Product</div>
                <div class="space-y-6 text-slate-300">
                    <a href="#features" class="block hover:text-yellow-200">Features</a>
                    <a href="#how" class="block hover:text-yellow-200">How it works</a>
                    <a href="#demo" class="block hover:text-yellow-200">Demo</a>
                    <a href="#" onclick="showLoginModal()" class="block hover:text-yellow-200">Login</a>
                </div>
            </div>
            
            <!-- Col 3 -->
            <div class="text-sm">
                <div class="uppercase text-slate-400 text-xs mb-6 tracking-wider">Company</div>
                <div class="space-y-6 text-slate-300">
                    <a href="#" class="block hover:text-yellow-200">About us</a>
                    <a href="#" class="block hover:text-yellow-200">Blog</a>
                    <a href="#" class="block hover:text-yellow-200">Support</a>
                    <a href="https://mukulmark42.github.io/Terms-of-Service" target="_blank" class="block hover:text-yellow-200">Terms</a>
                </div>
            </div>
            
            <!-- Col 4 -->
            <div class="text-sm">
                <div class="uppercase text-slate-400 text-xs mb-6 tracking-wider">Legal</div>
                <div onclick="window.open('https://mukulmark42.github.io/cardvault-privacy', '_blank')" 
                     class="cursor-pointer text-slate-300 hover:text-yellow-200 flex items-center gap-x-2">
                    <i class="fa-solid fa-file-lines text-xs"></i>
                    <span>Privacy policy</span>
                </div>
                <div onclick="window.open('https://mukulmark42.github.io/Terms-of-Service', '_blank')" 
                     class="cursor-pointer mt-6 text-slate-300 hover:text-yellow-200 flex items-center gap-x-2">
                    <i class="fa-solid fa-file-lines text-xs"></i>
                    <span>Terms of service</span>
                </div>
            </div>
            
            <!-- Col 5 -->
            <div>
                <div class="bg-slate-900 p-6 rounded-3xl">
                    <div class="text-xs font-medium">Questions or feedback?</div>
                    <a href="mailto:info@ssinfotech.qzz.io" 
                       class="block mt-3 text-sm text-yellow-300 hover:underline">info@ssinfotech.qzz.io</a>
                    
                    <div class="mt-16 text-[10px] text-slate-400">
                        Made with care in India 🇮🇳<br>
                        v24.03.12
                    </div>
                </div>
            </div>
        </div>
        
        <div class="text-center text-[10px] text-slate-500 mt-20">
            © 2025 CardVault. All rights reserved. Not a real financial institution.
        </div>
    </footer>

    <!-- GET STARTED MODAL -->
    <div onclick="if(event.target.id === 'get-modal') this.style.display = 'none'" id="get-modal"
         class="hidden fixed inset-0 bg-black/70 flex items-end md:items-center justify-center z-[9999]">
        <div onclick="event.stopImmediatePropagation()" 
             class="bg-slate-900 w-full max-w-lg mx-4 md:mx-0 rounded-t-3xl md:rounded-3xl overflow-hidden">
            
            <!-- Modal header -->
            <div class="px-8 pt-8 pb-4 border-b border-slate-700 flex items-center">
                <span class="font-semibold text-xl">Connect your inbox</span>
                <button onclick="hideGetStartedModal()" 
                        class="ml-auto text-slate-400 hover:text-white text-3xl leading-none">×</button>
            </div>
            
            <div class="p-8">
                <div class="border border-slate-600 rounded-3xl p-6">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center gap-x-4">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Gmail_icon_%282020%29.svg/512px-Gmail_icon_%282020%29.svg.png" 
                                 alt="Gmail" class="w-8 h-8">
                            <div>
                                <div class="font-medium text-white">Gmail</div>
                                <div class="text-xs text-slate-400">Recommended</div>
                            </div>
                        </div>
                        <div onclick="connectDemo()" 
                             class="bg-white text-slate-900 text-xs font-semibold px-7 py-3 rounded-3xl cursor-pointer active:scale-95 transition">
                            CONNECT
                        </div>
                    </div>
                </div>
                
                <div class="my-8 text-xs text-center text-slate-400">or connect other providers soon</div>
                
                <div class="flex justify-center gap-8 text-slate-400">
                    <div class="text-center cursor-not-allowed">
                        <div class="w-9 h-9 mx-auto bg-slate-800 rounded-2xl flex items-center justify-center text-xl">📧</div>
                        <div class="text-[10px] mt-2">Outlook</div>
                    </div>
                    <div class="text-center cursor-not-allowed">
                        <div class="w-9 h-9 mx-auto bg-slate-800 rounded-2xl flex items-center justify-center text-xl">🧾</div>
                        <div class="text-[10px] mt-2">Yahoo</div>
                    </div>
                </div>
            </div>
            
            <div class="bg-slate-950 px-8 py-6 text-xs flex items-center justify-between text-slate-400">
                <div class="flex items-center gap-x-4">
                    <i class="fa-solid fa-lock"></i>
                    <span>Secured by Google OAuth</span>
                </div>
                <button onclick="hideGetStartedModal()" 
                        class="underline">Cancel</button>
            </div>
        </div>
    </div>

    <!-- LOGIN MODAL -->
    <div onclick="if(event.target.id === 'login-modal') this.style.display = 'none'" id="login-modal"
         class="hidden fixed inset-0 bg-black/70 flex items-center justify-center z-[9999]">
        <div onclick="event.stopImmediatePropagation()" 
             class="bg-slate-900 w-full max-w-md rounded-3xl p-8">
            <div class="text-center">
                <span class="logo-font text-4xl text-yellow-300">CardVault</span>
            </div>
            
            <div class="mt-10">
                <input id="fake-email" type="text" value="demo@cardvault.app" 
                       class="block w-full bg-slate-800 border-0 focus:ring-1 focus:ring-yellow-400 rounded-3xl px-6 h-14 outline-none text-sm">
            </div>
            
            <button onclick="fakeLogin()" 
                    class="mt-4 w-full h-14 bg-white text-slate-950 rounded-3xl font-semibold">Continue with email</button>
            
            <div class="flex items-center gap-x-4 my-8">
                <div class="flex-1 h-px bg-slate-700"></div>
                <span class="uppercase text-xs text-slate-400">or</span>
                <div class="flex-1 h-px bg-slate-700"></div>
            </div>
            
            <button onclick="fakeLogin()" 
                    class="w-full flex justify-center items-center gap-x-3 border border-slate-600 hover:border-white h-12 rounded-3xl text-sm">
                <i class="fa-brands fa-google"></i>
                <span>Sign in with Google</span>
            </button>
            
            <div onclick="hideLoginModal()" 
                 class="text-center text-xs mt-8 cursor-pointer text-slate-400">Close</div>
        </div>
    </div>

    <!-- TOAST -->
    <div id="toast" onclick="this.style.transform = 'translateY(100px)'"
         class="hidden fixed bottom-6 right-6 bg-slate-800 border border-yellow-400 text-yellow-200 rounded-3xl px-6 py-4 flex items-center gap-x-3 shadow-2xl">
        <i class="fa-solid fa-check-circle"></i>
        <div class="text-sm pr-6" id="toast-text">Bill detected from SBI</div>
    </div>

    <script>
        // Tailwind script run
        function initializeTailwind() {
            const script = document.createElement('script')
            // Already included via CDN
        }
        
        function smoothScrollTo(section) {
            let el
            if (section === 'features') el = document.getElementById('features')
            else if (section === 'how') el = document.getElementById('how')
            else if (section === 'security') el = document.getElementById('security')
            else if (section === 'demo') el = document.getElementById('demo')
            
            if (el) {
                el.scrollIntoView({ behavior: "smooth" })
            }
            toggleMobileMenu(true)
        }
        
        let currentStep = 0
        const steps = [
            {
                num: "01",
                title: "Connect your Gmail",
                desc: "Grant read-only access to your inbox via secure OAuth. Takes less than 15 seconds.",
                color: "yellow"
            },
            {
                num: "02",
                title: "AI scans your inbox",
                desc: "We look for patterns in emails from banks and credit card providers.",
                color: "blue"
            },
            {
                num: "03",
                title: "Bills appear instantly",
                desc: "Due dates and amounts are extracted and shown in a clean dashboard.",
                color: "emerald"
            }
        ]
        
        function renderSteps() {
            const container = document.getElementById("step-container")
            container.innerHTML = ""
            
            steps.forEach((step, index) => {
                const active = index === currentStep
                
                const div = document.createElement("div")
                div.className = `p-8 border ${active ? 'border-yellow-400 bg-slate-900' : 'border-transparent bg-slate-950'} rounded-3xl transition-all flex gap-7`
                div.innerHTML = `
                    <div class="font-mono text-6xl font-light ${active ? 'text-yellow-400' : 'text-slate-600'}">${step.num}</div>
                    <div class="flex-1">
                        <div class="font-semibold text-2xl ${active ? 'text-white' : 'text-slate-400'}">${step.title}</div>
                        <div class="text-slate-400 mt-3">${step.desc}</div>
                    </div>
                `
                container.append(div)
            })
        }
        
        function nextStep() {
            currentStep = (currentStep + 1) % steps.length
            renderSteps()
        }
        
        function prevStep() {
            currentStep = (currentStep - 1 + steps.length) % steps.length
            renderSteps()
        }
        
        // Demo cards
        let demoCardData = [
            {
                issuer: "HDFC",
                last4: "4582",
                due: "Mar 18",
                amount: "18499",
                color: "from-blue-600 to-indigo-700"
            },
            {
                issuer: "SBI",
                last4: "7719",
                due: "Mar 9",
                amount: "6200",
                color: "from-red-600 to-rose-600"
            }
        ]
        
        function createDemoCard(card) {
            const wrapper = document.createElement("div")
            wrapper.className = `bill-card bg-gradient-to-br ${card.color} text-white p-5 rounded-3xl cursor-pointer`
            wrapper.innerHTML = `
                <div class="flex justify-between">
                    <div>
                        <div class="flex items-center gap-x-3">
                            <span class="text-xs tracking-wider opacity-75">${card.issuer}</span>
                            <span class="text-xs font-light">•••• ${card.last4}</span>
                        </div>
                        <div class="text-3xl font-light mt-7">₹${card.amount}</div>
                    </div>
                    
                    <div class="text-right flex flex-col justify-between">
                        <div class="text-xs bg-black/30 w-16 text-center py-1 rounded-3xl">VISA</div>
                        <div>
                            <div class="text-xs opacity-75">due</div>
                            <div class="text-lg font-medium">${card.due}</div>
                        </div>
                    </div>
                </div>
            `
            return wrapper
        }
        
        function renderDemoCards() {
            const container = document.getElementById("demo-cards")
            container.innerHTML = ""
            
            demoCardData.forEach(card => {
                container.appendChild(createDemoCard(card))
            })
            
            // Add a third smaller card
            const third = document.createElement("div")
            third.className = "col-span-1 sm:col-span-2 bg-slate-800 rounded-3xl p-5 flex justify-between items-center text-xs"
            third.innerHTML = `
                <div class="flex items-center gap-x-4">
                    <div class="text-emerald-400">
                        <i class="fa-solid fa-circle-check text-3xl"></i>
                    </div>
                    <div>
                        <div class="font-medium">Axis Bank</div>
                        <div class="text-slate-400">Paid on time</div>
                    </div>
                </div>
                <div class="text-right">
                    <div class="font-light text-2xl text-emerald-400">₹4500</div>
                    <div class="text-[10px]">Feb 27</div>
                </div>
            `
            container.appendChild(third)
        }
        
        function addFakeCard() {
            const newCard = {
                issuer: "ICICI",
                last4: "9931",
                due: "Apr 2",
                amount: "12500",
                color: "from-teal-500 to-cyan-500"
            }
            demoCardData.push(newCard)
            renderDemoCards()
            
            showToast("New card added to demo", 1800)
        }
        
        function fakeBillClick(el) {
            el.style.transform = "scale(0.95)"
            setTimeout(() => {
                el.style.transform = "scale(1)"
            }, 180)
            showToast("Bill marked as paid ✓", 2200)
        }
        
        function simulateScan() {
            const overlay = document.getElementById("scan-overlay")
            if (overlay) {
                overlay.classList.remove("hidden")
                overlay.style.display = "flex"
                
                setTimeout(() => {
                    overlay.style.display = "none"
                    showToast("New bill from Kotak detected", 2600)
                    
                    // Add a new card
                    const newScanCard = {
                        issuer: "KOTAK",
                        last4: "1124",
                        due: "Mar 30",
                        amount: "8750",
                        color: "from-purple-500 to-violet-600"
                    }
                    demoCardData.unshift(newScanCard)
                    renderDemoCards()
                }, 2100)
            }
        }
        
        function showToast(message, timeout = 2400) {
            const toast = document.getElementById("toast")
            const toastText = document.getElementById("toast-text")
            toastText.textContent = message
            toast.classList.remove("hidden")
            toast.style.transform = "translateY(0)"
            
            setTimeout(() => {
                toast.style.transform = "translateY(80px)"
                setTimeout(() => {
                    toast.classList.add("hidden")
                }, 600)
            }, timeout)
        }
        
        function showNotificationToast() {
            showToast("Reminder: HDFC bill due in 2 days", 3000)
        }
        
        // Modal controls
        function showGetStartedModal() {
            const modal = document.getElementById("get-modal")
            modal.classList.remove("hidden")
            modal.style.display = "flex"
        }
        
        function hideGetStartedModal() {
            const modal = document.getElementById("get-modal")
            modal.style.display = "none"
        }
        
        function showLoginModal() {
            const modal = document.getElementById("login-modal")
            modal.classList.remove("hidden")
            modal.style.display = "flex"
        }
        
        function hideLoginModal() {
            const modal = document.getElementById("login-modal")
            modal.style.display = "none"
        }
        
        function fakeLogin() {
            hideLoginModal()
            setTimeout(() => {
                showToast("Welcome back, demo user 👋", 2100)
            }, 700)
        }
        
        function connectDemo() {
            hideGetStartedModal()
            setTimeout(() => {
                showToast("Gmail connected successfully • 0 bills found", 2600)
            }, 400)
        }
        
        function watchDemo() {
            const messages = [
                "Scanning inbox...",
                "Detected 2 new statements",
                "Reminder scheduled"
            ]
            let i = 0
            const interval = setInterval(() => {
                if (i > 2) {
                    clearInterval(interval)
                    return
                }
                showToast(messages[i], 1300)
                i++
            }, 900)
        }
        
        function toggleMobileMenu(forceClose) {
            const mobileMenu = document.getElementById("mobile-menu")
            const icon = document.getElementById("mobile-menu-button")
            
            if (forceClose || !mobileMenu.classList.contains("hidden")) {
                mobileMenu.classList.add("hidden")
                icon.innerHTML = `<i class="fa-solid fa-bars"></i>`
            } else {
                mobileMenu.classList.remove("hidden")
                icon.innerHTML = `<i class="fa-solid fa-xmark"></i>`
            }
        }
        
        // Countdown demo
        function startFakeCountdown() {
            let count = 67
            const el = document.getElementById("countdown")
            
            if (!el) return
            
            const interval = setInterval(() => {
                count--
                if (count < 10) count = 67
                el.textContent = count
            }, 2100)
        }
        
        // Keyboard shortcuts
        function handleKeyboard(e) {
            if (e.metaKey && e.key === "k") {
                e.preventDefault()
                showGetStartedModal()
            }
        }
        
        // Main initialization
        function initialize() {
            // Tailwind ready
            renderSteps()
            renderDemoCards()
            startFakeCountdown()
            
            // Mobile menu handler
            const hamburger = document.getElementById("mobile-menu-button")
            hamburger.addEventListener("click", () => toggleMobileMenu())
            
            // Close modals when pressing escape
            document.addEventListener("keydown", function(e) {
                if (e.key === "Escape") {
                    const getModal = document.getElementById("get-modal")
                    const loginModal = document.getElementById("login-modal")
                    
                    if (getModal.style.display !== "none") hideGetStartedModal()
                    else if (loginModal.style.display !== "none") hideLoginModal()
                }
                
                handleKeyboard(e)
            })
            
            // Click anywhere outside the phone demo to hide scan overlay
            const phoneContainer = document.querySelector(".bg-slate-900.border-8")
            if (phoneContainer) {
                phoneContainer.addEventListener("click", function(e) {
                    const overlay = document.getElementById("scan-overlay")
                    if (overlay && overlay.style.display !== "none") {
                        if (!e.target.closest("#scan-overlay")) {
                            overlay.style.display = "none"
                        }
                    }
                })
            }
            
            // Make the countdown interactive
            const countdownEl = document.getElementById("countdown")
            if (countdownEl) {
                countdownEl.addEventListener("click", () => {
                    countdownEl.style.transitionDuration = "400ms"
                    countdownEl.style.transform = "scale(1.6)"
                    setTimeout(() => {
                        countdownEl.style.transform = "scale(1)"
                    }, 420)
                })
            }
            
            // Demo finish
            console.log('%c✅ CardVault landing page ready', 'font-family:monospace;color:#fcd34d;font-size:10px')
            
            // Random toast every 18 seconds
            setInterval(() => {
                if (Math.random() > 0.6) {
                    const messages = [
                        "Axis bill synced",
                        "Reminder delivered",
                        "All clear ✅"
                    ]
                    showToast(messages[Math.floor(Math.random()*messages.length)], 1500)
                }
            }, 18000)
            
            // Make all external links open in new tab automatically
            const externalLinks = document.querySelectorAll("a[target='_blank']")
            externalLinks.forEach(link => {
                link.setAttribute("rel", "noopener")
            })
        }
        
        // Boot app
        window.onload = initialize
    </script>
</body>
</html>

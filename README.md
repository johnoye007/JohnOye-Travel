<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>John Oye's Travels - Universal App</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    screens: {
                        'xs': '475px',
                        'sm': '640px',
                        'md': '768px',
                        'lg': '1024px',
                        'xl': '1280px',
                        '2xl': '1536px',
                    }
                }
            }
        }
    </script>
    <style>
        body {
            box-sizing: border-box;
        }
        
        /* Desktop/Windows PC Styles */
        @media (min-width: 1024px) {
            .app-container {
                max-width: 420px;
                margin: 0 auto;
                background: white;
                box-shadow: 0 0 30px rgba(0,0,0,0.1);
                border-radius: 24px;
                overflow: hidden;
                min-height: 100vh;
                position: relative;
            }
            
            .status-bar {
                display: none;
            }
            
            .desktop-header {
                display: block;
                background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
                color: white;
                padding: 20px;
                text-align: center;
            }
            
            .bottom-nav {
                position: relative;
                border-radius: 0 0 24px 24px;
            }
            
            .floating-action {
                bottom: 100px;
            }
        }
        
        /* Tablet Styles */
        @media (min-width: 768px) and (max-width: 1023px) {
            .tablet-grid {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .tablet-social-grid {
                grid-template-columns: repeat(4, 1fr);
            }
            
            .hero-gradient {
                padding: 2rem;
            }
            
            .swipe-card {
                margin: 8px;
            }
            
            .quick-actions-tablet {
                grid-template-columns: repeat(2, 1fr);
                gap: 1rem;
            }
        }
        
        /* Mobile Landscape */
        @media (orientation: landscape) and (max-height: 500px) {
            .hero-gradient {
                padding: 1rem;
            }
            
            .hero-gradient h2 {
                font-size: 1.25rem;
            }
            
            .pull-to-refresh {
                padding: 10px;
            }
            
            .app-header {
                padding: 12px 16px;
            }
        }
        
        /* High DPI Displays */
        @media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
            .card-hover {
                transform: translateZ(0);
            }
        }
        
        /* Windows PC Specific */
        @media (min-width: 1024px) and (pointer: fine) {
            .nav-item:hover {
                background: rgba(59, 130, 246, 0.1);
                border-radius: 8px;
            }
            
            .card-hover:hover {
                transform: translateY(-2px) scale(1.02);
            }
            
            button:hover {
                transform: translateY(-1px);
            }
        }
        
        /* Print Styles */
        @media print {
            .status-bar, .bottom-nav, .floating-action {
                display: none !important;
            }
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        
        .card-hover {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: white;
            border-top: 1px solid #e5e7eb;
            z-index: 50;
            padding: 8px 0;
        }
        
        .nav-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 8px;
            text-decoration: none;
            color: #6b7280;
            transition: color 0.3s ease;
        }
        
        .nav-item.active {
            color: #3b82f6;
        }
        
        .nav-item:hover {
            color: #3b82f6;
        }
        
        .screen {
            display: none;
            padding-bottom: 80px;
        }
        
        .screen.active {
            display: block;
        }
        
        .status-bar {
            background: #000;
            color: white;
            padding: 4px 16px;
            font-size: 14px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .app-header {
            background: white;
            padding: 16px;
            border-bottom: 1px solid #e5e7eb;
            position: sticky;
            top: 0;
            z-index: 40;
        }
        
        .floating-action {
            position: fixed;
            bottom: 90px;
            right: 20px;
            background: #10b981;
            color: white;
            width: 56px;
            height: 56px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(16, 185, 129, 0.4);
            z-index: 45;
            text-decoration: none;
        }
        
        .notification-badge {
            position: absolute;
            top: -4px;
            right: -4px;
            background: #ef4444;
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            font-size: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .swipe-card {
            background: white;
            border-radius: 16px;
            margin: 8px 16px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .pull-to-refresh {
            text-align: center;
            padding: 20px;
            color: #6b7280;
        }
        
        /* Safe Area Support for iPhone */
        @supports (padding: max(0px)) {
            .status-bar {
                padding-top: max(4px, env(safe-area-inset-top));
            }
            
            .bottom-nav {
                padding-bottom: max(8px, env(safe-area-inset-bottom));
            }
        }
        
        /* Dark Mode Support */
        @media (prefers-color-scheme: dark) {
            .lg\\:bg-gradient-to-br {
                background: linear-gradient(to bottom right, #1f2937, #374151);
            }
        }
        
        /* Reduced Motion Support */
        @media (prefers-reduced-motion: reduce) {
            .card-hover {
                transition: none;
            }
            
            button {
                transition: none;
            }
        }
    </style>
</head>
<body class="bg-gray-50 font-sans lg:bg-gradient-to-br lg:from-blue-50 lg:to-purple-50 lg:min-h-screen lg:py-8">
    <!-- Desktop Header (Desktop Only) -->
    <div class="desktop-header hidden lg:block">
        <h1 class="text-2xl font-bold mb-2">John Oye's Travels</h1>
        <p class="text-blue-100">Your Gateway to Amazing Adventures</p>
    </div>
    
    <!-- App Container -->
    <div class="app-container">
        <!-- Status Bar -->
        <div class="status-bar lg:hidden">
            <div class="flex items-center space-x-1">
                <span>9:41</span>
            </div>
            <div class="flex items-center space-x-1">
                <span>📶</span>
                <span>📶</span>
                <span>🔋</span>
                <span>100%</span>
            </div>
        </div>

        <!-- Home Screen -->
        <div id="home-screen" class="screen active">
            <!-- App Header -->
            <div class="app-header">
                <div class="flex items-center justify-between">
                    <div class="flex items-center space-x-3">
                        <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center">
                            <span class="text-white text-xl">✈️</span>
                        </div>
                        <div>
                            <h1 class="text-lg font-bold text-gray-800">John Oye's Travels</h1>
                            <p class="text-sm text-gray-500">Explore the World</p>
                        </div>
                    </div>
                    <div class="flex items-center space-x-3">
                        <button class="relative">
                            <span class="text-2xl">🔔</span>
                            <div class="notification-badge">3</div>
                        </button>
                        <button class="w-8 h-8 bg-gray-200 rounded-full"></button>
                    </div>
                </div>
            </div>

            <!-- Pull to Refresh -->
            <div class="pull-to-refresh lg:hidden">
                <div class="text-2xl mb-2">⬇️</div>
                <p class="text-sm">Pull to refresh</p>
            </div>

            <!-- Hero Section -->
            <div class="hero-gradient text-white p-6 m-4 rounded-2xl">
                <h2 class="text-2xl font-bold mb-2">Ready for Adventure?</h2>
                <p class="text-blue-100 mb-4">Discover amazing destinations worldwide</p>
                <button onclick="showScreen('destinations-screen')" class="bg-white text-blue-600 px-6 py-3 rounded-full font-semibold hover:bg-blue-50 transition-colors">
                    Explore Now
                </button>
            </div>

            <!-- Quick Actions -->
            <div class="px-4 mb-6">
                <h3 class="text-lg font-bold text-gray-800 mb-3">Quick Actions</h3>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-2 gap-3 quick-actions-tablet">
                    <button onclick="showScreen('bookings-screen')" class="bg-white p-4 rounded-xl shadow-sm flex items-center space-x-3 card-hover">
                        <span class="text-2xl">✈️</span>
                        <div class="text-left">
                            <div class="font-semibold text-gray-800">Book Flight</div>
                            <div class="text-sm text-gray-500">Find best deals</div>
                        </div>
                    </button>
                    <button onclick="showScreen('passport-screen')" class="bg-white p-4 rounded-xl shadow-sm flex items-center space-x-3 card-hover">
                        <span class="text-2xl">🛂</span>
                        <div class="text-left">
                            <div class="font-semibold text-gray-800">Passport</div>
                            <div class="text-sm text-gray-500">Apply/Renew</div>
                        </div>
                    </button>
                </div>
            </div>

            <!-- Featured Destinations -->
            <div class="px-4 mb-6">
                <div class="flex items-center justify-between mb-3">
                    <h3 class="text-lg font-bold text-gray-800">Featured Destinations</h3>
                    <button onclick="showScreen('destinations-screen')" class="text-blue-600 text-sm font-semibold hover:text-blue-700">See All</button>
                </div>
                <div class="flex space-x-3 overflow-x-auto pb-2">
                    <div class="flex-shrink-0 w-48 md:w-56 bg-white rounded-xl shadow-sm overflow-hidden card-hover">
                        <div class="h-32 bg-gradient-to-br from-orange-400 to-red-500 flex items-center justify-center">
                            <div class="text-center text-white">
                                <div class="text-4xl mb-1">🏔️</div>
                                <div class="font-bold">Swiss Alps</div>
                            </div>
                        </div>
                        <div class="p-3">
                            <h4 class="font-semibold text-gray-800 mb-1">Majestic Mountains</h4>
                            <p class="text-xs text-gray-600">From ₦2,500,000</p>
                        </div>
                    </div>
                    
                    <div class="flex-shrink-0 w-48 md:w-56 bg-white rounded-xl shadow-sm overflow-hidden card-hover">
                        <div class="h-32 bg-gradient-to-br from-blue-400 to-teal-500 flex items-center justify-center">
                            <div class="text-center text-white">
                                <div class="text-4xl mb-1">🏝️</div>
                                <div class="font-bold">Maldives</div>
                            </div>
                        </div>
                        <div class="p-3">
                            <h4 class="font-semibold text-gray-800 mb-1">Tropical Paradise</h4>
                            <p class="text-xs text-gray-600">From ₦1,800,000</p>
                        </div>
                    </div>
                    
                    <div class="flex-shrink-0 w-48 md:w-56 bg-white rounded-xl shadow-sm overflow-hidden card-hover">
                        <div class="h-32 bg-gradient-to-br from-purple-400 to-pink-500 flex items-center justify-center">
                            <div class="text-center text-white">
                                <div class="text-4xl mb-1">🗾</div>
                                <div class="font-bold">Japan</div>
                            </div>
                        </div>
                        <div class="p-3">
                            <h4 class="font-semibold text-gray-800 mb-1">Cultural Wonder</h4>
                            <p class="text-xs text-gray-600">From ₦3,200,000</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Recent Activity -->
            <div class="px-4 mb-6">
                <h3 class="text-lg font-bold text-gray-800 mb-3">Recent Activity</h3>
                <div class="space-y-3">
                    <div class="bg-white p-4 rounded-xl shadow-sm flex items-center space-x-3 card-hover">
                        <div class="w-10 h-10 bg-green-100 rounded-full flex items-center justify-center">
                            <span class="text-green-600">✓</span>
                        </div>
                        <div class="flex-1">
                            <div class="font-semibold text-gray-800">Flight to Dubai booked</div>
                            <div class="text-sm text-gray-500">2 hours ago</div>
                        </div>
                    </div>
                    
                    <div class="bg-white p-4 rounded-xl shadow-sm flex items-center space-x-3 card-hover">
                        <div class="w-10 h-10 bg-blue-100 rounded-full flex items-center justify-center">
                            <span class="text-blue-600">📄</span>
                        </div>
                        <div class="flex-1">
                            <div class="font-semibold text-gray-800">Passport application submitted</div>
                            <div class="text-sm text-gray-500">1 day ago</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Social Media Quick Links -->
            <div class="px-4 mb-6">
                <h3 class="text-lg font-bold text-gray-800 mb-3">Follow Our Journey</h3>
                <div class="bg-white rounded-xl p-4 shadow-sm">
                    <div class="grid grid-cols-6 md:grid-cols-8 lg:grid-cols-6 gap-3 tablet-social-grid">
                        <a href="https://www.facebook.com/johnoyetravels" target="_blank" rel="noopener noreferrer" class="w-12 h-12 md:w-14 md:h-14 bg-blue-600 rounded-full flex items-center justify-center hover:bg-blue-700 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="white">
                                <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                            </svg>
                        </a>
                        
                        <a href="https://www.instagram.com/johnoyetravels" target="_blank" rel="noopener noreferrer" class="w-12 h-12 md:w-14 md:h-14 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full flex items-center justify-center hover:from-purple-600 hover:to-pink-600 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="white">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                        </a>
                        
                        <a href="https://twitter.com/johnoyetravels" target="_blank" rel="noopener noreferrer" class="w-12 h-12 md:w-14 md:h-14 bg-black rounded-full flex items-center justify-center hover:bg-gray-800 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="white">
                                <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
                            </svg>
                        </a>
                        
                        <a href="https://www.linkedin.com/company/johnoyetravels" target="_blank" rel="noopener noreferrer" class="w-12 h-12 md:w-14 md:h-14 bg-blue-700 rounded-full flex items-center justify-center hover:bg-blue-800 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="white">
                                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                            </svg>
                        </a>
                        
                        <a href="https://t.me/johnoyetravels" target="_blank" rel="noopener noreferrer" class="w-12 h-12 md:w-14 md:h-14 bg-blue-500 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="white">
                                <path d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.820 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"/>
                            </svg>
                        </a>
                        
                        <a href="https://www.tiktok.com/@johnoyetravels" target="_blank" rel="noopener noreferrer" class="w-12 h-12 md:w-14 md:h-14 bg-black rounded-full flex items-center justify-center hover:bg-gray-800 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="white">
                                <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/>
                            </svg>
                        </a>
                    </div>
                    <div class="mt-3 text-center">
                        <button onclick="showScreen('profile-screen')" class="text-blue-600 text-sm font-semibold hover:text-blue-700">View All Social Links →</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Destinations Screen -->
        <div id="destinations-screen" class="screen">
            <div class="app-header">
                <div class="flex items-center space-x-3">
                    <button onclick="showScreen('home-screen')" class="text-2xl hover:bg-gray-100 p-1 rounded">←</button>
                    <h1 class="text-lg font-bold text-gray-800">Destinations</h1>
                </div>
            </div>

            <!-- Search Bar -->
            <div class="p-4">
                <div class="relative">
                    <input type="text" placeholder="Search destinations..." class="w-full pl-10 pr-4 py-3 bg-white rounded-xl border border-gray-200 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <span class="absolute left-3 top-3 text-gray-400">🔍</span>
                </div>
            </div>

            <!-- Categories -->
            <div class="px-4 mb-4">
                <div class="flex space-x-2 overflow-x-auto pb-2">
                    <button class="flex-shrink-0 bg-blue-600 text-white px-4 py-2 rounded-full text-sm font-semibold hover:bg-blue-700">All</button>
                    <button class="flex-shrink-0 bg-gray-200 text-gray-700 px-4 py-2 rounded-full text-sm hover:bg-gray-300">Beach</button>
                    <button class="flex-shrink-0 bg-gray-200 text-gray-700 px-4 py-2 rounded-full text-sm hover:bg-gray-300">Mountain</button>
                    <button class="flex-shrink-0 bg-gray-200 text-gray-700 px-4 py-2 rounded-full text-sm hover:bg-gray-300">City</button>
                    <button class="flex-shrink-0 bg-gray-200 text-gray-700 px-4 py-2 rounded-full text-sm hover:bg-gray-300">Adventure</button>
                </div>
            </div>

            <!-- Destinations Grid -->
            <div class="px-4 space-y-4">
                <div class="swipe-card card-hover">
                    <div class="h-48 bg-gradient-to-br from-orange-400 to-red-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🏔️</div>
                            <h4 class="text-xl font-bold">Swiss Alps</h4>
                        </div>
                    </div>
                    <div class="p-4">
                        <h4 class="text-lg font-bold text-gray-800 mb-2">Majestic Mountains</h4>
                        <p class="text-gray-600 text-sm mb-3">Experience breathtaking views and pristine alpine landscapes in the heart of Switzerland.</p>
                        <div class="flex items-center justify-between">
                            <span class="text-lg font-bold text-green-600">From ₦2,500,000</span>
                            <button class="bg-blue-600 text-white px-4 py-2 rounded-lg text-sm font-semibold hover:bg-blue-700 transition-colors">Book Now</button>
                        </div>
                    </div>
                </div>

                <div class="swipe-card card-hover">
                    <div class="h-48 bg-gradient-to-br from-blue-400 to-teal-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🏝️</div>
                            <h4 class="text-xl font-bold">Maldives</h4>
                        </div>
                    </div>
                    <div class="p-4">
                        <h4 class="text-lg font-bold text-gray-800 mb-2">Tropical Paradise</h4>
                        <p class="text-gray-600 text-sm mb-3">Crystal clear waters and overwater bungalows in this Indian Ocean paradise.</p>
                        <div class="flex items-center justify-between">
                            <span class="text-lg font-bold text-green-600">From ₦1,800,000</span>
                            <button class="bg-blue-600 text-white px-4 py-2 rounded-lg text-sm font-semibold hover:bg-blue-700 transition-colors">Book Now</button>
                        </div>
                    </div>
                </div>

                <div class="swipe-card card-hover">
                    <div class="h-48 bg-gradient-to-br from-purple-400 to-pink-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🗾</div>
                            <h4 class="text-xl font-bold">Japan</h4>
                        </div>
                    </div>
                    <div class="p-4">
                        <h4 class="text-lg font-bold text-gray-800 mb-2">Cultural Wonder</h4>
                        <p class="text-gray-600 text-sm mb-3">Ancient traditions meet modern innovation in the Land of the Rising Sun.</p>
                        <div class="flex items-center justify-between">
                            <span class="text-lg font-bold text-green-600">From ₦3,200,000</span>
                            <button class="bg-blue-600 text-white px-4 py-2 rounded-lg text-sm font-semibold hover:bg-blue-700 transition-colors">Book Now</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Bookings Screen -->
        <div id="bookings-screen" class="screen">
            <div class="app-header">
                <div class="flex items-center space-x-3">
                    <button onclick="showScreen('home-screen')" class="text-2xl hover:bg-gray-100 p-1 rounded">←</button>
                    <h1 class="text-lg font-bold text-gray-800">Flight & Hotels</h1>
                </div>
            </div>

            <!-- Booking Tabs -->
            <div class="px-4 mb-4">
                <div class="flex bg-gray-100 rounded-xl p-1">
                    <button class="flex-1 bg-white text-blue-600 py-2 rounded-lg font-semibold text-sm shadow-sm">Flights</button>
                    <button class="flex-1 text-gray-600 py-2 rounded-lg font-semibold text-sm hover:bg-gray-50">Hotels</button>
                </div>
            </div>

            <!-- Flight Search Form -->
            <div class="px-4 mb-6">
                <div class="bg-white rounded-xl p-4 shadow-sm">
                    <div class="space-y-4">
                        <div class="flex items-center space-x-3">
                            <div class="flex-1">
                                <label class="block text-sm font-medium text-gray-700 mb-1">From</label>
                                <input type="text" placeholder="Lagos (LOS)" class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                            </div>
                            <button class="mt-6 text-blue-600 hover:text-blue-700">⇄</button>
                            <div class="flex-1">
                                <label class="block text-sm font-medium text-gray-700 mb-1">To</label>
                                <input type="text" placeholder="Dubai (DXB)" class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-2 gap-3">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-1">Departure</label>
                                <input type="date" class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-1">Return</label>
                                <input type="date" class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-2 gap-3">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-1">Passengers</label>
                                <select class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                                    <option>1 Passenger</option>
                                    <option>2 Passengers</option>
                                    <option>3 Passengers</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-1">Class</label>
                                <select class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                                    <option>Economy</option>
                                    <option>Business</option>
                                    <option>First</option>
                                </select>
                            </div>
                        </div>
                        
                        <button class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors">Search Flights</button>
                    </div>
                </div>
            </div>

            <!-- Popular Routes -->
            <div class="px-4">
                <h3 class="text-lg font-bold text-gray-800 mb-3">Popular Routes</h3>
                <div class="space-y-3">
                    <div class="bg-white p-4 rounded-xl shadow-sm card-hover">
                        <div class="flex items-center justify-between mb-2">
                            <div class="flex items-center space-x-3">
                                <div class="text-center">
                                    <div class="font-bold text-gray-800">LOS</div>
                                    <div class="text-xs text-gray-500">Lagos</div>
                                </div>
                                <span class="text-blue-500">✈️</span>
                                <div class="text-center">
                                    <div class="font-bold text-gray-800">DXB</div>
                                    <div class="text-xs text-gray-500">Dubai</div>
                                </div>
                            </div>
                            <div class="text-right">
                                <div class="font-bold text-green-600">₦450,000</div>
                                <div class="text-xs text-gray-500">Round trip</div>
                            </div>
                        </div>
                        <button class="w-full bg-blue-600 text-white py-2 rounded-lg text-sm font-semibold hover:bg-blue-700 transition-colors">Book Now</button>
                    </div>

                    <div class="bg-white p-4 rounded-xl shadow-sm card-hover">
                        <div class="flex items-center justify-between mb-2">
                            <div class="flex items-center space-x-3">
                                <div class="text-center">
                                    <div class="font-bold text-gray-800">LOS</div>
                                    <div class="text-xs text-gray-500">Lagos</div>
                                </div>
                                <span class="text-blue-500">✈️</span>
                                <div class="text-center">
                                    <div class="font-bold text-gray-800">LHR</div>
                                    <div class="text-xs text-gray-500">London</div>
                                </div>
                            </div>
                            <div class="text-right">
                                <div class="font-bold text-green-600">₦850,000</div>
                                <div class="text-xs text-gray-500">Round trip</div>
                            </div>
                        </div>
                        <button class="w-full bg-blue-600 text-white py-2 rounded-lg text-sm font-semibold hover:bg-blue-700 transition-colors">Book Now</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Passport Screen -->
        <div id="passport-screen" class="screen">
            <div class="app-header">
                <div class="flex items-center space-x-3">
                    <button onclick="showScreen('home-screen')" class="text-2xl hover:bg-gray-100 p-1 rounded">←</button>
                    <h1 class="text-lg font-bold text-gray-800">Passport Services</h1>
                </div>
            </div>

            <!-- Service Options -->
            <div class="px-4 mb-6">
                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-gradient-to-br from-green-500 to-emerald-600 p-4 rounded-xl text-white text-center card-hover">
                        <div class="text-3xl mb-2">📄</div>
                        <h4 class="font-bold mb-1">Fresh Application</h4>
                        <p class="text-xs opacity-90">New passport</p>
                    </div>
                    <div class="bg-gradient-to-br from-blue-500 to-indigo-600 p-4 rounded-xl text-white text-center card-hover">
                        <div class="text-3xl mb-2">🔄</div>
                        <h4 class="font-bold mb-1">Renewal</h4>
                        <p class="text-xs opacity-90">Renew existing</p>
                    </div>
                </div>
            </div>

            <!-- Process Steps -->
            <div class="px-4 mb-6">
                <h3 class="text-lg font-bold text-gray-800 mb-3">Simple Process</h3>
                <div class="space-y-3">
                    <div class="flex items-center space-x-3">
                        <div class="w-8 h-8 bg-blue-100 rounded-full flex items-center justify-center">
                            <span class="text-blue-600 font-bold text-sm">1</span>
                        </div>
                        <div>
                            <div class="font-semibold text-gray-800">Contact Us</div>
                            <div class="text-sm text-gray-500">Call or WhatsApp to start</div>
                        </div>
                    </div>
                    
                    <div class="flex items-center space-x-3">
                        <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center">
                            <span class="text-green-600 font-bold text-sm">2</span>
                        </div>
                        <div>
                            <div class="font-semibold text-gray-800">Document Review</div>
                            <div class="text-sm text-gray-500">We guide you through requirements</div>
                        </div>
                    </div>
                    
                    <div class="flex items-center space-x-3">
                        <div class="w-8 h-8 bg-purple-100 rounded-full flex items-center justify-center">
                            <span class="text-purple-600 font-bold text-sm">3</span>
                        </div>
                        <div>
                            <div class="font-semibold text-gray-800">Application Submit</div>
                            <div class="text-sm text-gray-500">We handle the submission</div>
                        </div>
                    </div>
                    
                    <div class="flex items-center space-x-3">
                        <div class="w-8 h-8 bg-orange-100 rounded-full flex items-center justify-center">
                            <span class="text-orange-600 font-bold text-sm">4</span>
                        </div>
                        <div>
                            <div class="font-semibold text-gray-800">Passport Ready</div>
                            <div class="text-sm text-gray-500">Collect your passport</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Quick Application -->
            <div class="px-4">
                <div class="bg-white rounded-xl p-4 shadow-sm">
                    <h4 class="font-bold text-gray-800 mb-3">Quick Application Form</h4>
                    <form onsubmit="handlePassportApplication(event)">
                        <div class="space-y-3">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-1">Full Name</label>
                                <input type="text" placeholder="Enter your full name" class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                            </div>
                            
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-1">Phone Number</label>
                                <input type="tel" placeholder="080XXXXXXXX" class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                            </div>
                            
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-1">Application Type</label>
                                <select class="w-full px-3 py-2 border border-gray-300 rounded-lg text-sm focus:ring-2 focus:ring-blue-500 focus:border-blue-500">
                                    <option>Fresh Application</option>
                                    <option>Renewal</option>
                                    <option>Correction</option>
                                </select>
                            </div>
                            
                            <button type="submit" class="w-full bg-green-600 text-white py-3 rounded-lg font-semibold hover:bg-green-700 transition-colors">Start Application</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>

        <!-- Profile Screen -->
        <div id="profile-screen" class="screen">
            <div class="app-header">
                <div class="flex items-center space-x-3">
                    <h1 class="text-lg font-bold text-gray-800">Profile</h1>
                </div>
            </div>

            <!-- Profile Header -->
            <div class="px-4 mb-6">
                <div class="bg-gradient-to-r from-blue-600 to-purple-600 rounded-xl p-6 text-white text-center">
                    <div class="w-20 h-20 bg-white bg-opacity-20 rounded-full mx-auto mb-3 flex items-center justify-center">
                        <span class="text-2xl">👤</span>
                    </div>
                    <h3 class="text-xl font-bold mb-1">Welcome Back!</h3>
                    <p class="text-blue-100">Traveler since 2024</p>
                </div>
            </div>

            <!-- Menu Items -->
            <div class="px-4 space-y-2">
                <button class="w-full bg-white p-4 rounded-xl shadow-sm flex items-center justify-between card-hover">
                    <div class="flex items-center space-x-3">
                        <span class="text-2xl">📋</span>
                        <span class="font-semibold text-gray-800">My Bookings</span>
                    </div>
                    <span class="text-gray-400">→</span>
                </button>
                
                <button class="w-full bg-white p-4 rounded-xl shadow-sm flex items-center justify-between card-hover">
                    <div class="flex items-center space-x-3">
                        <span class="text-2xl">🛂</span>
                        <span class="font-semibold text-gray-800">Passport Status</span>
                    </div>
                    <span class="text-gray-400">→</span>
                </button>
                
                <button class="w-full bg-white p-4 rounded-xl shadow-sm flex items-center justify-between card-hover">
                    <div class="flex items-center space-x-3">
                        <span class="text-2xl">💳</span>
                        <span class="font-semibold text-gray-800">Payment Methods</span>
                    </div>
                    <span class="text-gray-400">→</span>
                </button>
                
                <button class="w-full bg-white p-4 rounded-xl shadow-sm flex items-center justify-between card-hover">
                    <div class="flex items-center space-x-3">
                        <span class="text-2xl">🔔</span>
                        <span class="font-semibold text-gray-800">Notifications</span>
                    </div>
                    <span class="text-gray-400">→</span>
                </button>
                
                <button class="w-full bg-white p-4 rounded-xl shadow-sm flex items-center justify-between card-hover">
                    <div class="flex items-center space-x-3">
                        <span class="text-2xl">📞</span>
                        <span class="font-semibold text-gray-800">Contact Support</span>
                    </div>
                    <span class="text-gray-400">→</span>
                </button>
                
                <button class="w-full bg-white p-4 rounded-xl shadow-sm flex items-center justify-between card-hover">
                    <div class="flex items-center space-x-3">
                        <span class="text-2xl">ℹ️</span>
                        <span class="font-semibold text-gray-800">About</span>
                    </div>
                    <span class="text-gray-400">→</span>
                </button>
            </div>

            <!-- Contact Info -->
            <div class="px-4 mt-6">
                <div class="bg-white rounded-xl p-4 shadow-sm">
                    <h4 class="font-bold text-gray-800 mb-3">Contact Information</h4>
                    <div class="space-y-2 text-sm">
                        <div class="flex items-center space-x-2">
                            <span>📧</span>
                            <span class="text-gray-600">johnextry@gmail.com</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <span>📱</span>
                            <span class="text-gray-600">0806 348 3975</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <span>💬</span>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="text-green-600 hover:text-green-700">WhatsApp Group</a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Social Media Links -->
            <div class="px-4 mt-4">
                <div class="bg-white rounded-xl p-4 shadow-sm">
                    <h4 class="font-bold text-gray-800 mb-3">Follow Our Journey</h4>
                    <div class="grid grid-cols-3 md:grid-cols-4 lg:grid-cols-3 gap-3 tablet-grid">
                        <a href="https://www.facebook.com/johnoyetravels" target="_blank" rel="noopener noreferrer" class="bg-blue-600 hover:bg-blue-700 text-white p-3 rounded-lg flex flex-col items-center space-y-1 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                            </svg>
                            <span class="text-xs font-semibold">Facebook</span>
                        </a>
                        
                        <a href="https://www.instagram.com/johnoyetravels" target="_blank" rel="noopener noreferrer" class="bg-gradient-to-r from-purple-500 to-pink-500 hover:from-purple-600 hover:to-pink-600 text-white p-3 rounded-lg flex flex-col items-center space-y-1 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                            <span class="text-xs font-semibold">Instagram</span>
                        </a>
                        
                        <a href="https://twitter.com/johnoyetravels" target="_blank" rel="noopener noreferrer" class="bg-black hover:bg-gray-800 text-white p-3 rounded-lg flex flex-col items-center space-y-1 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
                            </svg>
                            <span class="text-xs font-semibold">Twitter</span>
                        </a>
                        
                        <a href="https://www.linkedin.com/company/johnoyetravels" target="_blank" rel="noopener noreferrer" class="bg-blue-700 hover:bg-blue-800 text-white p-3 rounded-lg flex flex-col items-center space-y-1 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                            </svg>
                            <span class="text-xs font-semibold">LinkedIn</span>
                        </a>
                        
                        <a href="https://t.me/johnoyetravels" target="_blank" rel="noopener noreferrer" class="bg-blue-500 hover:bg-blue-600 text-white p-3 rounded-lg flex flex-col items-center space-y-1 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.820 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"/>
                            </svg>
                            <span class="text-xs font-semibold">Telegram</span>
                        </a>
                        
                        <a href="https://www.tiktok.com/@johnoyetravels" target="_blank" rel="noopener noreferrer" class="bg-black hover:bg-gray-800 text-white p-3 rounded-lg flex flex-col items-center space-y-1 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/>
                            </svg>
                            <span class="text-xs font-semibold">TikTok</span>
                        </a>
                    </div>
                    
                    <div class="mt-3">
                        <a href="https://www.threads.net/@johnoyetravels" target="_blank" rel="noopener noreferrer" class="w-full bg-black hover:bg-gray-800 text-white p-3 rounded-lg flex items-center justify-center space-x-2 transition-colors">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M12.186 24h-.007c-3.581-.024-6.334-1.205-8.184-3.509C2.35 18.44 1.5 15.586 1.472 12.01v-.017c.03-3.579.879-6.43 2.525-8.482C5.845 1.205 8.6.024 12.18 0h.014c2.746.02 5.043.725 6.826 2.098 1.677 1.29 2.858 3.13 3.509 5.467l-2.04.569c-1.104-3.96-3.898-5.984-8.304-6.015-2.91.022-5.11.936-6.54 2.717C4.307 6.504 3.616 8.914 3.589 12c.027 3.086.718 5.496 2.057 7.164 1.43 1.781 3.631 2.695 6.54 2.717 2.623-.02 4.358-.631 5.8-2.045 1.647-1.613 1.618-3.593 1.09-4.798-.31-.71-.873-1.3-1.634-1.75-.192 1.352-.622 2.446-1.284 3.272-.886 1.102-2.14 1.704-3.73 1.79-1.202.065-2.361-.218-3.259-.801-1.063-.689-1.685-1.74-1.752-2.964-.065-1.19.408-2.285 1.33-3.082.88-.76 2.119-1.207 3.583-1.291a13.853 13.853 0 0 1 3.02.142c-.126-.742-.375-1.332-.74-1.755-.365-.424-.84-.636-1.414-.636-.861 0-1.436.357-1.711.746-.3.424-.455.973-.463 1.64h-2.149c.01-1.283.339-2.394 1.005-3.301C7.87 2.402 9.168 1.938 10.96 1.938c1.353 0 2.531.35 3.505 1.042.928.659 1.58 1.61 1.94 2.834.359 1.22.359 2.669.359 4.32v.04c3.02.26 5.255 1.789 5.255 4.508 0 1.401-.604 2.654-1.736 3.505-1.235.929-2.905 1.387-4.969 1.387-1.705 0-3.207-.339-4.467-1.007-1.269-.673-2.264-1.659-2.957-2.93-.347-.636-.608-1.314-.777-2.019h2.240c.104.411.263.794.475 1.146.477.793 1.181 1.29 2.09 1.477.455.094.949.094 1.404 0 .91-.187 1.614-.684 2.09-1.477.239-.397.398-.84.475-1.326-.476-.039-.953-.098-1.429-.176-1.553-.254-2.97-.67-4.22-1.236-.628-.284-1.207-.634-1.732-1.045-.525-.411-.94-.882-1.24-1.413-.3-.531-.45-1.123-.45-1.776 0-1.061.45-1.983 1.35-2.766.9-.783 2.115-1.175 3.645-1.175 1.53 0 2.745.392 3.645 1.175.9.783 1.35 1.705 1.35 2.766v.04c0 .411-.075.822-.225 1.233.15.411.225.822.225 1.233v.04c0 1.061-.45 1.983-1.35 2.766-.9.783-2.115 1.175-3.645 1.175z"/>
                            </svg>
                            <span class="font-semibold">Threads</span>
                        </a>
                    </div>
                    
                    <p class="text-xs text-gray-500 text-center mt-3">Follow us for travel tips, destination updates & exclusive deals!</p>
                </div>
            </div>
        </div>

        <!-- Floating WhatsApp Button -->
        <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="floating-action hover:bg-green-600 transition-colors">
            <span class="text-2xl">💬</span>
        </a>

        <!-- Bottom Navigation -->
        <div class="bottom-nav">
            <div class="flex justify-around">
                <a href="#" onclick="showScreen('home-screen')" class="nav-item active">
                    <span class="text-xl mb-1">🏠</span>
                    <span class="text-xs">Home</span>
                </a>
                <a href="#" onclick="showScreen('destinations-screen')" class="nav-item">
                    <span class="text-xl mb-1">🌍</span>
                    <span class="text-xs">Explore</span>
                </a>
                <a href="#" onclick="showScreen('bookings-screen')" class="nav-item">
                    <span class="text-xl mb-1">✈️</span>
                    <span class="text-xs">Book</span>
                </a>
                <a href="#" onclick="showScreen('passport-screen')" class="nav-item">
                    <span class="text-xl mb-1">🛂</span>
                    <span class="text-xs">Passport</span>
                </a>
                <a href="#" onclick="showScreen('profile-screen')" class="nav-item">
                    <span class="text-xl mb-1">👤</span>
                    <span class="text-xs">Profile</span>
                </a>
            </div>
        </div>
    </div>

    <script>
        function showScreen(screenId) {
            // Hide all screens
            const screens = document.querySelectorAll('.screen');
            screens.forEach(screen => screen.classList.remove('active'));
            
            // Show selected screen
            document.getElementById(screenId).classList.add('active');
            
            // Update navigation
            const navItems = document.querySelectorAll('.nav-item');
            navItems.forEach(item => item.classList.remove('active'));
            
            // Add active class to corresponding nav item
            const navMap = {
                'home-screen': 0,
                'destinations-screen': 1,
                'bookings-screen': 2,
                'passport-screen': 3,
                'profile-screen': 4
            };
            
            if (navMap[screenId] !== undefined) {
                navItems[navMap[screenId]].classList.add('active');
            }
            
            // Scroll to top
            window.scrollTo(0, 0);
        }

        // Handle form submissions
        function handleFlightSearch(event) {
            event.preventDefault();
            showNotification('Searching for flights...', 'info');
        }

        function handlePassportApplication(event) {
            event.preventDefault();
            showNotification('Application submitted successfully!', 'success');
        }

        function showNotification(message, type) {
            // Create notification element
            const notification = document.createElement('div');
            notification.className = `fixed top-20 left-4 right-4 p-4 rounded-lg text-white z-50 ${
                type === 'success' ? 'bg-green-500' : 
                type === 'error' ? 'bg-red-500' : 'bg-blue-500'
            }`;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            // Remove after 3 seconds
            setTimeout(() => {
                notification.remove();
            }, 3000);
        }

        // Add touch gestures for mobile feel
        let startY = 0;
        let currentY = 0;
        let pullDistance = 0;

        document.addEventListener('touchstart', (e) => {
            startY = e.touches[0].clientY;
        });

        document.addEventListener('touchmove', (e) => {
            currentY = e.touches[0].clientY;
            pullDistance = currentY - startY;
            
            if (pullDistance > 0 && window.scrollY === 0) {
                // Pull to refresh logic
                const pullToRefresh = document.querySelector('.pull-to-refresh');
                if (pullToRefresh && pullDistance > 100) {
                    pullToRefresh.innerHTML = '<div class="text-2xl mb-2">↻</div><p class="text-sm">Release to refresh</p>';
                }
            }
        });

        document.addEventListener('touchend', (e) => {
            if (pullDistance > 100 && window.scrollY === 0) {
                showNotification('Refreshing content...', 'info');
                // Reset pull to refresh
                setTimeout(() => {
                    const pullToRefresh = document.querySelector('.pull-to-refresh');
                    if (pullToRefresh) {
                        pullToRefresh.innerHTML = '<div class="text-2xl mb-2">⬇️</div><p class="text-sm">Pull to refresh</p>';
                    }
                }, 1000);
            }
            pullDistance = 0;
        });

        // Initialize app
        document.addEventListener('DOMContentLoaded', () => {
            showScreen('home-screen');
        });

        // Detect device type and adjust layout
        function detectDevice() {
            const userAgent = navigator.userAgent;
            const isTablet = /iPad|Android(?!.*Mobile)|Tablet/i.test(userAgent);
            const isMobile = /iPhone|Android.*Mobile|BlackBerry|Opera Mini|IEMobile/i.test(userAgent);
            const isDesktop = !isMobile && !isTablet;
            
            document.body.classList.toggle('is-desktop', isDesktop);
            document.body.classList.toggle('is-tablet', isTablet);
            document.body.classList.toggle('is-mobile', isMobile);
        }

        // Call on load
        detectDevice();
        
        // Handle orientation changes
        window.addEventListener('orientationchange', () => {
            setTimeout(() => {
                detectDevice();
            }, 100);
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'98f0c0500464d06b',t:'MTc2MDU0NjM1Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>

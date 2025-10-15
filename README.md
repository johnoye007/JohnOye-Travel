<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>John Oye's Travels - Discover Amazing Destinations</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            box-sizing: border-box;
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        
        .card-hover {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }
        
        .parallax {
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }
    </style>
</head>
<body class="font-sans">
    <!-- Navigation -->
    <nav class="bg-white shadow-lg fixed w-full z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center">
                    <div class="mr-3">
                        <svg width="40" height="40" viewBox="0 0 40 40" class="text-blue-600">
                            <!-- Globe background -->
                            <circle cx="20" cy="20" r="18" fill="currentColor" opacity="0.1"/>
                            <circle cx="20" cy="20" r="18" fill="none" stroke="currentColor" stroke-width="2"/>
                            
                            <!-- Airplane -->
                            <path d="M12 20 L28 20 M20 12 L28 20 L20 28" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
                            
                            <!-- Globe lines -->
                            <path d="M2 20 L38 20" stroke="currentColor" stroke-width="1" opacity="0.6"/>
                            <path d="M20 2 Q20 20 20 38" fill="none" stroke="currentColor" stroke-width="1" opacity="0.6"/>
                            <path d="M20 2 Q30 20 20 38" fill="none" stroke="currentColor" stroke-width="1" opacity="0.6"/>
                            <path d="M20 2 Q10 20 20 38" fill="none" stroke="currentColor" stroke-width="1" opacity="0.6"/>
                        </svg>
                    </div>
                    <h1 class="text-2xl font-bold text-gray-800">John Oye's Travels</h1>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-8">
                        <a href="#home" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Home</a>
                        <a href="#destinations" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Destinations</a>
                        <a href="#bookings" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Flight & Hotels</a>
                        <a href="#passport" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Passport</a>
                        <a href="#stress-free" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Stress-Free Services</a>
                        <a href="#payment" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Payment</a>
                        <a href="#about" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">About</a>
                        <a href="#contact" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Contact</a>
                        <a href="#disclaimer" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">Terms</a>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-gradient h-full flex items-center justify-center text-white pt-16">
        <div class="text-center px-4 py-20">
            <h2 class="text-5xl md:text-7xl font-bold mb-6">Explore the World</h2>
            <p class="text-xl md:text-2xl mb-8 max-w-3xl mx-auto">Join John Oye on incredible journeys to breathtaking destinations around the globe. Adventure awaits!</p>
            <button onclick="scrollToSection('destinations')" class="bg-white text-blue-600 px-8 py-4 rounded-full text-lg font-semibold hover:bg-gray-100 transition-colors shadow-lg">
                Start Your Journey
            </button>
        </div>
    </section>

    <!-- Destinations Section -->
    <section id="destinations" class="py-20 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h3 class="text-4xl font-bold text-gray-800 mb-4">Featured Destinations</h3>
                <p class="text-xl text-gray-600 max-w-2xl mx-auto">Discover amazing places through John's eyes and experiences</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Destination Card 1 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-48 bg-gradient-to-br from-orange-400 to-red-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🏔️</div>
                            <h4 class="text-xl font-bold">Swiss Alps</h4>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-xl font-bold text-gray-800 mb-2">Majestic Mountains</h4>
                        <p class="text-gray-600 mb-4">Experience breathtaking views and pristine alpine landscapes in the heart of Switzerland.</p>
                        <button onclick="showDestinationDetails('Swiss Alps')" class="text-blue-600 font-semibold hover:text-blue-800 transition-colors">
                            Learn More →
                        </button>
                    </div>
                </div>

                <!-- Destination Card 2 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-48 bg-gradient-to-br from-blue-400 to-teal-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🏝️</div>
                            <h4 class="text-xl font-bold">Maldives</h4>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-xl font-bold text-gray-800 mb-2">Tropical Paradise</h4>
                        <p class="text-gray-600 mb-4">Crystal clear waters and overwater bungalows in this Indian Ocean paradise.</p>
                        <button onclick="showDestinationDetails('Maldives')" class="text-blue-600 font-semibold hover:text-blue-800 transition-colors">
                            Learn More →
                        </button>
                    </div>
                </div>

                <!-- Destination Card 3 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-48 bg-gradient-to-br from-purple-400 to-pink-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🗾</div>
                            <h4 class="text-xl font-bold">Japan</h4>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-xl font-bold text-gray-800 mb-2">Cultural Wonder</h4>
                        <p class="text-gray-600 mb-4">Ancient traditions meet modern innovation in the Land of the Rising Sun.</p>
                        <button onclick="showDestinationDetails('Japan')" class="text-blue-600 font-semibold hover:text-blue-800 transition-colors">
                            Learn More →
                        </button>
                    </div>
                </div>

                <!-- Destination Card 4 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-48 bg-gradient-to-br from-green-400 to-blue-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🦁</div>
                            <h4 class="text-xl font-bold">Kenya Safari</h4>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-xl font-bold text-gray-800 mb-2">Wildlife Adventure</h4>
                        <p class="text-gray-600 mb-4">Witness the Great Migration and incredible wildlife in their natural habitat.</p>
                        <button onclick="showDestinationDetails('Kenya Safari')" class="text-blue-600 font-semibold hover:text-blue-800 transition-colors">
                            Learn More →
                        </button>
                    </div>
                </div>

                <!-- Destination Card 5 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-48 bg-gradient-to-br from-yellow-400 to-orange-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🏛️</div>
                            <h4 class="text-xl font-bold">Greece</h4>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-xl font-bold text-gray-800 mb-2">Ancient History</h4>
                        <p class="text-gray-600 mb-4">Explore ancient ruins and stunning islands in the cradle of civilization.</p>
                        <button onclick="showDestinationDetails('Greece')" class="text-blue-600 font-semibold hover:text-blue-800 transition-colors">
                            Learn More →
                        </button>
                    </div>
                </div>

                <!-- Destination Card 6 -->
                <div class="bg-white rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-48 bg-gradient-to-br from-red-400 to-pink-500 flex items-center justify-center">
                        <div class="text-center text-white">
                            <div class="text-6xl mb-2">🌸</div>
                            <h4 class="text-xl font-bold">Peru</h4>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-xl font-bold text-gray-800 mb-2">Mystical Journey</h4>
                        <p class="text-gray-600 mb-4">Trek to Machu Picchu and discover the mysteries of the Inca civilization.</p>
                        <button onclick="showDestinationDetails('Peru')" class="text-blue-600 font-semibold hover:text-blue-800 transition-colors">
                            Learn More →
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Flight & Hotel Bookings Section -->
    <section id="bookings" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Header -->
            <div class="text-center mb-16">
                <div class="flex justify-center items-center space-x-4 mb-6">
                    <div class="text-6xl">✈️</div>
                    <div class="text-6xl">🏨</div>
                </div>
                <h3 class="text-4xl md:text-5xl font-bold text-gray-800 mb-6">Flight & Hotel Bookings</h3>
                <p class="text-xl text-gray-600 max-w-4xl mx-auto leading-relaxed">
                    Get the best deals on flights and accommodations worldwide. We handle everything from budget-friendly options to luxury experiences.
                </p>
            </div>

            <!-- Services Overview -->
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
                <!-- Flight Bookings -->
                <div class="bg-gradient-to-br from-blue-500 to-indigo-600 rounded-2xl p-8 text-white">
                    <div class="text-center mb-8">
                        <div class="text-8xl mb-4">✈️</div>
                        <h4 class="text-3xl font-bold mb-4">Flight Bookings</h4>
                        <p class="text-blue-100 text-lg">Domestic and international flights at competitive prices</p>
                    </div>
                    
                    <div class="space-y-4 mb-8">
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">🌍</div>
                            <span class="text-lg">Worldwide destinations</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">💰</div>
                            <span class="text-lg">Best price guarantee</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">🎫</div>
                            <span class="text-lg">All major airlines</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">📱</div>
                            <span class="text-lg">24/7 booking support</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">🔄</div>
                            <span class="text-lg">Flexible booking options</span>
                        </div>
                    </div>

                    <button onclick="openFlightBooking()" class="w-full bg-white text-blue-600 py-3 rounded-lg font-bold text-lg hover:bg-gray-100 transition-colors">
                        Book Flights Now
                    </button>
                </div>

                <!-- Hotel Bookings -->
                <div class="bg-gradient-to-br from-purple-500 to-pink-600 rounded-2xl p-8 text-white">
                    <div class="text-center mb-8">
                        <div class="text-8xl mb-4">🏨</div>
                        <h4 class="text-3xl font-bold mb-4">Hotel Bookings</h4>
                        <p class="text-purple-100 text-lg">From budget stays to luxury resorts worldwide</p>
                    </div>
                    
                    <div class="space-y-4 mb-8">
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">🏆</div>
                            <span class="text-lg">Luxury to budget options</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">⭐</div>
                            <span class="text-lg">Verified reviews & ratings</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">🎯</div>
                            <span class="text-lg">Prime locations</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">🛡️</div>
                            <span class="text-lg">Secure reservations</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">💳</div>
                            <span class="text-lg">Flexible payment plans</span>
                        </div>
                    </div>

                    <button onclick="openHotelBooking()" class="w-full bg-white text-purple-600 py-3 rounded-lg font-bold text-lg hover:bg-gray-100 transition-colors">
                        Book Hotels Now
                    </button>
                </div>
            </div>

            <!-- Popular Routes & Destinations -->
            <div class="mb-16">
                <h4 class="text-3xl font-bold text-gray-800 text-center mb-12">Popular Flight Routes</h4>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Lagos to Dubai -->
                    <div class="bg-white rounded-xl shadow-lg p-6 border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="flex items-center justify-between mb-4">
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">LOS</div>
                                <div class="text-sm text-gray-600">Lagos</div>
                            </div>
                            <div class="text-3xl text-blue-500">✈️</div>
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">DXB</div>
                                <div class="text-sm text-gray-600">Dubai</div>
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-green-600 mb-2">From ₦450,000</div>
                            <div class="text-sm text-gray-600 mb-4">Round trip • Economy</div>
                            <button onclick="bookRoute('LOS-DXB')" class="w-full bg-blue-600 text-white py-2 rounded-lg hover:bg-blue-700 transition-colors">
                                Book Now
                            </button>
                        </div>
                    </div>

                    <!-- Lagos to London -->
                    <div class="bg-white rounded-xl shadow-lg p-6 border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="flex items-center justify-between mb-4">
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">LOS</div>
                                <div class="text-sm text-gray-600">Lagos</div>
                            </div>
                            <div class="text-3xl text-blue-500">✈️</div>
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">LHR</div>
                                <div class="text-sm text-gray-600">London</div>
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-green-600 mb-2">From ₦850,000</div>
                            <div class="text-sm text-gray-600 mb-4">Round trip • Economy</div>
                            <button onclick="bookRoute('LOS-LHR')" class="w-full bg-blue-600 text-white py-2 rounded-lg hover:bg-blue-700 transition-colors">
                                Book Now
                            </button>
                        </div>
                    </div>

                    <!-- Lagos to New York -->
                    <div class="bg-white rounded-xl shadow-lg p-6 border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="flex items-center justify-between mb-4">
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">LOS</div>
                                <div class="text-sm text-gray-600">Lagos</div>
                            </div>
                            <div class="text-3xl text-blue-500">✈️</div>
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">JFK</div>
                                <div class="text-sm text-gray-600">New York</div>
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-green-600 mb-2">From ₦1,200,000</div>
                            <div class="text-sm text-gray-600 mb-4">Round trip • Economy</div>
                            <button onclick="bookRoute('LOS-JFK')" class="w-full bg-blue-600 text-white py-2 rounded-lg hover:bg-blue-700 transition-colors">
                                Book Now
                            </button>
                        </div>
                    </div>

                    <!-- Abuja to Paris -->
                    <div class="bg-white rounded-xl shadow-lg p-6 border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="flex items-center justify-between mb-4">
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">ABV</div>
                                <div class="text-sm text-gray-600">Abuja</div>
                            </div>
                            <div class="text-3xl text-blue-500">✈️</div>
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">CDG</div>
                                <div class="text-sm text-gray-600">Paris</div>
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-green-600 mb-2">From ₦780,000</div>
                            <div class="text-sm text-gray-600 mb-4">Round trip • Economy</div>
                            <button onclick="bookRoute('ABV-CDG')" class="w-full bg-blue-600 text-white py-2 rounded-lg hover:bg-blue-700 transition-colors">
                                Book Now
                            </button>
                        </div>
                    </div>

                    <!-- Lagos to Toronto -->
                    <div class="bg-white rounded-xl shadow-lg p-6 border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="flex items-center justify-between mb-4">
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">LOS</div>
                                <div class="text-sm text-gray-600">Lagos</div>
                            </div>
                            <div class="text-3xl text-blue-500">✈️</div>
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">YYZ</div>
                                <div class="text-sm text-gray-600">Toronto</div>
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-green-600 mb-2">From ₦950,000</div>
                            <div class="text-sm text-gray-600 mb-4">Round trip • Economy</div>
                            <button onclick="bookRoute('LOS-YYZ')" class="w-full bg-blue-600 text-white py-2 rounded-lg hover:bg-blue-700 transition-colors">
                                Book Now
                            </button>
                        </div>
                    </div>

                    <!-- Lagos to Istanbul -->
                    <div class="bg-white rounded-xl shadow-lg p-6 border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="flex items-center justify-between mb-4">
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">LOS</div>
                                <div class="text-sm text-gray-600">Lagos</div>
                            </div>
                            <div class="text-3xl text-blue-500">✈️</div>
                            <div class="text-center">
                                <div class="text-2xl font-bold text-gray-800">IST</div>
                                <div class="text-sm text-gray-600">Istanbul</div>
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-2xl font-bold text-green-600 mb-2">From ₦520,000</div>
                            <div class="text-sm text-gray-600 mb-4">Round trip • Economy</div>
                            <button onclick="bookRoute('LOS-IST')" class="w-full bg-blue-600 text-white py-2 rounded-lg hover:bg-blue-700 transition-colors">
                                Book Now
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Featured Hotels -->
            <div class="mb-16">
                <h4 class="text-3xl font-bold text-gray-800 text-center mb-12">Featured Hotel Destinations</h4>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <!-- Dubai Hotels -->
                    <div class="bg-gradient-to-br from-yellow-400 to-orange-500 rounded-xl p-6 text-white text-center hover:scale-105 transition-transform duration-300">
                        <div class="text-5xl mb-4">🏙️</div>
                        <h5 class="text-xl font-bold mb-2">Dubai</h5>
                        <p class="text-sm opacity-90 mb-4">Luxury hotels & resorts</p>
                        <div class="text-lg font-bold mb-4">From ₦45,000/night</div>
                        <button onclick="searchHotels('Dubai')" class="bg-white text-orange-600 px-4 py-2 rounded-lg font-semibold hover:bg-gray-100 transition-colors">
                            View Hotels
                        </button>
                    </div>

                    <!-- London Hotels -->
                    <div class="bg-gradient-to-br from-red-500 to-pink-600 rounded-xl p-6 text-white text-center hover:scale-105 transition-transform duration-300">
                        <div class="text-5xl mb-4">🏰</div>
                        <h5 class="text-xl font-bold mb-2">London</h5>
                        <p class="text-sm opacity-90 mb-4">Historic & modern stays</p>
                        <div class="text-lg font-bold mb-4">From ₦65,000/night</div>
                        <button onclick="searchHotels('London')" class="bg-white text-pink-600 px-4 py-2 rounded-lg font-semibold hover:bg-gray-100 transition-colors">
                            View Hotels
                        </button>
                    </div>

                    <!-- Paris Hotels -->
                    <div class="bg-gradient-to-br from-purple-500 to-indigo-600 rounded-xl p-6 text-white text-center hover:scale-105 transition-transform duration-300">
                        <div class="text-5xl mb-4">🗼</div>
                        <h5 class="text-xl font-bold mb-2">Paris</h5>
                        <p class="text-sm opacity-90 mb-4">Romantic boutique hotels</p>
                        <div class="text-lg font-bold mb-4">From ₦55,000/night</div>
                        <button onclick="searchHotels('Paris')" class="bg-white text-indigo-600 px-4 py-2 rounded-lg font-semibold hover:bg-gray-100 transition-colors">
                            View Hotels
                        </button>
                    </div>

                    <!-- New York Hotels -->
                    <div class="bg-gradient-to-br from-blue-500 to-teal-600 rounded-xl p-6 text-white text-center hover:scale-105 transition-transform duration-300">
                        <div class="text-5xl mb-4">🗽</div>
                        <h5 class="text-xl font-bold mb-2">New York</h5>
                        <p class="text-sm opacity-90 mb-4">Manhattan & Brooklyn</p>
                        <div class="text-lg font-bold mb-4">From ₦85,000/night</div>
                        <button onclick="searchHotels('New York')" class="bg-white text-teal-600 px-4 py-2 rounded-lg font-semibold hover:bg-gray-100 transition-colors">
                            View Hotels
                        </button>
                    </div>
                </div>
            </div>

            <!-- Booking Benefits -->
            <div class="bg-gradient-to-r from-green-600 to-blue-600 rounded-2xl p-8 text-white mb-16">
                <div class="text-center mb-8">
                    <div class="text-6xl mb-4">🎯</div>
                    <h4 class="text-3xl font-bold mb-4">Why Book With Us?</h4>
                    <p class="text-xl opacity-90">Experience the difference of personalized travel service</p>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                    <div class="bg-white bg-opacity-20 rounded-lg p-4 text-center">
                        <div class="text-4xl mb-3">💰</div>
                        <h5 class="font-bold text-lg mb-2">Best Prices</h5>
                        <p class="text-sm opacity-90">Competitive rates with price match guarantee</p>
                    </div>
                    <div class="bg-white bg-opacity-20 rounded-lg p-4 text-center">
                        <div class="text-4xl mb-3">🛡️</div>
                        <h5 class="font-bold text-lg mb-2">Secure Booking</h5>
                        <p class="text-sm opacity-90">Safe and encrypted payment processing</p>
                    </div>
                    <div class="bg-white bg-opacity-20 rounded-lg p-4 text-center">
                        <div class="text-4xl mb-3">📞</div>
                        <h5 class="font-bold text-lg mb-2">24/7 Support</h5>
                        <p class="text-sm opacity-90">Round-the-clock customer assistance</p>
                    </div>
                    <div class="bg-white bg-opacity-20 rounded-lg p-4 text-center">
                        <div class="text-4xl mb-3">🎁</div>
                        <h5 class="font-bold text-lg mb-2">Extra Perks</h5>
                        <p class="text-sm opacity-90">Exclusive deals and loyalty rewards</p>
                    </div>
                </div>
            </div>

            <!-- Quick Booking Forms -->
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
                <!-- Flight Search Form -->
                <div class="bg-white rounded-xl shadow-lg p-8 border-2 border-blue-200">
                    <div class="text-center mb-6">
                        <div class="text-4xl mb-2">✈️</div>
                        <h4 class="text-2xl font-bold text-gray-800">Quick Flight Search</h4>
                        <p class="text-gray-600">Find and compare flight prices instantly</p>
                    </div>
                    
                    <form onsubmit="handleFlightSearch(event)" class="space-y-4">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">From</label>
                                <input type="text" placeholder="Lagos (LOS)" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">To</label>
                                <input type="text" placeholder="Dubai (DXB)" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Departure Date</label>
                                <input type="date" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Return Date</label>
                                <input type="date" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Passengers</label>
                                <select class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                                    <option value="1">1 Passenger</option>
                                    <option value="2">2 Passengers</option>
                                    <option value="3">3 Passengers</option>
                                    <option value="4">4+ Passengers</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Class</label>
                                <select class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                                    <option value="economy">Economy</option>
                                    <option value="business">Business</option>
                                    <option value="first">First Class</option>
                                </select>
                            </div>
                        </div>
                        
                        <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white py-3 rounded-lg font-semibold transition-colors">
                            Search Flights
                        </button>
                    </form>
                </div>

                <!-- Hotel Search Form -->
                <div class="bg-white rounded-xl shadow-lg p-8 border-2 border-purple-200">
                    <div class="text-center mb-6">
                        <div class="text-4xl mb-2">🏨</div>
                        <h4 class="text-2xl font-bold text-gray-800">Quick Hotel Search</h4>
                        <p class="text-gray-600">Find perfect accommodations for your stay</p>
                    </div>
                    
                    <form onsubmit="handleHotelSearch(event)" class="space-y-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Destination</label>
                            <input type="text" placeholder="Dubai, UAE" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent">
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Check-in Date</label>
                                <input type="date" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Check-out Date</label>
                                <input type="date" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent">
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Guests</label>
                                <select class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent">
                                    <option value="1">1 Guest</option>
                                    <option value="2">2 Guests</option>
                                    <option value="3">3 Guests</option>
                                    <option value="4">4+ Guests</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Rooms</label>
                                <select class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent">
                                    <option value="1">1 Room</option>
                                    <option value="2">2 Rooms</option>
                                    <option value="3">3 Rooms</option>
                                    <option value="4">4+ Rooms</option>
                                </select>
                            </div>
                        </div>
                        
                        <button type="submit" class="w-full bg-purple-600 hover:bg-purple-700 text-white py-3 rounded-lg font-semibold transition-colors">
                            Search Hotels
                        </button>
                    </form>
                </div>
            </div>

            <!-- Contact for Bookings -->
            <div class="text-center">
                <h4 class="text-3xl font-bold text-gray-800 mb-6">Ready to Book Your Trip?</h4>
                <p class="text-xl text-gray-600 mb-8">Contact our travel experts for personalized assistance and exclusive deals</p>
                
                <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                    <a href="tel:08063483975" class="bg-blue-600 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-blue-700 transition-colors shadow-lg flex items-center space-x-2">
                        <span>📞</span>
                        <span>Call for Bookings</span>
                    </a>
                    <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-green-500 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-green-600 transition-colors shadow-lg flex items-center space-x-2">
                        <span>💬</span>
                        <span>WhatsApp Us</span>
                    </a>
                    <a href="mailto:johnextry@gmail.com" class="bg-gray-600 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-gray-700 transition-colors shadow-lg flex items-center space-x-2">
                        <span>📧</span>
                        <span>Email Us</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Passport Services Section -->
    <section id="passport" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <div class="text-8xl mb-6">🛂</div>
                <h3 class="text-4xl md:text-5xl font-bold text-gray-800 mb-6">Need an International Passport?</h3>
                <h4 class="text-2xl md:text-3xl font-semibold text-blue-600 mb-8">Let's Make It Effortless.</h4>
                <p class="text-xl text-gray-600 max-w-4xl mx-auto leading-relaxed">
                    Whether it's for travel, study, business, or relocation—your passport is your global access key. 
                    Don't wait in endless queues or deal with confusing processes.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center mb-16">
                <div class="space-y-8">
                    <div class="flex items-start space-x-4">
                        <div class="text-3xl">✅</div>
                        <div>
                            <h4 class="text-xl font-bold text-gray-800 mb-2">Fresh Passport Application</h4>
                            <p class="text-gray-600">Complete assistance for first-time passport applicants with all required documentation and guidance.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start space-x-4">
                        <div class="text-3xl">✅</div>
                        <div>
                            <h4 class="text-xl font-bold text-gray-800 mb-2">Renewals & Data Corrections</h4>
                            <p class="text-gray-600">Hassle-free passport renewals and corrections for expired or damaged passports.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start space-x-4">
                        <div class="text-3xl">✅</div>
                        <div>
                            <h4 class="text-xl font-bold text-gray-800 mb-2">Fast-Track & VIP Processing Available</h4>
                            <p class="text-gray-600">Expedited services for urgent travel needs with priority processing options.</p>
                        </div>
                    </div>
                </div>

                <div class="bg-gradient-to-br from-green-400 to-blue-500 rounded-2xl p-8 text-white text-center">
                    <div class="text-6xl mb-6">🌍</div>
                    <h4 class="text-2xl font-bold mb-4">Why Choose Us?</h4>
                    <div class="space-y-4 text-left">
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">🔒</div>
                            <span class="text-lg">Seamless Process</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">👁️</div>
                            <span class="text-lg">Transparent Pricing</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">⭐</div>
                            <span class="text-lg">Reliable Service</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="text-2xl">⚡</div>
                            <span class="text-lg">Fast Processing</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Call to Action -->
            <div class="bg-gradient-to-r from-blue-600 to-purple-600 rounded-2xl p-8 text-white text-center mb-16">
                <h4 class="text-3xl font-bold mb-4">Contact us today for your international passport, get your passport with ease now!!!</h4>
                <p class="text-xl mb-6 opacity-90">Your Destination Awaits. Let's Get You Ready.</p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                    <a href="tel:08063483975" class="bg-white text-blue-600 px-8 py-4 rounded-full text-lg font-semibold hover:bg-gray-100 transition-colors shadow-lg flex items-center space-x-2">
                        <span>📞</span>
                        <span>Call 08063483975</span>
                    </a>
                    <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-green-500 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-green-600 transition-colors shadow-lg flex items-center space-x-2">
                        <span>💬</span>
                        <span>Chat on WhatsApp</span>
                    </a>
                </div>
                <p class="text-sm mt-4 opacity-75">#TravelReady #PassportDoneRight #NoBordersJustBeginnings</p>
            </div>

            <!-- Passport Options -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
                <!-- Passport Types -->
                <div class="bg-white rounded-xl shadow-lg p-6 border-l-4 border-blue-500">
                    <h5 class="text-xl font-bold text-gray-800 mb-4">📄 Passport Types</h5>
                    <ul class="space-y-2 text-gray-600">
                        <li>• 32 PAGES</li>
                        <li>• 64 PAGES</li>
                    </ul>
                </div>

                <!-- Validity Options -->
                <div class="bg-white rounded-xl shadow-lg p-6 border-l-4 border-green-500">
                    <h5 class="text-xl font-bold text-gray-800 mb-4">⏰ Validity Period</h5>
                    <ul class="space-y-2 text-gray-600">
                        <li>• 5 YEARS</li>
                        <li>• 10 YEARS</li>
                    </ul>
                </div>

                <!-- Processing Speed -->
                <div class="bg-white rounded-xl shadow-lg p-6 border-l-4 border-purple-500">
                    <h5 class="text-xl font-bold text-gray-800 mb-4">⚡ Processing Speed</h5>
                    <ul class="space-y-2 text-gray-600">
                        <li>• NORMAL</li>
                        <li>• FAST TRACK (2-3 days)</li>
                    </ul>
                </div>

                <!-- Special Services -->
                <div class="bg-white rounded-xl shadow-lg p-6 border-l-4 border-orange-500 md:col-span-2 lg:col-span-3">
                    <h5 class="text-xl font-bold text-gray-800 mb-4">🔧 Special Services Available</h5>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <ul class="space-y-2 text-gray-600">
                            <li>• NAME CHANGE (marriage)</li>
                            <li>• AGE CORRECTION</li>
                        </ul>
                        <ul class="space-y-2 text-gray-600">
                            <li>• NAME CORRECTION</li>
                            <li>• ETC</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Application Form -->
            <div class="bg-white rounded-xl shadow-lg p-8 mb-16">
                <h4 class="text-3xl font-bold text-gray-800 text-center mb-8">International Passport Requirements</h4>
                <p class="text-lg text-gray-600 text-center mb-8">Fill the following information and return to us</p>

                <form onsubmit="handlePassportForm(event)" class="space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- Application Type -->
                        <div class="md:col-span-2">
                            <label class="block text-sm font-medium text-gray-700 mb-2">Application Type</label>
                            <div class="flex space-x-4">
                                <label class="flex items-center">
                                    <input type="radio" name="applicationType" value="FRESH" class="mr-2">
                                    <span>FRESH</span>
                                </label>
                                <label class="flex items-center">
                                    <input type="radio" name="applicationType" value="RE-ISSUE" class="mr-2">
                                    <span>RE-ISSUE</span>
                                </label>
                            </div>
                        </div>

                        <!-- Personal Information -->
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Title</label>
                            <select class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                                <option value="">Select Title</option>
                                <option value="Mr">Mr</option>
                                <option value="Mrs">Mrs</option>
                                <option value="Miss">Miss</option>
                                <option value="Dr">Dr</option>
                                <option value="Prof">Prof</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Surname</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">First Name</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Middle Name</label>
                            <input type="text" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Sex</label>
                            <select required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                                <option value="">Select Sex</option>
                                <option value="Male">Male</option>
                                <option value="Female">Female</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Date of Birth</label>
                            <input type="date" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">NIN</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Place of Birth</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div class="md:col-span-2">
                            <label class="block text-sm font-medium text-gray-700 mb-2">Residential Address</label>
                            <textarea rows="2" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"></textarea>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">City</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">State</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">LGA</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">State of Origin</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">LGA (Origin)</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Home Town</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Nationality</label>
                            <input type="text" value="Nigerian" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Occupation</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Maiden Name</label>
                            <input type="text" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Marital Status</label>
                            <select required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                                <option value="">Select Status</option>
                                <option value="Single">Single</option>
                                <option value="Married">Married</option>
                                <option value="Divorced">Divorced</option>
                                <option value="Widowed">Widowed</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Mobile Phone</label>
                            <input type="tel" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Email Address</label>
                            <input type="email" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Height</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Colour of Eyes</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Colour of Hair</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <!-- Next of Kin Information -->
                        <div class="md:col-span-2">
                            <h5 class="text-lg font-semibold text-gray-800 mb-4 mt-6">Next of Kin Information</h5>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Next of Kin Name</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Relationship</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div class="md:col-span-2">
                            <label class="block text-sm font-medium text-gray-700 mb-2">Next of Kin Address</label>
                            <textarea rows="2" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"></textarea>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">City</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">State</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">LGA</label>
                            <input type="text" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Phone Number</label>
                            <input type="tel" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                        </div>
                    </div>

                    <div class="text-center">
                        <button type="submit" class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-3 rounded-lg font-semibold transition-colors">
                            Submit Application
                        </button>
                    </div>
                </form>
            </div>

            <!-- Required Documents -->
            <div class="bg-yellow-50 border-l-4 border-yellow-400 rounded-r-xl p-8 mb-16">
                <h4 class="text-2xl font-bold text-gray-800 mb-6">📋 Additional Required Scan Documents</h4>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <h5 class="text-lg font-semibold text-gray-800 mb-3">Required Documents:</h5>
                        <ul class="space-y-2 text-gray-700">
                            <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> NIN slip</li>
                            <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Birth certificate</li>
                            <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Passport photograph</li>
                        </ul>
                    </div>
                    <div>
                        <h5 class="text-lg font-semibold text-gray-800 mb-3">Origin Certificate (Choose One):</h5>
                        <ul class="space-y-2 text-gray-700">
                            <li class="flex items-center"><span class="text-blue-500 mr-2">•</span> State of origin certificate</li>
                            <li class="text-center text-gray-500 my-2">OR</li>
                            <li class="flex items-center"><span class="text-blue-500 mr-2">•</span> Local Government identification certificate</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Process Steps -->
            <div class="mt-16">
                <h4 class="text-3xl font-bold text-gray-800 text-center mb-12">Simple 4-Step Process</h4>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="text-center">
                        <div class="bg-blue-100 rounded-full w-16 h-16 flex items-center justify-center mx-auto mb-4">
                            <span class="text-2xl font-bold text-blue-600">1</span>
                        </div>
                        <h5 class="text-lg font-semibold text-gray-800 mb-2">Contact Us</h5>
                        <p class="text-gray-600">Reach out via phone or WhatsApp to discuss your passport needs</p>
                    </div>
                    
                    <div class="text-center">
                        <div class="bg-green-100 rounded-full w-16 h-16 flex items-center justify-center mx-auto mb-4">
                            <span class="text-2xl font-bold text-green-600">2</span>
                        </div>
                        <h5 class="text-lg font-semibold text-gray-800 mb-2">Document Review</h5>
                        <p class="text-gray-600">We'll guide you through required documents and help with preparation</p>
                    </div>
                    
                    <div class="text-center">
                        <div class="bg-purple-100 rounded-full w-16 h-16 flex items-center justify-center mx-auto mb-4">
                            <span class="text-2xl font-bold text-purple-600">3</span>
                        </div>
                        <h5 class="text-lg font-semibold text-gray-800 mb-2">Application Submit</h5>
                        <p class="text-gray-600">We handle the submission process and track your application</p>
                    </div>
                    
                    <div class="text-center">
                        <div class="bg-orange-100 rounded-full w-16 h-16 flex items-center justify-center mx-auto mb-4">
                            <span class="text-2xl font-bold text-orange-600">4</span>
                        </div>
                        <h5 class="text-lg font-semibold text-gray-800 mb-2">Passport Ready</h5>
                        <p class="text-gray-600">Collect your passport and start planning your next adventure!</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stress-Free Passport Services Section -->
    <section id="stress-free" class="py-20 bg-gradient-to-br from-blue-600 to-purple-700 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <div class="text-8xl mb-6">🛂</div>
                <h3 class="text-4xl md:text-6xl font-bold mb-6">STRESS-FREE PASSPORT APPLICATION & RENEWAL</h3>
                <h4 class="text-2xl md:text-3xl font-semibold mb-8 text-blue-200">LET US HANDLE IT!</h4>
                <div class="flex items-center justify-center space-x-4 mb-8">
                    <div class="bg-white text-blue-600 px-6 py-3 rounded-full font-bold text-lg">
                        💯 Training Is Also Available ✔️
                    </div>
                </div>
                <p class="text-xl md:text-2xl max-w-4xl mx-auto leading-relaxed opacity-90">
                    Need to apply or renew your passport? Skip the hassle! We manage everything—
                </p>
            </div>

            <!-- Services Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16">
                <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-xl p-6 text-center hover:bg-opacity-20 transition-all duration-300">
                    <div class="text-5xl mb-4">📝</div>
                    <h4 class="text-xl font-bold mb-2">1. Applications</h4>
                    <p class="text-blue-100">Complete passport application processing from start to finish</p>
                </div>

                <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-xl p-6 text-center hover:bg-opacity-20 transition-all duration-300">
                    <div class="text-5xl mb-4">📅</div>
                    <h4 class="text-xl font-bold mb-2">2. Appointments</h4>
                    <p class="text-blue-100">Booking & rescheduling appointments hassle-free</p>
                </div>

                <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-xl p-6 text-center hover:bg-opacity-20 transition-all duration-300">
                    <div class="text-5xl mb-4">✈️</div>
                    <h4 class="text-xl font-bold mb-2">3. Flight Bookings</h4>
                    <p class="text-blue-100">Complete travel arrangements and flight reservations</p>
                </div>

                <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-xl p-6 text-center hover:bg-opacity-20 transition-all duration-300">
                    <div class="text-5xl mb-4">✏️</div>
                    <h4 class="text-xl font-bold mb-2">4. Corrections</h4>
                    <p class="text-blue-100">Corrections on your International Passport data</p>
                </div>
            </div>

            <!-- Benefits Section -->
            <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-2xl p-8 mb-16">
                <h4 class="text-3xl font-bold text-center mb-8">Why Choose Our Stress-Free Service?</h4>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="text-center">
                        <div class="text-6xl mb-4">⏰</div>
                        <h5 class="text-xl font-bold mb-2">Save Time</h5>
                        <p class="text-blue-100">No more wasting hours in long queues or dealing with bureaucracy</p>
                    </div>
                    <div class="text-center">
                        <div class="text-6xl mb-4">💪</div>
                        <h5 class="text-xl font-bold mb-2">Save Energy</h5>
                        <p class="text-blue-100">Let our experts handle all the paperwork and processes</p>
                    </div>
                    <div class="text-center">
                        <div class="text-6xl mb-4">😌</div>
                        <h5 class="text-xl font-bold mb-2">Avoid Stress</h5>
                        <p class="text-blue-100">Sit back, relax, and let us manage everything for you</p>
                    </div>
                </div>
            </div>

            <!-- Training Section -->
            <div class="bg-gradient-to-r from-green-500 to-teal-600 rounded-2xl p-8 mb-16">
                <div class="text-center">
                    <div class="text-6xl mb-4">🎓</div>
                    <h4 class="text-3xl font-bold mb-4">Professional Training Available</h4>
                    <p class="text-xl mb-6 opacity-90">
                        Want to learn the passport application process yourself? We offer comprehensive training programs for individuals and organizations.
                    </p>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-4xl mx-auto">
                        <div class="bg-white bg-opacity-20 rounded-lg p-4">
                            <h5 class="font-bold text-lg mb-2">Individual Training</h5>
                            <p class="text-sm opacity-90">Learn the complete process step-by-step</p>
                        </div>
                        <div class="bg-white bg-opacity-20 rounded-lg p-4">
                            <h5 class="font-bold text-lg mb-2">Corporate Training</h5>
                            <p class="text-sm opacity-90">Train your team to handle passport services</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Call to Action -->
            <div class="text-center">
                <h4 class="text-3xl md:text-4xl font-bold mb-6">Save time, energy, and avoid long queues.</h4>
                <p class="text-xl md:text-2xl mb-8 opacity-90">Sit back, relax, and let us save you the stress. Contact us now for a smooth process!</p>
                
                <div class="flex flex-col sm:flex-row gap-6 justify-center items-center">
                    <a href="tel:08061697503" class="bg-white text-blue-600 px-8 py-4 rounded-full text-xl font-bold hover:bg-gray-100 transition-colors shadow-lg flex items-center space-x-3">
                        <span>📞</span>
                        <span>CALL: 08061697503</span>
                    </a>
                    <a href="https://wa.me/2348061697503" target="_blank" rel="noopener noreferrer" class="bg-green-500 text-white px-8 py-4 rounded-full text-xl font-bold hover:bg-green-600 transition-colors shadow-lg flex items-center space-x-3">
                        <span>💬</span>
                        <span>WHATSAPP: 08061697503</span>
                    </a>
                </div>
                
                <p class="text-lg mt-6 opacity-75 italic">Your passport journey starts with just one call!</p>
            </div>

            <!-- Process Steps -->
            <div class="mt-20">
                <h4 class="text-3xl font-bold text-center mb-12">Our Simple 3-Step Process</h4>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="text-center">
                        <div class="bg-white bg-opacity-20 rounded-full w-20 h-20 flex items-center justify-center mx-auto mb-6">
                            <span class="text-3xl font-bold">1</span>
                        </div>
                        <h5 class="text-xl font-bold mb-3">Contact Us</h5>
                        <p class="text-blue-100">Call or WhatsApp us with your passport needs</p>
                    </div>
                    
                    <div class="text-center">
                        <div class="bg-white bg-opacity-20 rounded-full w-20 h-20 flex items-center justify-center mx-auto mb-6">
                            <span class="text-3xl font-bold">2</span>
                        </div>
                        <h5 class="text-xl font-bold mb-3">We Handle Everything</h5>
                        <p class="text-blue-100">Sit back while we manage all processes and paperwork</p>
                    </div>
                    
                    <div class="text-center">
                        <div class="bg-white bg-opacity-20 rounded-full w-20 h-20 flex items-center justify-center mx-auto mb-6">
                            <span class="text-3xl font-bold">3</span>
                        </div>
                        <h5 class="text-xl font-bold mb-3">Get Your Passport</h5>
                        <p class="text-blue-100">Receive your passport without any stress or delays</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Payment Section -->
    <section id="payment" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <div class="text-8xl mb-6">💳</div>
                <h3 class="text-4xl md:text-5xl font-bold text-gray-800 mb-6">Travel Payment Options</h3>
                <p class="text-xl text-gray-600 max-w-4xl mx-auto leading-relaxed">
                    Flexible payment plans and secure booking options to make your dream trip affordable and accessible.
                </p>
            </div>

            <!-- Payment Plans -->
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-16">
                <!-- Full Payment -->
                <div class="bg-gradient-to-br from-green-500 to-emerald-600 rounded-2xl p-8 text-white text-center transform hover:scale-105 transition-transform duration-300">
                    <div class="text-6xl mb-4">💰</div>
                    <h4 class="text-2xl font-bold mb-4">Full Payment</h4>
                    <div class="text-4xl font-bold mb-2">Save 10%</div>
                    <p class="text-green-100 mb-6">Pay in full and get instant discount on all travel packages</p>
                    <ul class="text-left space-y-2 mb-6">
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> 10% discount on total cost</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Priority booking</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Free travel insurance</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Flexible date changes</li>
                    </ul>
                    <button onclick="selectPaymentPlan('full')" class="bg-white text-green-600 px-6 py-3 rounded-full font-bold hover:bg-gray-100 transition-colors">
                        Choose Full Payment
                    </button>
                </div>

                <!-- Installment Plan -->
                <div class="bg-gradient-to-br from-blue-500 to-indigo-600 rounded-2xl p-8 text-white text-center transform hover:scale-105 transition-transform duration-300 border-4 border-yellow-400">
                    <div class="bg-yellow-400 text-blue-600 px-4 py-1 rounded-full text-sm font-bold mb-4">MOST POPULAR</div>
                    <div class="text-6xl mb-4">📅</div>
                    <h4 class="text-2xl font-bold mb-4">Installment Plan</h4>
                    <div class="text-4xl font-bold mb-2">3-6 Months</div>
                    <p class="text-blue-100 mb-6">Spread your payments over 3-6 months with flexible terms</p>
                    <ul class="text-left space-y-2 mb-6">
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> 30% deposit to start</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Monthly installments</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> No hidden charges</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Secure payment plan</li>
                    </ul>
                    <button onclick="selectPaymentPlan('installment')" class="bg-white text-blue-600 px-6 py-3 rounded-full font-bold hover:bg-gray-100 transition-colors">
                        Choose Installments
                    </button>
                </div>

                <!-- Group Booking -->
                <div class="bg-gradient-to-br from-purple-500 to-pink-600 rounded-2xl p-8 text-white text-center transform hover:scale-105 transition-transform duration-300">
                    <div class="text-6xl mb-4">👥</div>
                    <h4 class="text-2xl font-bold mb-4">Group Booking</h4>
                    <div class="text-4xl font-bold mb-2">Save 15%</div>
                    <p class="text-purple-100 mb-6">Special rates for groups of 5 or more travelers</p>
                    <ul class="text-left space-y-2 mb-6">
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> 15% group discount</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Dedicated group coordinator</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Custom itinerary</li>
                        <li class="flex items-center"><span class="text-2xl mr-2">✓</span> Group activities included</li>
                    </ul>
                    <button onclick="selectPaymentPlan('group')" class="bg-white text-purple-600 px-6 py-3 rounded-full font-bold hover:bg-gray-100 transition-colors">
                        Book for Group
                    </button>
                </div>
            </div>

            <!-- Payment Methods -->
            <div class="bg-gray-50 rounded-2xl p-8 mb-16">
                <h4 class="text-3xl font-bold text-gray-800 text-center mb-8">Accepted Payment Methods</h4>
                
                <!-- Bank Details Section -->
                <div class="bg-gradient-to-r from-green-600 to-blue-600 rounded-xl p-6 mb-8 text-white text-center">
                    <div class="text-4xl mb-4">🏦</div>
                    <h5 class="text-2xl font-bold mb-4">Primary Bank Account</h5>
                    <div class="bg-white bg-opacity-20 rounded-lg p-4 max-w-md mx-auto">
                        <div class="space-y-2 text-lg">
                            <div><strong>Account Name:</strong> John Oyedele O.</div>
                            <div><strong>Bank:</strong> Access Bank PLC</div>
                            <div><strong>Account Number:</strong> <span class="text-2xl font-bold">0030456086</span></div>
                        </div>
                    </div>
                    <p class="text-sm opacity-90 mt-4">Send payment confirmation via WhatsApp after transfer</p>
                </div>

                <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6">
                    <div class="bg-white rounded-lg p-4 text-center shadow-md">
                        <div class="text-3xl mb-2">🏦</div>
                        <div class="text-sm font-semibold">Bank Transfer</div>
                    </div>
                    <div class="bg-white rounded-lg p-4 text-center shadow-md">
                        <div class="text-3xl mb-2">💳</div>
                        <div class="text-sm font-semibold">Debit Cards</div>
                    </div>
                    <div class="bg-white rounded-lg p-4 text-center shadow-md">
                        <div class="text-3xl mb-2">💰</div>
                        <div class="text-sm font-semibold">Cash Payment</div>
                    </div>
                    <div class="bg-white rounded-lg p-4 text-center shadow-md">
                        <div class="text-3xl mb-2">📱</div>
                        <div class="text-sm font-semibold">Mobile Money</div>
                    </div>
                    <div class="bg-white rounded-lg p-4 text-center shadow-md">
                        <div class="text-3xl mb-2">🌐</div>
                        <div class="text-sm font-semibold">Online Banking</div>
                    </div>
                    <div class="bg-white rounded-lg p-4 text-center shadow-md">
                        <div class="text-3xl mb-2">💸</div>
                        <div class="text-sm font-semibold">Cryptocurrency</div>
                    </div>
                </div>
            </div>

            <!-- Sample Pricing -->
            <div class="mb-16">
                <h4 class="text-3xl font-bold text-gray-800 text-center mb-12">Sample Travel Packages & Pricing</h4>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Europe Package -->
                    <div class="bg-white rounded-xl shadow-lg overflow-hidden border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="bg-gradient-to-r from-blue-500 to-purple-600 p-6 text-white">
                            <div class="text-4xl mb-2">🇪🇺</div>
                            <h5 class="text-xl font-bold">Europe Explorer</h5>
                            <p class="text-blue-100">7 Days • 3 Countries</p>
                        </div>
                        <div class="p-6">
                            <div class="text-3xl font-bold text-gray-800 mb-4">₦2,500,000</div>
                            <ul class="space-y-2 text-gray-600 mb-6">
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Flights included</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> 4-star hotels</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Guided tours</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Visa assistance</li>
                            </ul>
                            <div class="text-sm text-gray-500 mb-4">
                                <div>Full Payment: ₦2,250,000 (Save ₦250,000)</div>
                                <div>Installment: ₦750,000 deposit + 3 monthly payments</div>
                            </div>
                            <button onclick="bookPackage('europe')" class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors">
                                Book Europe Package
                            </button>
                        </div>
                    </div>

                    <!-- Dubai Package -->
                    <div class="bg-white rounded-xl shadow-lg overflow-hidden border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="bg-gradient-to-r from-yellow-500 to-orange-600 p-6 text-white">
                            <div class="text-4xl mb-2">🇦🇪</div>
                            <h5 class="text-xl font-bold">Dubai Luxury</h5>
                            <p class="text-yellow-100">5 Days • Premium Experience</p>
                        </div>
                        <div class="p-6">
                            <div class="text-3xl font-bold text-gray-800 mb-4">₦1,800,000</div>
                            <ul class="space-y-2 text-gray-600 mb-6">
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Emirates flights</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> 5-star hotels</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Desert safari</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> City tours</li>
                            </ul>
                            <div class="text-sm text-gray-500 mb-4">
                                <div>Full Payment: ₦1,620,000 (Save ₦180,000)</div>
                                <div>Installment: ₦540,000 deposit + 3 monthly payments</div>
                            </div>
                            <button onclick="bookPackage('dubai')" class="w-full bg-orange-600 text-white py-3 rounded-lg font-semibold hover:bg-orange-700 transition-colors">
                                Book Dubai Package
                            </button>
                        </div>
                    </div>

                    <!-- USA Package -->
                    <div class="bg-white rounded-xl shadow-lg overflow-hidden border-2 border-gray-200 hover:border-blue-500 transition-colors">
                        <div class="bg-gradient-to-r from-red-500 to-blue-600 p-6 text-white">
                            <div class="text-4xl mb-2">🇺🇸</div>
                            <h5 class="text-xl font-bold">USA Adventure</h5>
                            <p class="text-red-100">10 Days • Coast to Coast</p>
                        </div>
                        <div class="p-6">
                            <div class="text-3xl font-bold text-gray-800 mb-4">₦4,200,000</div>
                            <ul class="space-y-2 text-gray-600 mb-6">
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Direct flights</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Premium hotels</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Multiple cities</li>
                                <li class="flex items-center"><span class="text-green-500 mr-2">✓</span> Visa support</li>
                            </ul>
                            <div class="text-sm text-gray-500 mb-4">
                                <div>Full Payment: ₦3,780,000 (Save ₦420,000)</div>
                                <div>Installment: ₦1,260,000 deposit + 6 monthly payments</div>
                            </div>
                            <button onclick="bookPackage('usa')" class="w-full bg-red-600 text-white py-3 rounded-lg font-semibold hover:bg-red-700 transition-colors">
                                Book USA Package
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Payment Security -->
            <div class="bg-gradient-to-r from-green-600 to-teal-600 rounded-2xl p-8 text-white text-center mb-16">
                <div class="text-6xl mb-4">🔒</div>
                <h4 class="text-3xl font-bold mb-4">Secure Payment Guarantee</h4>
                <p class="text-xl mb-6 opacity-90">Your payments are protected with bank-level security and full transparency</p>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="bg-white bg-opacity-20 rounded-lg p-4">
                        <div class="text-3xl mb-2">🛡️</div>
                        <h5 class="font-bold mb-2">Secure Transactions</h5>
                        <p class="text-sm opacity-90">All payments encrypted and protected</p>
                    </div>
                    <div class="bg-white bg-opacity-20 rounded-lg p-4">
                        <div class="text-3xl mb-2">📋</div>
                        <h5 class="font-bold mb-2">Clear Receipts</h5>
                        <p class="text-sm opacity-90">Detailed payment records provided</p>
                    </div>
                    <div class="bg-white bg-opacity-20 rounded-lg p-4">
                        <div class="text-3xl mb-2">💯</div>
                        <h5 class="font-bold mb-2">Money-Back Policy</h5>
                        <p class="text-sm opacity-90">Refund policy for cancellations</p>
                    </div>
                </div>
            </div>

            <!-- Contact for Payment -->
            <div class="text-center">
                <h4 class="text-3xl font-bold text-gray-800 mb-6">Ready to Book Your Dream Trip?</h4>
                <p class="text-xl text-gray-600 mb-8">Contact us to discuss payment options and customize your travel package</p>
                
                <!-- QR Code Section -->
                <div class="bg-white rounded-2xl shadow-lg p-8 max-w-md mx-auto mb-8">
                    <h5 class="text-xl font-bold text-gray-800 mb-4">Quick Access - Scan QR Code</h5>
                    <div class="bg-gray-100 p-4 rounded-lg mb-4">
                        <svg width="200" height="200" viewBox="0 0 200 200" class="mx-auto">
                            <!-- QR Code Pattern -->
                            <rect width="200" height="200" fill="white"/>
                            <!-- Corner squares -->
                            <rect x="10" y="10" width="50" height="50" fill="black"/>
                            <rect x="20" y="20" width="30" height="30" fill="white"/>
                            <rect x="25" y="25" width="20" height="20" fill="black"/>
                            
                            <rect x="140" y="10" width="50" height="50" fill="black"/>
                            <rect x="150" y="20" width="30" height="30" fill="white"/>
                            <rect x="155" y="25" width="20" height="20" fill="black"/>
                            
                            <rect x="10" y="140" width="50" height="50" fill="black"/>
                            <rect x="20" y="150" width="30" height="30" fill="white"/>
                            <rect x="25" y="155" width="20" height="20" fill="black"/>
                            
                            <!-- Timing patterns -->
                            <rect x="70" y="10" width="10" height="10" fill="black"/>
                            <rect x="90" y="10" width="10" height="10" fill="black"/>
                            <rect x="110" y="10" width="10" height="10" fill="black"/>
                            <rect x="130" y="10" width="10" height="10" fill="black"/>
                            
                            <rect x="10" y="70" width="10" height="10" fill="black"/>
                            <rect x="10" y="90" width="10" height="10" fill="black"/>
                            <rect x="10" y="110" width="10" height="10" fill="black"/>
                            <rect x="10" y="130" width="10" height="10" fill="black"/>
                            
                            <!-- Data pattern -->
                            <rect x="30" y="70" width="10" height="10" fill="black"/>
                            <rect x="50" y="70" width="10" height="10" fill="black"/>
                            <rect x="70" y="70" width="10" height="10" fill="black"/>
                            <rect x="90" y="70" width="10" height="10" fill="black"/>
                            <rect x="110" y="70" width="10" height="10" fill="black"/>
                            <rect x="130" y="70" width="10" height="10" fill="black"/>
                            <rect x="150" y="70" width="10" height="10" fill="black"/>
                            <rect x="170" y="70" width="10" height="10" fill="black"/>
                            
                            <rect x="70" y="30" width="10" height="10" fill="black"/>
                            <rect x="70" y="50" width="10" height="10" fill="black"/>
                            <rect x="70" y="90" width="10" height="10" fill="black"/>
                            <rect x="70" y="110" width="10" height="10" fill="black"/>
                            <rect x="70" y="130" width="10" height="10" fill="black"/>
                            <rect x="70" y="150" width="10" height="10" fill="black"/>
                            <rect x="70" y="170" width="10" height="10" fill="black"/>
                            
                            <!-- More data patterns -->
                            <rect x="90" y="90" width="10" height="10" fill="black"/>
                            <rect x="110" y="90" width="10" height="10" fill="black"/>
                            <rect x="130" y="90" width="10" height="10" fill="black"/>
                            <rect x="150" y="90" width="10" height="10" fill="black"/>
                            <rect x="170" y="90" width="10" height="10" fill="black"/>
                            
                            <rect x="90" y="110" width="10" height="10" fill="black"/>
                            <rect x="110" y="110" width="10" height="10" fill="black"/>
                            <rect x="130" y="110" width="10" height="10" fill="black"/>
                            <rect x="150" y="110" width="10" height="10" fill="black"/>
                            <rect x="170" y="110" width="10" height="10" fill="black"/>
                            
                            <rect x="90" y="130" width="10" height="10" fill="black"/>
                            <rect x="110" y="130" width="10" height="10" fill="black"/>
                            <rect x="130" y="130" width="10" height="10" fill="black"/>
                            <rect x="150" y="130" width="10" height="10" fill="black"/>
                            <rect x="170" y="130" width="10" height="10" fill="black"/>
                            
                            <rect x="90" y="150" width="10" height="10" fill="black"/>
                            <rect x="110" y="150" width="10" height="10" fill="black"/>
                            <rect x="130" y="150" width="10" height="10" fill="black"/>
                            <rect x="150" y="150" width="10" height="10" fill="black"/>
                            <rect x="170" y="150" width="10" height="10" fill="black"/>
                            
                            <rect x="90" y="170" width="10" height="10" fill="black"/>
                            <rect x="110" y="170" width="10" height="10" fill="black"/>
                            <rect x="130" y="170" width="10" height="10" fill="black"/>
                            <rect x="150" y="170" width="10" height="10" fill="black"/>
                            <rect x="170" y="170" width="10" height="10" fill="black"/>
                            
                            <!-- Additional patterns -->
                            <rect x="30" y="90" width="10" height="10" fill="black"/>
                            <rect x="50" y="90" width="10" height="10" fill="black"/>
                            <rect x="30" y="110" width="10" height="10" fill="black"/>
                            <rect x="50" y="110" width="10" height="10" fill="black"/>
                            <rect x="30" y="130" width="10" height="10" fill="black"/>
                            <rect x="50" y="130" width="10" height="10" fill="black"/>
                            <rect x="30" y="150" width="10" height="10" fill="black"/>
                            <rect x="50" y="150" width="10" height="10" fill="black"/>
                            <rect x="30" y="170" width="10" height="10" fill="black"/>
                            <rect x="50" y="170" width="10" height="10" fill="black"/>
                        </svg>
                    </div>
                    <p class="text-sm text-gray-600 mb-4">Scan to join our WhatsApp travel group instantly!</p>
                    <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="text-green-600 hover:text-green-700 font-semibold text-sm">
                        Or click here to join →
                    </a>
                </div>
                
                <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                    <a href="tel:08063483975" class="bg-blue-600 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-blue-700 transition-colors shadow-lg flex items-center space-x-2">
                        <span>📞</span>
                        <span>Call for Payment Plans</span>
                    </a>
                    <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-green-500 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-green-600 transition-colors shadow-lg flex items-center space-x-2">
                        <span>💬</span>
                        <span>WhatsApp for Booking</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Company Background -->
            <div class="text-center mb-16">
                <h3 class="text-4xl font-bold text-gray-800 mb-8">About John Oye's Travel</h3>
                <div class="bg-white rounded-xl shadow-lg p-8 max-w-4xl mx-auto">
                    <div class="text-6xl mb-6">🏢</div>
                    <p class="text-lg text-gray-600 leading-relaxed mb-6">
                        <strong>John Oye's Travel</strong> is a subsidiary of <strong>Johnmich Resource Services</strong>, an arm of service created from <strong>John Extry Foundation</strong> which was established in 2016 by <strong>John Oyedele Oluwaseun</strong>, popularly known as <strong>John Oye</strong> or <strong>Johnextry</strong> as he preferred to be called.
                    </p>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
                        <div class="text-center p-4 bg-blue-50 rounded-lg">
                            <div class="text-3xl mb-2">🌟</div>
                            <h4 class="font-bold text-gray-800">John Extry Foundation</h4>
                            <p class="text-sm text-gray-600">Est. 2016</p>
                        </div>
                        <div class="text-center p-4 bg-green-50 rounded-lg">
                            <div class="text-3xl mb-2">🏗️</div>
                            <h4 class="font-bold text-gray-800">Johnmich Resource Services</h4>
                            <p class="text-sm text-gray-600">Parent Company</p>
                        </div>
                        <div class="text-center p-4 bg-purple-50 rounded-lg">
                            <div class="text-3xl mb-2">✈️</div>
                            <h4 class="font-bold text-gray-800">John Oye's Travel</h4>
                            <p class="text-sm text-gray-600">Travel Division</p>
                        </div>
                    </div>
                </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <h3 class="text-4xl font-bold text-gray-800 mb-6">Meet John Oye</h3>
                    <p class="text-lg text-gray-600 mb-6">
                        With over 15 years of travel experience and visits to more than 80 countries, John Oye is passionate about sharing the beauty and wonder of our world. His journey began with a simple backpacking trip through Europe and has evolved into a mission to inspire others to explore.
                    </p>
                    <p class="text-lg text-gray-600 mb-8">
                        From remote mountain villages to bustling metropolitan cities, John captures the essence of each destination through authentic experiences and meaningful connections with local communities.
                    </p>
                    <div class="flex space-x-4">
                        <div class="text-center">
                            <div class="text-3xl font-bold text-blue-600">80+</div>
                            <div class="text-gray-600">Countries Visited</div>
                        </div>
                        <div class="text-center">
                            <div class="text-3xl font-bold text-blue-600">15</div>
                            <div class="text-gray-600">Years Experience</div>
                        </div>
                        <div class="text-center">
                            <div class="text-3xl font-bold text-blue-600">500+</div>
                            <div class="text-gray-600">Adventures Shared</div>
                        </div>
                    </div>
                </div>
                <div class="bg-gradient-to-br from-blue-400 to-purple-500 rounded-2xl p-8 text-white text-center">
                    <div class="text-8xl mb-4">🧳</div>
                    <h4 class="text-2xl font-bold mb-4">Travel Philosophy</h4>
                    <p class="text-lg opacity-90">
                        "Travel is not just about seeing new places, it's about opening your mind, challenging your perspectives, and creating memories that last a lifetime."
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gray-800 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h3 class="text-4xl font-bold mb-4">Start Your Adventure</h3>
                <p class="text-xl text-gray-300 max-w-2xl mx-auto">Ready to explore the world? Get in touch to plan your next unforgettable journey.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <div>
                    <h4 class="text-2xl font-bold mb-6">Get In Touch</h4>
                    <div class="space-y-4">
                        <div class="flex items-center">
                            <div class="text-2xl mr-4">📧</div>
                            <div>
                                <div class="font-semibold">Email</div>
                                <div class="text-gray-300">johnextry@gmail.com</div>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="text-2xl mr-4">📱</div>
                            <div>
                                <div class="font-semibold">Phone</div>
                                <div class="text-gray-300">0704 628 8447</div>
                                <div class="text-gray-300">0806 348 3975</div>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="text-2xl mr-4">💬</div>
                            <div>
                                <div class="font-semibold">WhatsApp</div>
                                <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa?mode=wwt" target="_blank" rel="noopener noreferrer" class="text-green-400 hover:text-green-300 transition-colors">Join Travel Group</a>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <div class="text-2xl mr-4">🌍</div>
                            <div>
                                <div class="font-semibold">Follow the Journey</div>
                                <div class="text-gray-300">@johnoyetravels</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div>
                    <form onsubmit="handleContactForm(event)" class="space-y-4">
                        <div>
                            <label class="block text-sm font-medium mb-2">Name</label>
                            <input type="text" required class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white">
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-2">Email</label>
                            <input type="email" required class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white">
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-2">Dream Destination</label>
                            <input type="text" class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white">
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-2">Message</label>
                            <textarea rows="4" required class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white"></textarea>
                        </div>
                        <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-lg font-semibold transition-colors">
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Disclaimer Section -->
    <section id="disclaimer" class="py-16 bg-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-white rounded-xl shadow-lg p-8">
                <h3 class="text-3xl font-bold text-gray-800 mb-8 text-center">DISCLAIMER</h3>
                
                <div class="space-y-8">
                    <!-- Visa Approval Section -->
                    <div>
                        <h4 class="text-xl font-bold text-gray-800 mb-4">1. Visa Approval/Refusal</h4>
                        <p class="text-gray-600 leading-relaxed">
                            The approval or refusal of a visa is solely at the discretion of the respective Consulate or Embassy. John Oye's travel is not involved in the decision-making process and has no control over the outcome.
                        </p>
                    </div>

                    <!-- Role Section -->
                    <div>
                        <h4 class="text-xl font-bold text-gray-800 mb-4">2. Role of John Oye's travel:</h4>
                        <p class="text-gray-600 leading-relaxed">
                            John Oye's travel acts solely as a facilitator in the visa application process. We can not be held responsible for any delays, rejections, or refusals of visas by the issuing authority. All outcomes are governed by the rules and decisions of the respective Consulate or Embassy.
                        </p>
                    </div>

                    <!-- Non-Refundable Fees -->
                    <div>
                        <h4 class="text-xl font-bold text-gray-800 mb-4">3. Non-Refundable Fees</h4>
                        <p class="text-gray-600 leading-relaxed">
                            All visa application fees, processing charges, and related costs are non-refundable once paid. This applies to all receipted charges, regardless of the outcome of the visa application.
                        </p>
                    </div>

                    <!-- Changes in Fees -->
                    <div>
                        <h4 class="text-xl font-bold text-gray-800 mb-4">4. Changes in Fees and Requirements</h4>
                        <p class="text-gray-600 leading-relaxed">
                            Visa fees, charges, and document requirements are subject to change without prior notice, as they are determined by the issuing authority. John Oye's travel is not liable for such changes and advises applicants to verify all information directly with the relevant Consulate or Embassy.
                        </p>
                    </div>

                    <!-- Overstay Section -->
                    <div>
                        <h4 class="text-xl font-bold text-gray-800 mb-4">5. Overstay or Absconding</h4>
                        <p class="text-gray-600 leading-relaxed">
                            If a traveller overstays or absconds in the host country, the B2C agent handling the traveller will be held liable for any financial damages incurred due to this action. John Oye's travel is not responsible for the actions or decisions of the traveller once the visa has been issued.
                        </p>
                    </div>

                    <!-- Commission Structure -->
                    <div>
                        <h4 class="text-xl font-bold text-gray-800 mb-4">6. John Oye's travel commission for different countries are as follows:</h4>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <ul class="space-y-2 text-gray-700">
                                <li><strong>a.</strong> First World countries, Schengen & Europe - 700k-860k</li>
                                <li><strong>b.</strong> Asia, Middle East & other countries - 500k-650k</li>
                                <li><strong>c.</strong> Africa countries - 300k</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- WhatsApp Terms Section -->
                <div class="mt-12 pt-8 border-t border-gray-200">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">John Oye's travel WhatsApp Group Terms and Conditions</h3>
                    <p class="text-gray-600 mb-6 leading-relaxed">
                        The John Oye's travel WhatsApp group serves as a platform for sharing information and discussing topics related to visa applications and travel services. By participating, you acknowledge the following terms and conditions:
                    </p>

                    <div class="space-y-6">
                        <!-- Packages and Payment -->
                        <div>
                            <h4 class="text-lg font-bold text-gray-800 mb-3">1. Packages and Payment</h4>
                            <p class="text-gray-600 mb-3">
                                All visa and travel packages offered by John Oye's travel come with NO DEPOSIT or otherwise stated. However, proof of commitment (POC) is mandatory. The POC can be provided by any of the following means:
                            </p>
                            <ul class="list-disc list-inside text-gray-600 space-y-1 ml-4">
                                <li>Blocking funds in your personal account</li>
                                <li>Opening a joint account with two signatories</li>
                                <li>Providing a bank draft</li>
                            </ul>
                            <p class="text-gray-600 mt-3 italic">
                                Please ensure that you fully understand these payment terms before proceeding with any transactions.
                            </p>
                        </div>

                        <!-- Business Transactions -->
                        <div>
                            <h4 class="text-lg font-bold text-gray-800 mb-3">2. Business Transactions</h4>
                            <p class="text-gray-600">
                                Any business transactions or dealings conducted outside the purview of the group administrators or conveners are done so at your own risk. John Oye's travel and its administrators can not be held liable for any losses or damages incurred as a result of such transactions.
                            </p>
                        </div>

                        <!-- Liability -->
                        <div>
                            <h4 class="text-lg font-bold text-gray-800 mb-3">3. Liability</h4>
                            <p class="text-gray-600 mb-3">
                                John Oye's travel and its administrators will not be held responsible for any losses, damages, or claims arising from:
                            </p>
                            <ul class="list-disc list-inside text-gray-600 space-y-1 ml-4">
                                <li>Misinformation or miscommunication</li>
                                <li>Unverified or unauthenticated transactions</li>
                                <li>Breaches of contract or agreement</li>
                                <li>Any other circumstances beyond our control</li>
                            </ul>
                        </div>

                        <!-- Information Sharing -->
                        <div>
                            <h4 class="text-lg font-bold text-gray-800 mb-3">4. Information Sharing</h4>
                            <p class="text-gray-600 mb-3">
                                Information shared within the group is intended for general guidance only and should not be considered as professional advice. We strongly recommend that you verify all information through the relevant authorities and seek professional counsel when necessary.
                            </p>
                            <p class="text-blue-600 font-semibold">Note: Appointment required before visiting.</p>
                        </div>
                    </div>

                    <!-- Final Notice -->
                    <div class="mt-8 p-6 bg-yellow-50 border-l-4 border-yellow-400 rounded-r-lg">
                        <p class="text-gray-700 mb-4">
                            By participating in the John Oye's travel WhatsApp group, you acknowledge that you have read, understood, and agreed to the terms and conditions outlined in this disclaimer.
                        </p>
                        <p class="text-lg font-semibold text-gray-800 mb-4 italic">
                            Live, study, and travel the world with ease, but always prioritize caution and due diligence in all your transactions.
                        </p>
                        <div class="space-y-2">
                            <p class="text-gray-700">
                                <strong>For more information, call:</strong> 
                                <span class="text-blue-600 font-semibold">08063483975</span> (direct call only)
                            </p>
                            <p class="text-gray-700">
                                <strong>John Oye's travel</strong>
                            </p>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="inline-block text-green-600 hover:text-green-700 font-semibold transition-colors">
                                Join WhatsApp Group →
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">&copy; 2024 John Oye's Travels. All rights reserved. | Inspiring wanderlust since 2009</p>
        </div>
    </footer>

    <!-- Destination Modal -->
    <div id="destinationModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center p-4">
        <div class="bg-white rounded-xl max-w-2xl w-full max-h-full overflow-y-auto">
            <div class="p-6">
                <div class="flex justify-between items-center mb-4">
                    <h3 id="modalTitle" class="text-2xl font-bold text-gray-800"></h3>
                    <button onclick="closeModal()" class="text-gray-500 hover:text-gray-700 text-2xl">&times;</button>
                </div>
                <div id="modalContent" class="text-gray-600"></div>
                <button onclick="closeModal()" class="mt-6 bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-lg transition-colors">
                    Close
                </button>
            </div>
        </div>
    </div>

    <script>
        function scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({
                behavior: 'smooth'
            });
        }

        function showDestinationDetails(destination) {
            const modal = document.getElementById('destinationModal');
            const title = document.getElementById('modalTitle');
            const content = document.getElementById('modalContent');
            
            const destinations = {
                'Swiss Alps': {
                    title: 'Swiss Alps Adventure',
                    content: `
                        <div class="space-y-4">
                            <div class="text-6xl text-center">🏔️</div>
                            <p>Experience the breathtaking beauty of the Swiss Alps with John's carefully curated mountain adventures. From the iconic Matterhorn to the pristine lakes of Interlaken, discover why Switzerland remains one of the world's most spectacular destinations.</p>
                            <h4 class="font-bold text-lg">Highlights:</h4>
                            <ul class="list-disc list-inside space-y-1">
                                <li>Scenic train rides through mountain passes</li>
                                <li>Traditional Alpine village experiences</li>
                                <li>World-class skiing and hiking trails</li>
                                <li>Authentic Swiss cuisine and hospitality</li>
                            </ul>
                            <p class="italic">"The Alps taught me that some of nature's greatest masterpieces are best appreciated in silence." - John Oye</p>
                        </div>
                    `
                },
                'Maldives': {
                    title: 'Maldives Paradise',
                    content: `
                        <div class="space-y-4">
                            <div class="text-6xl text-center">🏝️</div>
                            <p>Escape to the ultimate tropical paradise where crystal-clear waters meet pristine white sand beaches. John's Maldives experience showcases the perfect blend of luxury and natural beauty in the Indian Ocean.</p>
                            <h4 class="font-bold text-lg">Highlights:</h4>
                            <ul class="list-disc list-inside space-y-1">
                                <li>Overwater bungalow accommodations</li>
                                <li>World-class snorkeling and diving</li>
                                <li>Sunset dolphin watching cruises</li>
                                <li>Private beach dining experiences</li>
                            </ul>
                            <p class="italic">"In the Maldives, every sunset feels like a personal gift from nature." - John Oye</p>
                        </div>
                    `
                },
                'Japan': {
                    title: 'Japan Cultural Journey',
                    content: `
                        <div class="space-y-4">
                            <div class="text-6xl text-center">🗾</div>
                            <p>Immerse yourself in the fascinating contrast between ancient traditions and cutting-edge modernity. John's Japan adventures reveal the soul of a nation that honors its past while embracing the future.</p>
                            <h4 class="font-bold text-lg">Highlights:</h4>
                            <ul class="list-disc list-inside space-y-1">
                                <li>Traditional tea ceremonies and temples</li>
                                <li>Cherry blossom season experiences</li>
                                <li>Authentic sushi and ramen tours</li>
                                <li>Modern Tokyo and historic Kyoto</li>
                            </ul>
                            <p class="italic">"Japan showed me that tradition and innovation can dance together in perfect harmony." - John Oye</p>
                        </div>
                    `
                },
                'Kenya Safari': {
                    title: 'Kenya Safari Adventure',
                    content: `
                        <div class="space-y-4">
                            <div class="text-6xl text-center">🦁</div>
                            <p>Witness the raw beauty of African wildlife in their natural habitat. John's Kenya safari experiences offer unforgettable encounters with the Big Five and the spectacular Great Migration.</p>
                            <h4 class="font-bold text-lg">Highlights:</h4>
                            <ul class="list-disc list-inside space-y-1">
                                <li>Masai Mara game drives</li>
                                <li>Great Migration witnessing</li>
                                <li>Cultural visits with Masai communities</li>
                                <li>Hot air balloon safaris</li>
                            </ul>
                            <p class="italic">"Africa doesn't just show you wildlife; it shows you life in its purest, most powerful form." - John Oye</p>
                        </div>
                    `
                },
                'Greece': {
                    title: 'Greece Ancient Wonders',
                    content: `
                        <div class="space-y-4">
                            <div class="text-6xl text-center">🏛️</div>
                            <p>Walk in the footsteps of ancient philosophers and gods while enjoying stunning Mediterranean landscapes. John's Greek odyssey combines historical exploration with island paradise relaxation.</p>
                            <h4 class="font-bold text-lg">Highlights:</h4>
                            <ul class="list-disc list-inside space-y-1">
                                <li>Acropolis and ancient Athens exploration</li>
                                <li>Santorini sunset experiences</li>
                                <li>Traditional Greek island hopping</li>
                                <li>Authentic Mediterranean cuisine</li>
                            </ul>
                            <p class="italic">"Greece reminds us that some stories are so powerful, they echo through millennia." - John Oye</p>
                        </div>
                    `
                },
                'Peru': {
                    title: 'Peru Mystical Journey',
                    content: `
                        <div class="space-y-4">
                            <div class="text-6xl text-center">🌸</div>
                            <p>Embark on a spiritual journey through the heart of the ancient Inca Empire. John's Peru adventures combine challenging treks with profound cultural discoveries in the Andes Mountains.</p>
                            <h4 class="font-bold text-lg">Highlights:</h4>
                            <ul class="list-disc list-inside space-y-1">
                                <li>Machu Picchu sunrise experiences</li>
                                <li>Inca Trail trekking adventures</li>
                                <li>Sacred Valley cultural immersion</li>
                                <li>Traditional Andean cuisine</li>
                            </ul>
                            <p class="italic">"Machu Picchu taught me that some achievements are worth every step of the journey." - John Oye</p>
                        </div>
                    `
                }
            };
            
            const dest = destinations[destination];
            title.textContent = dest.title;
            content.innerHTML = dest.content;
            modal.classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('destinationModal').classList.add('hidden');
        }

        function handleContactForm(event) {
            event.preventDefault();
            
            // Create success message
            const form = event.target;
            const successMessage = document.createElement('div');
            successMessage.className = 'bg-green-600 text-white p-4 rounded-lg mt-4';
            successMessage.innerHTML = `
                <div class="flex items-center">
                    <div class="text-2xl mr-3">✅</div>
                    <div>
                        <div class="font-semibold">Message Sent Successfully!</div>
                        <div class="text-sm opacity-90">John will get back to you within 24 hours to start planning your adventure.</div>
                    </div>
                </div>
            `;
            
            // Replace form with success message
            form.style.display = 'none';
            form.parentNode.appendChild(successMessage);
            
            // Reset form after 3 seconds
            setTimeout(() => {
                form.reset();
                form.style.display = 'block';
                successMessage.remove();
            }, 3000);
        }

        function handlePassportForm(event) {
            event.preventDefault();
            
            // Create success message
            const form = event.target;
            const successMessage = document.createElement('div');
            successMessage.className = 'bg-green-600 text-white p-4 rounded-lg mt-4';
            successMessage.innerHTML = `
                <div class="flex items-center">
                    <div class="text-2xl mr-3">🛂</div>
                    <div>
                        <div class="font-semibold">Passport Application Submitted Successfully!</div>
                        <div class="text-sm opacity-90">We'll review your information and contact you within 24 hours to proceed with your passport application. Please ensure you have all required documents ready.</div>
                    </div>
                </div>
            `;
            
            // Replace form with success message
            form.style.display = 'none';
            form.parentNode.appendChild(successMessage);
            
            // Reset form after 5 seconds
            setTimeout(() => {
                form.reset();
                form.style.display = 'block';
                successMessage.remove();
            }, 5000);
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Close modal when clicking outside
        document.getElementById('destinationModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });

        // Payment plan selection
        function selectPaymentPlan(plan) {
            const planNames = {
                'full': 'Full Payment Plan',
                'installment': 'Installment Payment Plan',
                'group': 'Group Booking Plan'
            };
            
            const planDetails = {
                'full': 'You\'ve selected the Full Payment Plan with 10% discount. We\'ll contact you to finalize your booking.',
                'installment': 'You\'ve selected the Installment Plan. We\'ll discuss flexible payment terms that work for you.',
                'group': 'You\'ve selected Group Booking. We\'ll create a custom package for your group with special rates.'
            };

            // Create success message
            const successMessage = document.createElement('div');
            successMessage.className = 'fixed top-4 right-4 bg-green-600 text-white p-6 rounded-lg shadow-lg z-50 max-w-md';
            successMessage.innerHTML = `
                <div class="flex items-start">
                    <div class="text-2xl mr-3">✅</div>
                    <div>
                        <div class="font-bold text-lg mb-2">${planNames[plan]} Selected!</div>
                        <div class="text-sm opacity-90 mb-4">${planDetails[plan]}</div>
                        <div class="flex space-x-2">
                            <a href="tel:08063483975" class="bg-white text-green-600 px-3 py-1 rounded text-sm font-semibold hover:bg-gray-100">Call Now</a>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-green-500 text-white px-3 py-1 rounded text-sm font-semibold hover:bg-green-400">WhatsApp</a>
                        </div>
                    </div>
                    <button onclick="this.parentElement.parentElement.remove()" class="text-white hover:text-gray-200 ml-2">&times;</button>
                </div>
            `;
            
            document.body.appendChild(successMessage);
            
            // Auto remove after 8 seconds
            setTimeout(() => {
                if (successMessage.parentNode) {
                    successMessage.remove();
                }
            }, 8000);
        }

        // Flight and Hotel booking functions
        function openFlightBooking() {
            const message = document.createElement('div');
            message.className = 'fixed top-4 right-4 bg-blue-600 text-white p-6 rounded-lg shadow-lg z-50 max-w-md';
            message.innerHTML = `
                <div class="flex items-start">
                    <div class="text-2xl mr-3">✈️</div>
                    <div>
                        <div class="font-bold text-lg mb-2">Flight Booking Service</div>
                        <div class="text-sm opacity-90 mb-4">Contact us for personalized flight booking assistance. We'll find the best deals for your travel dates and preferences.</div>
                        <div class="flex space-x-2">
                            <a href="tel:08063483975" class="bg-white text-blue-600 px-3 py-1 rounded text-sm font-semibold hover:bg-gray-100">Call Now</a>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-blue-500 text-white px-3 py-1 rounded text-sm font-semibold hover:bg-blue-400">WhatsApp</a>
                        </div>
                    </div>
                    <button onclick="this.parentElement.parentElement.remove()" class="text-white hover:text-gray-200 ml-2">&times;</button>
                </div>
            `;
            document.body.appendChild(message);
            setTimeout(() => { if (message.parentNode) message.remove(); }, 8000);
        }

        function openHotelBooking() {
            const message = document.createElement('div');
            message.className = 'fixed top-4 right-4 bg-purple-600 text-white p-6 rounded-lg shadow-lg z-50 max-w-md';
            message.innerHTML = `
                <div class="flex items-start">
                    <div class="text-2xl mr-3">🏨</div>
                    <div>
                        <div class="font-bold text-lg mb-2">Hotel Booking Service</div>
                        <div class="text-sm opacity-90 mb-4">Let us help you find the perfect accommodation. From budget-friendly to luxury options, we have access to exclusive rates.</div>
                        <div class="flex space-x-2">
                            <a href="tel:08063483975" class="bg-white text-purple-600 px-3 py-1 rounded text-sm font-semibold hover:bg-gray-100">Call Now</a>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-purple-500 text-white px-3 py-1 rounded text-sm font-semibold hover:bg-purple-400">WhatsApp</a>
                        </div>
                    </div>
                    <button onclick="this.parentElement.parentElement.remove()" class="text-white hover:text-gray-200 ml-2">&times;</button>
                </div>
            `;
            document.body.appendChild(message);
            setTimeout(() => { if (message.parentNode) message.remove(); }, 8000);
        }

        function bookRoute(route) {
            const routes = {
                'LOS-DXB': { from: 'Lagos', to: 'Dubai', price: '₦450,000' },
                'LOS-LHR': { from: 'Lagos', to: 'London', price: '₦850,000' },
                'LOS-JFK': { from: 'Lagos', to: 'New York', price: '₦1,200,000' },
                'ABV-CDG': { from: 'Abuja', to: 'Paris', price: '₦780,000' },
                'LOS-YYZ': { from: 'Lagos', to: 'Toronto', price: '₦950,000' },
                'LOS-IST': { from: 'Lagos', to: 'Istanbul', price: '₦520,000' }
            };
            
            const routeInfo = routes[route];
            const message = document.createElement('div');
            message.className = 'fixed top-4 right-4 bg-green-600 text-white p-6 rounded-lg shadow-lg z-50 max-w-md';
            message.innerHTML = `
                <div class="flex items-start">
                    <div class="text-2xl mr-3">🎯</div>
                    <div>
                        <div class="font-bold text-lg mb-2">Flight Route Selected!</div>
                        <div class="text-sm opacity-90 mb-1"><strong>${routeInfo.from} → ${routeInfo.to}</strong></div>
                        <div class="text-lg font-bold mb-3">Starting from ${routeInfo.price}</div>
                        <div class="text-sm opacity-90 mb-4">Contact us to check availability and get the best deals for your travel dates.</div>
                        <div class="flex space-x-2">
                            <a href="tel:08063483975" class="bg-white text-green-600 px-3 py-1 rounded text-sm font-semibold hover:bg-gray-100">Call Now</a>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-green-500 text-white px-3 py-1 rounded text-sm font-semibold hover:bg-green-400">WhatsApp</a>
                        </div>
                    </div>
                    <button onclick="this.parentElement.parentElement.remove()" class="text-white hover:text-gray-200 ml-2">&times;</button>
                </div>
            `;
            document.body.appendChild(message);
            setTimeout(() => { if (message.parentNode) message.remove(); }, 10000);
        }

        function searchHotels(destination) {
            const destinations = {
                'Dubai': { price: '₦45,000', description: 'Luxury hotels & resorts in the heart of Dubai' },
                'London': { price: '₦65,000', description: 'Historic & modern stays across London' },
                'Paris': { price: '₦55,000', description: 'Romantic boutique hotels in Paris' },
                'New York': { price: '₦85,000', description: 'Manhattan & Brooklyn accommodations' }
            };
            
            const destInfo = destinations[destination];
            const message = document.createElement('div');
            message.className = 'fixed top-4 right-4 bg-orange-600 text-white p-6 rounded-lg shadow-lg z-50 max-w-md';
            message.innerHTML = `
                <div class="flex items-start">
                    <div class="text-2xl mr-3">🏨</div>
                    <div>
                        <div class="font-bold text-lg mb-2">${destination} Hotels</div>
                        <div class="text-sm opacity-90 mb-1">${destInfo.description}</div>
                        <div class="text-lg font-bold mb-3">Starting from ${destInfo.price}/night</div>
                        <div class="text-sm opacity-90 mb-4">Contact us to explore available hotels and get exclusive rates for your stay.</div>
                        <div class="flex space-x-2">
                            <a href="tel:08063483975" class="bg-white text-orange-600 px-3 py-1 rounded text-sm font-semibold hover:bg-gray-100">Call Now</a>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-orange-500 text-white px-3 py-1 rounded text-sm font-semibold hover:bg-orange-400">WhatsApp</a>
                        </div>
                    </div>
                    <button onclick="this.parentElement.parentElement.remove()" class="text-white hover:text-gray-200 ml-2">&times;</button>
                </div>
            `;
            document.body.appendChild(message);
            setTimeout(() => { if (message.parentNode) message.remove(); }, 10000);
        }

        function handleFlightSearch(event) {
            event.preventDefault();
            const form = event.target;
            const formData = new FormData(form);
            
            const successMessage = document.createElement('div');
            successMessage.className = 'bg-blue-600 text-white p-4 rounded-lg mt-4';
            successMessage.innerHTML = `
                <div class="flex items-center">
                    <div class="text-2xl mr-3">✈️</div>
                    <div>
                        <div class="font-semibold">Flight Search Submitted!</div>
                        <div class="text-sm opacity-90">We're searching for the best flight options for you. Our team will contact you within 2 hours with available flights and prices.</div>
                    </div>
                </div>
            `;
            
            form.style.display = 'none';
            form.parentNode.appendChild(successMessage);
            
            setTimeout(() => {
                form.reset();
                form.style.display = 'block';
                successMessage.remove();
            }, 5000);
        }

        function handleHotelSearch(event) {
            event.preventDefault();
            const form = event.target;
            const formData = new FormData(form);
            
            const successMessage = document.createElement('div');
            successMessage.className = 'bg-purple-600 text-white p-4 rounded-lg mt-4';
            successMessage.innerHTML = `
                <div class="flex items-center">
                    <div class="text-2xl mr-3">🏨</div>
                    <div>
                        <div class="font-semibold">Hotel Search Submitted!</div>
                        <div class="text-sm opacity-90">We're finding the perfect accommodations for your stay. Our team will contact you within 2 hours with available hotels and rates.</div>
                    </div>
                </div>
            `;
            
            form.style.display = 'none';
            form.parentNode.appendChild(successMessage);
            
            setTimeout(() => {
                form.reset();
                form.style.display = 'block';
                successMessage.remove();
            }, 5000);
        }

        // Package booking
        function bookPackage(packageType) {
            const packages = {
                'europe': {
                    name: 'Europe Explorer Package',
                    price: '₦2,500,000',
                    description: '7-day European adventure across 3 countries'
                },
                'dubai': {
                    name: 'Dubai Luxury Package',
                    price: '₦1,800,000',
                    description: '5-day premium Dubai experience'
                },
                'usa': {
                    name: 'USA Adventure Package',
                    price: '₦4,200,000',
                    description: '10-day coast-to-coast American journey'
                }
            };

            const pkg = packages[packageType];
            
            // Create booking confirmation
            const bookingMessage = document.createElement('div');
            bookingMessage.className = 'fixed top-4 right-4 bg-blue-600 text-white p-6 rounded-lg shadow-lg z-50 max-w-md';
            bookingMessage.innerHTML = `
                <div class="flex items-start">
                    <div class="text-2xl mr-3">🎯</div>
                    <div>
                        <div class="font-bold text-lg mb-2">Package Selected!</div>
                        <div class="text-sm opacity-90 mb-1"><strong>${pkg.name}</strong></div>
                        <div class="text-sm opacity-90 mb-1">${pkg.description}</div>
                        <div class="text-lg font-bold mb-3">${pkg.price}</div>
                        <div class="text-sm opacity-90 mb-4">Contact us to discuss payment options and finalize your booking.</div>
                        <div class="flex space-x-2">
                            <a href="tel:08063483975" class="bg-white text-blue-600 px-3 py-1 rounded text-sm font-semibold hover:bg-gray-100">Call Now</a>
                            <a href="https://chat.whatsapp.com/EHufce5WI8h27YKzvPdcKa" target="_blank" rel="noopener noreferrer" class="bg-blue-500 text-white px-3 py-1 rounded text-sm font-semibold hover:bg-blue-400">WhatsApp</a>
                        </div>
                    </div>
                    <button onclick="this.parentElement.parentElement.remove()" class="text-white hover:text-gray-200 ml-2">&times;</button>
                </div>
            `;
            
            document.body.appendChild(bookingMessage);
            
            // Auto remove after 10 seconds
            setTimeout(() => {
                if (bookingMessage.parentNode) {
                    bookingMessage.remove();
                }
            }, 10000);
        }
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'98f0092df1a22695',t:'MTc2MDUzODg1MS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>

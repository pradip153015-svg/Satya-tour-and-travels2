<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Satya Tour and Travels | Puri Darshan & Taxi Booking</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            gold: '#f59e0b',
                            saffron: '#ea580c',
                            blue: '#0284c7',
                            dark: '#0f172a',
                            light: '#f8fafc'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif']
                    }
                }
            }
        }
    </script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- AOS Animation Library -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>

    <style>
        body {
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
        }
        .font-serif-title {
            font-family: 'Playfair Display', serif;
        }
        /* Custom Glowing & Pulse Animations */
        @keyframes pulse-subtle {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        .animate-pulse-subtle {
            animation: pulse-subtle 2.5s infinite ease-in-out;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        .animate-float {
            animation: float 4s ease-in-out infinite;
        }
        /* Gradient Overlay Text */
        .gradient-text {
            background: linear-gradient(135deg, #f59e0b 0%, #ea580c 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .hero-bg {
            background: linear-gradient(rgba(15, 23, 42, 0.75), rgba(15, 23, 42, 0.85)), url('https://images.unsplash.com/photo-1590050752117-238cb0fb12b1?q=80&w=1600&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased selection:bg-amber-500 selection:text-white">

    <!-- Top Announcement Bar -->
    <div class="bg-gradient-to-r from-amber-600 to-orange-600 text-white text-xs sm:text-sm py-2 px-4 text-center font-medium shadow-sm flex justify-between items-center max-w-full">
        <div class="container mx-auto flex justify-between items-center">
            <span class="flex items-center gap-2"><i class="fa-solid fa-star text-yellow-300"></i> #1 Trusted Taxi Service in Puri & Bhubaneswar</span>
            <div class="hidden md:flex items-center gap-6">
                <a href="tel:7978039882" class="hover:underline flex items-center gap-1"><i class="fa-solid fa-phone"></i> +91 7978039882</a>
                <span class="flex items-center gap-1"><i class="fa-solid fa-clock"></i> 24/7 Cab Dispatch</span>
            </div>
        </div>
    </div>

    <!-- Navigation Header -->
    <header class="sticky top-0 z-40 bg-white/90 backdrop-blur-md border-b border-slate-100 shadow-sm transition-all duration-300">
        <div class="container mx-auto px-4 lg:px-8 py-3 flex items-center justify-between">
            <!-- Brand Logo -->
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-amber-500 to-orange-600 flex items-center justify-center text-white font-bold text-xl shadow-md shadow-amber-500/20 group-hover:scale-105 transition-transform">
                    <i class="fa-solid fa-taxi"></i>
                </div>
                <div>
                    <span class="text-xl font-extrabold text-slate-900 tracking-tight block leading-none">Satya <span class="text-amber-500">Tour & Travels</span></span>
                    <span class="text-xs text-slate-500 font-medium tracking-wide">Puri & Odisha Sightseeing Experts</span>
                </div>
            </a>

            <!-- Desktop Nav Items -->
            <nav class="hidden lg:flex items-center gap-8 font-medium text-slate-600 text-sm">
                <a href="#home" class="hover:text-amber-600 transition-colors">Home</a>
                <a href="#tour1" class="hover:text-amber-600 transition-colors flex items-center gap-1"><span class="w-2 h-2 rounded-full bg-orange-500 inline-block animate-ping"></span> Mega Tour 1</a>
                <a href="#fleet" class="hover:text-amber-600 transition-colors">Car Fleet</a>
                <a href="#services" class="hover:text-amber-600 transition-colors">Services</a>
                <a href="#why-us" class="hover:text-amber-600 transition-colors">Why Choose Us</a>
            </nav>

            <!-- Call to Action Buttons -->
            <div class="hidden sm:flex items-center gap-3">
                <a href="tel:7978039882" class="flex items-center gap-2 bg-slate-100 hover:bg-slate-200 text-slate-800 px-4 py-2 rounded-xl font-semibold text-sm transition-all">
                    <i class="fa-solid fa-phone text-amber-500"></i> Call 7978039882
                </a>
                <a href="#booking" class="bg-gradient-to-r from-amber-500 to-orange-600 hover:from-amber-600 hover:to-orange-700 text-white px-5 py-2 rounded-xl font-semibold text-sm shadow-md shadow-orange-500/20 hover:shadow-lg transition-all hover:-translate-y-0.5">
                    Book Taxi
                </a>
            </div>

            <!-- Mobile Menu Toggle -->
            <button id="mobileMenuBtn" class="lg:hidden p-2 rounded-lg text-slate-700 hover:bg-slate-100 focus:outline-none">
                <i class="fa-solid fa-bars text-xl"></i>
            </button>
        </div>

        <!-- Mobile Navigation Drawer -->
        <div id="mobileMenu" class="hidden lg:hidden bg-white border-b border-slate-200 px-6 py-4 transition-all">
            <div class="flex flex-col gap-4 font-medium text-slate-700">
                <a href="#home" class="mobile-link py-1 hover:text-amber-600">Home</a>
                <a href="#tour1" class="mobile-link py-1 hover:text-amber-600 text-orange-600 font-semibold">Mega Tour 1 (Puri-Konark-Bhubaneswar)</a>
                <a href="#fleet" class="mobile-link py-1 hover:text-amber-600">Our Fleet</a>
                <a href="#services" class="mobile-link py-1 hover:text-amber-600">Services</a>
                <a href="#why-us" class="mobile-link py-1 hover:text-amber-600">Why Us</a>
                <div class="pt-2 border-t border-slate-100 flex flex-col gap-2">
                    <a href="tel:7978039882" class="flex items-center justify-center gap-2 bg-slate-100 text-slate-800 py-2.5 rounded-xl font-semibold text-sm">
                        <i class="fa-solid fa-phone text-amber-500"></i> Call 7978039882
                    </a>
                    <a href="#booking" class="mobile-link text-center bg-gradient-to-r from-amber-500 to-orange-600 text-white py-2.5 rounded-xl font-semibold text-sm shadow-md">
                        Book Taxi Now
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section with Booking Form -->
    <section id="home" class="hero-bg relative text-white py-12 lg:py-20 px-4 lg:px-8">
        <div class="container mx-auto grid lg:grid-cols-12 gap-12 items-center">
            
            <!-- Hero Content Left -->
            <div class="lg:col-span-7 space-y-6" data-aos="fade-right">
                <div class="inline-flex items-center gap-2 bg-amber-500/20 backdrop-blur-md border border-amber-400/30 px-3 py-1.5 rounded-full text-amber-300 text-xs sm:text-sm font-semibold">
                    <i class="fa-solid fa-dharmachakra animate-spin-slow"></i> Satya Tour & Travels Puri
                </div>
                
                <h1 class="text-3xl sm:text-5xl lg:text-6xl font-extrabold leading-tight font-serif-title">
                    Explore Odisha with <br class="hidden sm:inline">
                    <span class="gradient-text">Comfort & Safety</span>
                </h1>
                
                <p class="text-slate-300 text-base sm:text-lg max-w-2xl leading-relaxed">
                    Reliable AC Cabs & Experienced Drivers for Puri Temple Darshan, Konark Sun Temple, Chilika Lake & Bhubaneswar local sightseeing. Transparent rates & zero hidden fees.
                </p>

                <!-- Feature Badges -->
                <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 pt-2">
                    <div class="flex items-center gap-3 bg-white/10 backdrop-blur-md p-3 rounded-xl border border-white/10">
                        <i class="fa-solid fa-car text-amber-400 text-xl"></i>
                        <span class="text-xs sm:text-sm font-medium">Clean AC Cabs</span>
                    </div>
                    <div class="flex items-center gap-3 bg-white/10 backdrop-blur-md p-3 rounded-xl border border-white/10">
                        <i class="fa-solid fa-user-shield text-amber-400 text-xl"></i>
                        <span class="text-xs sm:text-sm font-medium">Expert Local Drivers</span>
                    </div>
                    <div class="flex items-center gap-3 bg-white/10 backdrop-blur-md p-3 rounded-xl border border-white/10 col-span-2 sm:col-span-1">
                        <i class="fa-solid fa-indian-rupee-sign text-amber-400 text-xl"></i>
                        <span class="text-xs sm:text-sm font-medium">Best Price Guarantee</span>
                    </div>
                </div>

                <!-- Direct Call Banner -->
                <div class="bg-gradient-to-r from-amber-500/30 to-orange-500/30 border border-amber-500/40 p-4 rounded-2xl backdrop-blur-md flex flex-wrap items-center justify-between gap-4">
                    <div>
                        <div class="text-xs text-amber-300 uppercase tracking-wider font-semibold">Instant Tele-Booking</div>
                        <div class="text-xl sm:text-2xl font-bold text-white flex items-center gap-2">
                            <i class="fa-solid fa-phone-volume text-amber-400 animate-pulse"></i> 7978039882
                        </div>
                    </div>
                    <a href="https://wa.me/917978039882?text=Hello%20Satya%20Tour%20and%20Travels,%20I%20want%20to%20book%20a%20taxi." target="_blank" class="bg-emerald-600 hover:bg-emerald-700 text-white px-4 py-2.5 rounded-xl font-bold text-sm flex items-center gap-2 shadow-lg transition-all hover:scale-105">
                        <i class="fa-brands fa-whatsapp text-lg"></i> WhatsApp Booking
                    </a>
                </div>
            </div>

            <!-- Booking Form Right -->
            <div id="booking" class="lg:col-span-5 bg-white text-slate-800 p-6 sm:p-8 rounded-3xl shadow-2xl relative border border-slate-100" data-aos="fade-left">
                <div class="absolute -top-3 right-6 bg-gradient-to-r from-amber-500 to-orange-600 text-white text-xs font-bold px-3 py-1 rounded-full shadow-md uppercase tracking-wide">
                    Instant Confirmation
                </div>
                
                <h3 class="text-2xl font-bold text-slate-900 mb-1">Book Your Taxi</h3>
                <p class="text-xs text-slate-500 mb-6">Fill in details for quick quote or booking</p>

                <form id="taxiBookingForm" onsubmit="handleBookingSubmit(event)" class="space-y-4">
                    <!-- Ride Type -->
                    <div class="grid grid-cols-2 gap-2 p-1 bg-slate-100 rounded-xl text-xs font-semibold">
                        <button type="button" onclick="setBookingType('tour')" id="btnTypeTour" class="py-2 rounded-lg bg-amber-500 text-white shadow-sm transition-all">Tour Package</button>
                        <button type="button" onclick="setBookingType('custom')" id="btnTypeCustom" class="py-2 rounded-lg text-slate-600 hover:bg-slate-200 transition-all">Pick & Drop / Custom</button>
                    </div>

                    <!-- Hidden field for booking type -->
                    <input type="hidden" id="bookingType" value="tour">

                    <!-- Tour Selector / Pickup Location -->
                    <div id="tourSelectGroup">
                        <label class="block text-xs font-semibold text-slate-700 mb-1">Select Tour Package</label>
                        <select id="tourPackage" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-200 focus:ring-2 focus:ring-amber-500 focus:border-amber-500 text-sm bg-slate-50">
                            <option value="Tour 1: Puri-Konark-Bhubaneswar Full Day (6:30 AM - 6:30 PM)">Tour 1: Puri - Konark - Bhubaneswar (Full Day)</option>
                            <option value="Puri Local & Temple Darshan">Puri Local Sightseeing & Jagannath Temple</option>
                            <option value="Puri to Konark & Satapada Chilika">Puri - Konark & Satapada Chilika Lake</option>
                            <option value="Bhubaneswar Airport/Station Transfer">Airport / Railway Station Transfer</option>
                        </select>
                    </div>

                    <div id="customLocGroup" class="hidden space-y-3">
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 mb-1">Pickup Location</label>
                            <input type="text" id="pickupLoc" placeholder="e.g. Puri Railway Station / Hotel" class="w-full px-3.5 py-2 rounded-xl border border-slate-200 focus:ring-2 focus:ring-amber-500 text-sm">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 mb-1">Drop Location</label>
                            <input type="text" id="dropLoc" placeholder="e.g. Bhubaneswar Airport / Konark" class="w-full px-3.5 py-2 rounded-xl border border-slate-200 focus:ring-2 focus:ring-amber-500 text-sm">
                        </div>
                    </div>

                    <!-- Date & Car Type -->
                    <div class="grid grid-cols-2 gap-3">
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 mb-1">Travel Date</label>
                            <input type="date" id="travelDate" required class="w-full px-3.5 py-2 rounded-xl border border-slate-200 focus:ring-2 focus:ring-amber-500 text-sm bg-slate-50">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 mb-1">Car Type</label>
                            <select id="carType" required class="w-full px-3.5 py-2 rounded-xl border border-slate-200 focus:ring-2 focus:ring-amber-500 text-sm bg-slate-50">
                                <option value="Sedan (Dzire/Etios)">Sedan (Dzire / Etios)</option>
                                <option value="SUV (Ertiga)">SUV (Ertiga)</option>
                                <option value="Luxury SUV (Innova Crysta)">Innova Crysta</option>
                                <option value="Hatchback (Swift/Indica)">Hatchback (Swift/Indica)</option>
                                <option value="Tempo Traveller (13/17 Seater)">Tempo Traveller</option>
                            </select>
                        </div>
                    </div>

                    <!-- Customer Info -->
                    <div>
                        <label class="block text-xs font-semibold text-slate-700 mb-1">Your Name</label>
                        <input type="text" id="custName" placeholder="Enter full name" required class="w-full px-3.5 py-2 rounded-xl border border-slate-200 focus:ring-2 focus:ring-amber-500 text-sm">
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-700 mb-1">Phone / WhatsApp Number</label>
                        <input type="tel" id="custPhone" placeholder="10-digit mobile number" required pattern="[0-9]{10}" class="w-full px-3.5 py-2 rounded-xl border border-slate-200 focus:ring-2 focus:ring-amber-500 text-sm">
                    </div>

                    <button type="submit" class="w-full py-3.5 bg-gradient-to-r from-amber-500 to-orange-600 hover:from-amber-600 hover:to-orange-700 text-white font-bold rounded-xl shadow-lg shadow-orange-500/30 transition-all flex items-center justify-center gap-2 hover:scale-[1.02]">
                        <i class="fa-solid fa-paper-plane"></i> Submit Booking / Get Quote
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- FEATURED TOUR SECTION: TOUR 1 -->
    <section id="tour1" class="py-16 bg-white">
        <div class="container mx-auto px-4 lg:px-8">
            
            <!-- Section Header -->
            <div class="text-center max-w-3xl mx-auto mb-12" data-aos="fade-up">
                <span class="bg-orange-100 text-orange-700 text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wider">Most Popular Sightseeing Package</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-slate-900 mt-3 font-serif-title">
                    Tour 1: Complete Odisha Heritage & Sightseeing
                </h2>
                <p class="text-slate-600 mt-2 text-sm sm:text-base">
                    An all-inclusive 12-hour guided taxi tour covering coastal beaches, ancient UNESCO world heritage temples, peace pagodas, and wildlife sanctuaries.
                </p>
                
                <!-- Quick Info Badges -->
                <div class="flex flex-wrap justify-center gap-4 mt-6">
                    <div class="bg-slate-50 border border-slate-200 px-4 py-2 rounded-xl flex items-center gap-2 text-sm font-semibold text-slate-800">
                        <i class="fa-solid fa-clock text-amber-500"></i> Timing: 6:30 AM to 6:30 PM
                    </div>
                    <div class="bg-red-50 border border-red-200 px-4 py-2 rounded-xl flex items-center gap-2 text-sm font-semibold text-red-700">
                        <i class="fa-solid fa-calendar-xmark text-red-500"></i> Closed On: Mondays
                    </div>
                    <div class="bg-emerald-50 border border-emerald-200 px-4 py-2 rounded-xl flex items-center gap-2 text-sm font-semibold text-emerald-800">
                        <i class="fa-solid fa-car-side text-emerald-600"></i> Doorstep Pickup & Drop
                    </div>
                </div>
            </div>

            <!-- Animated Timeline Itinerary Grid -->
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 relative">
                
                <!-- Card 1: Ramachandi -->
                <div class="bg-slate-50 rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition-all duration-300 group" data-aos="fade-up" data-aos-delay="100">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?q=80&w=800&auto=format&fit=crop" alt="Ramachandi Temple" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-amber-500 text-white text-xs font-bold px-2.5 py-1 rounded-lg">Stop 1</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-amber-600 transition-colors">Ramachandi Temple & Beach</h3>
                        <p class="text-xs text-amber-600 font-medium mb-2">Beautiful confluence of Kushabhadra River & Bay of Bengal</p>
                        <p class="text-slate-600 text-xs leading-relaxed">Enjoy serene morning views, peaceful temple vibes, and optional water sports along the scenic beach.</p>
                    </div>
                </div>

                <!-- Card 2: Chandrabhaga Beach -->
                <div class="bg-slate-50 rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition-all duration-300 group" data-aos="fade-up" data-aos-delay="200">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1544551763-46a013bb70d5?q=80&w=800&auto=format&fit=crop" alt="Chandrabhaga Beach" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-amber-500 text-white text-xs font-bold px-2.5 py-1 rounded-lg">Stop 2</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-amber-600 transition-colors">Chandrabhaga Beach</h3>
                        <p class="text-xs text-amber-600 font-medium mb-2">Clean, Golden Sand Blue Flag Beach</p>
                        <p class="text-slate-600 text-xs leading-relaxed">Famous for its cultural importance, golden sands, and fresh sea breeze close to Konark.</p>
                    </div>
                </div>

                <!-- Card 3: Konark Sun Temple -->
                <div class="bg-slate-50 rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition-all duration-300 group" data-aos="fade-up" data-aos-delay="300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1628155930542-3c7a64e2c833?q=80&w=800&auto=format&fit=crop" alt="Konark Sun Temple" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-amber-500 text-white text-xs font-bold px-2.5 py-1 rounded-lg">Stop 3</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-amber-600 transition-colors">Konark Sun Temple</h3>
                        <p class="text-xs text-amber-600 font-medium mb-2">UNESCO World Heritage Black Pagoda</p>
                        <p class="text-slate-600 text-xs leading-relaxed">Marvel at 13th-century architectural splendor shaped like a giant stone chariot with intricate stone carvings.</p>
                    </div>
                </div>

                <!-- Card 4: Dhauli Peace Pagoda -->
                <div class="bg-slate-50 rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition-all duration-300 group" data-aos="fade-up" data-aos-delay="100">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1609946782102-1c2ec8587b99?q=80&w=800&auto=format&fit=crop" alt="Dhauli Giri" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-amber-500 text-white text-xs font-bold px-2.5 py-1 rounded-lg">Stop 4</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-amber-600 transition-colors">Dhauli Peace Pagoda</h3>
                        <p class="text-xs text-amber-600 font-medium mb-2">Historic Kalinga War Site & Shanti Stupa</p>
                        <p class="text-slate-600 text-xs leading-relaxed">Hilltop white pagoda overlooking Daya River, where Emperor Ashoka embraced Buddhism & non-violence.</p>
                    </div>
                </div>

                <!-- Card 5: Bhubaneswar Temples -->
                <div class="bg-slate-50 rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition-all duration-300 group" data-aos="fade-up" data-aos-delay="200">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1600100397608-f010e423b971?q=80&w=800&auto=format&fit=crop" alt="Bhubaneswar Temples" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-amber-500 text-white text-xs font-bold px-2.5 py-1 rounded-lg">Stop 5</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-amber-600 transition-colors">Bhubaneswar Temples</h3>
                        <p class="text-xs text-amber-600 font-medium mb-2">Lingaraj, Mukteswar & Rajarani Temples</p>
                        <p class="text-slate-600 text-xs leading-relaxed">Visit the Temple City's most iconic sacred shrines showcasing classic Kalinga stone architecture.</p>
                    </div>
                </div>

                <!-- Card 6: Udayagiri, Khandagiri & Nandankanan -->
                <div class="bg-slate-50 rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition-all duration-300 group" data-aos="fade-up" data-aos-delay="300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1534567153574-2b12153a87f0?q=80&w=800&auto=format&fit=crop" alt="Nandankanan Zoo" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <span class="absolute top-3 left-3 bg-amber-500 text-white text-xs font-bold px-2.5 py-1 rounded-lg">Stop 6 & 7</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-amber-600 transition-colors">Udayagiri Caves & Nandankanan Zoo</h3>
                        <p class="text-xs text-amber-600 font-medium mb-2">Ancient Rock-Cut Caves & White Tiger Safari</p>
                        <p class="text-slate-600 text-xs leading-relaxed">Explore historical Jain caves followed by a visit to the famous zoological park & botanical sanctuary.</p>
                    </div>
                </div>

            </div>

            <!-- CTA Banner for Tour 1 -->
            <div class="mt-12 bg-gradient-to-r from-slate-900 via-slate-800 to-slate-900 text-white p-8 rounded-3xl flex flex-wrap items-center justify-between gap-6 shadow-2xl" data-aos="zoom-in">
                <div>
                    <h4 class="text-2xl font-bold font-serif-title text-amber-400">Ready for Tour 1 Experience?</h4>
                    <p class="text-slate-300 text-sm mt-1">Book your private AC cab for 6:30 AM to 6:30 PM full-day tour.</p>
                </div>
                <div class="flex items-center gap-3">
                    <a href="#booking" onclick="quickSelectTour('Tour 1: Puri-Konark-Bhubaneswar Full Day (6:30 AM - 6:30 PM)')" class="bg-amber-500 hover:bg-amber-600 text-slate-900 font-extrabold px-6 py-3 rounded-xl shadow-lg transition-all hover:scale-105 text-sm">
                        Book Tour 1 Now
                    </a>
                    <a href="tel:7978039882" class="border border-white/20 hover:bg-white/10 text-white font-semibold px-5 py-3 rounded-xl transition-all text-sm">
                        <i class="fa-solid fa-phone"></i> Call Driver
                    </a>
                </div>
            </div>

        </div>
    </section>

    <!-- CAR FLEET SHOWCASE -->
    <section id="fleet" class="py-16 bg-slate-50">
        <div class="container mx-auto px-4 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-12" data-aos="fade-up">
                <span class="text-amber-600 font-bold text-xs uppercase tracking-wider">Well Maintained & Clean Cars</span>
                <h2 class="text-3xl font-extrabold text-slate-900 mt-1 font-serif-title">Choose Your Ride</h2>
                <p class="text-slate-600 text-sm mt-2">All types of vehicles available with experienced local drivers for comfortable journeys.</p>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                
                <!-- Sedan -->
                <div class="bg-white rounded-2xl p-5 border border-slate-200/80 shadow-sm hover:shadow-xl transition-all hover:-translate-y-1" data-aos="fade-up" data-aos-delay="100">
                    <div class="h-36 bg-slate-100 rounded-xl mb-4 flex items-center justify-center p-2 relative">
                        <span class="absolute top-2 right-2 bg-emerald-100 text-emerald-800 text-[10px] font-bold px-2 py-0.5 rounded">Most Popular</span>
                        <i class="fa-solid fa-car-side text-6xl text-slate-700"></i>
                    </div>
                    <h3 class="text-lg font-bold text-slate-900">Swift Dzire / Etios</h3>
                    <p class="text-xs text-slate-500 mb-3">Ideal for small families (Up to 4 Passengers)</p>
                    
                    <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 mb-4 bg-slate-50 p-2.5 rounded-lg">
                        <span><i class="fa-solid fa-users text-amber-500 mr-1"></i> 4 Seats</span>
                        <span><i class="fa-solid fa-snowflake text-amber-500 mr-1"></i> Full AC</span>
                        <span><i class="fa-solid fa-suitcase text-amber-500 mr-1"></i> 2 Bags</span>
                        <span><i class="fa-solid fa-shield text-amber-500 mr-1"></i> Sanitized</span>
                    </div>

                    <button onclick="selectCarForBooking('Sedan (Dzire/Etios)')" class="w-full py-2.5 bg-slate-900 hover:bg-amber-500 hover:text-slate-900 text-white rounded-xl font-bold text-xs transition-all">
                        Book Sedan Cab
                    </button>
                </div>

                <!-- SUV Ertiga -->
                <div class="bg-white rounded-2xl p-5 border border-slate-200/80 shadow-sm hover:shadow-xl transition-all hover:-translate-y-1" data-aos="fade-up" data-aos-delay="200">
                    <div class="h-36 bg-slate-100 rounded-xl mb-4 flex items-center justify-center p-2 relative">
                        <span class="absolute top-2 right-2 bg-amber-100 text-amber-800 text-[10px] font-bold px-2 py-0.5 rounded">Best Value</span>
                        <i class="fa-solid fa-van-shuttle text-6xl text-slate-700"></i>
                    </div>
                    <h3 class="text-lg font-bold text-slate-900">Maruti Ertiga (SUV)</h3>
                    <p class="text-xs text-slate-500 mb-3">Perfect for medium groups & long tours</p>
                    
                    <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 mb-4 bg-slate-50 p-2.5 rounded-lg">
                        <span><i class="fa-solid fa-users text-amber-500 mr-1"></i> 6+1 Seats</span>
                        <span><i class="fa-solid fa-snowflake text-amber-500 mr-1"></i> Rear AC</span>
                        <span><i class="fa-solid fa-suitcase text-amber-500 mr-1"></i> 3 Bags</span>
                        <span><i class="fa-solid fa-shield text-amber-500 mr-1"></i> Sanitized</span>
                    </div>

                    <button onclick="selectCarForBooking('SUV (Ertiga)')" class="w-full py-2.5 bg-slate-900 hover:bg-amber-500 hover:text-slate-900 text-white rounded-xl font-bold text-xs transition-all">
                        Book Ertiga SUV
                    </button>
                </div>

                <!-- Innova Crysta -->
                <div class="bg-white rounded-2xl p-5 border border-slate-200/80 shadow-sm hover:shadow-xl transition-all hover:-translate-y-1" data-aos="fade-up" data-aos-delay="300">
                    <div class="h-36 bg-slate-100 rounded-xl mb-4 flex items-center justify-center p-2 relative">
                        <span class="absolute top-2 right-2 bg-purple-100 text-purple-800 text-[10px] font-bold px-2 py-0.5 rounded">Premium Comfort</span>
                        <i class="fa-solid fa-car-rear text-6xl text-slate-700"></i>
                    </div>
                    <h3 class="text-lg font-bold text-slate-900">Innova Crysta</h3>
                    <p class="text-xs text-slate-500 mb-3">Luxury ride with extra legroom & comfort</p>
                    
                    <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 mb-4 bg-slate-50 p-2.5 rounded-lg">
                        <span><i class="fa-solid fa-users text-amber-500 mr-1"></i> 7 Seats</span>
                        <span><i class="fa-solid fa-snowflake text-amber-500 mr-1"></i> Dual AC</span>
                        <span><i class="fa-solid fa-suitcase text-amber-500 mr-1"></i> 4 Bags</span>
                        <span><i class="fa-solid fa-shield text-amber-500 mr-1"></i> Premium</span>
                    </div>

                    <button onclick="selectCarForBooking('Luxury SUV (Innova Crysta)')" class="w-full py-2.5 bg-slate-900 hover:bg-amber-500 hover:text-slate-900 text-white rounded-xl font-bold text-xs transition-all">
                        Book Innova Crysta
                    </button>
                </div>

                <!-- Tempo Traveller -->
                <div class="bg-white rounded-2xl p-5 border border-slate-200/80 shadow-sm hover:shadow-xl transition-all hover:-translate-y-1" data-aos="fade-up" data-aos-delay="400">
                    <div class="h-36 bg-slate-100 rounded-xl mb-4 flex items-center justify-center p-2 relative">
                        <span class="absolute top-2 right-2 bg-blue-100 text-blue-800 text-[10px] font-bold px-2 py-0.5 rounded">Group Travel</span>
                        <i class="fa-solid fa-bus text-6xl text-slate-700"></i>
                    </div>
                    <h3 class="text-lg font-bold text-slate-900">Tempo Traveller</h3>
                    <p class="text-xs text-slate-500 mb-3">For large family groups & joint tours</p>
                    
                    <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 mb-4 bg-slate-50 p-2.5 rounded-lg">
                        <span><i class="fa-solid fa-users text-amber-500 mr-1"></i> 13-17 Seats</span>
                        <span><i class="fa-solid fa-snowflake text-amber-500 mr-1"></i> Roof AC</span>
                        <span><i class="fa-solid fa-suitcase text-amber-500 mr-1"></i> Large Boot</span>
                        <span><i class="fa-solid fa-shield text-amber-500 mr-1"></i> Reclining</span>
                    </div>

                    <button onclick="selectCarForBooking('Tempo Traveller (13/17 Seater)')" class="w-full py-2.5 bg-slate-900 hover:bg-amber-500 hover:text-slate-900 text-white rounded-xl font-bold text-xs transition-all">
                        Book Tempo Traveller
                    </button>
                </div>

            </div>
        </div>
    </section>

    <!-- WHY CHOOSE US & SERVICES -->
    <section id="why-us" class="py-16 bg-white border-t border-slate-100">
        <div class="container mx-auto px-4 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-12 items-center">
                
                <div data-aos="fade-right">
                    <span class="text-amber-600 font-bold text-xs uppercase tracking-wider">Trusted Taxi Provider</span>
                    <h2 class="text-3xl font-extrabold text-slate-900 mt-1 font-serif-title">
                        Why Travelers Prefer <br>Satya Tour and Travels
                    </h2>
                    <p class="text-slate-600 text-sm mt-3 leading-relaxed">
                        We take pride in offering hassle-free, comfortable, and punctual taxi services across Puri, Bhubaneswar, Cuttack, and all iconic tourist destinations in Odisha.
                    </p>

                    <div class="space-y-4 mt-6">
                        <div class="flex items-start gap-4">
                            <div class="w-10 h-10 rounded-xl bg-amber-100 text-amber-600 flex items-center justify-center font-bold shrink-0">
                                <i class="fa-solid fa-clock-rotate-left"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-slate-900 text-base">Always On Time</h4>
                                <p class="text-xs text-slate-500">Punctual pickups at hotel, railway station, or airport without delays.</p>
                            </div>
                        </div>

                        <div class="flex items-start gap-4">
                            <div class="w-10 h-10 rounded-xl bg-orange-100 text-orange-600 flex items-center justify-center font-bold shrink-0">
                                <i class="fa-solid fa-id-card"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-slate-900 text-base">Courteous Local Drivers</h4>
                                <p class="text-xs text-slate-500">Polite, experienced drivers who double up as knowledgeable local guides.</p>
                            </div>
                        </div>

                        <div class="flex items-start gap-4">
                            <div class="w-10 h-10 rounded-xl bg-emerald-100 text-emerald-600 flex items-center justify-center font-bold shrink-0">
                                <i class="fa-solid fa-hand-holding-dollar"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-slate-900 text-base">Transparent Fixed Rates</h4>
                                <p class="text-xs text-slate-500">No surge pricing or hidden charges. Pay standard rates for all tour packages.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="grid grid-cols-2 gap-4" data-aos="fade-left">
                    <div class="bg-amber-50 p-6 rounded-2xl border border-amber-100 text-center">
                        <div class="text-3xl font-extrabold text-amber-600 mb-1">10,000+</div>
                        <div class="text-xs font-semibold text-slate-700">Happy Pilgrims & Tourists</div>
                    </div>
                    <div class="bg-slate-900 text-white p-6 rounded-2xl text-center">
                        <div class="text-3xl font-extrabold text-amber-400 mb-1">24 / 7</div>
                        <div class="text-xs font-semibold text-slate-300">Customer Support</div>
                    </div>
                    <div class="bg-slate-100 p-6 rounded-2xl text-center col-span-2">
                        <div class="text-2xl font-bold text-slate-900 mb-1">Quick Pickup Guaranteed</div>
                        <p class="text-xs text-slate-500">Puri Railway Station • Bhubaneswar Airport • Beach Hotels</p>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-slate-900 text-white pt-12 pb-24 lg:pb-12 border-t border-slate-800">
        <div class="container mx-auto px-4 lg:px-8">
            <div class="grid md:grid-cols-3 gap-8 mb-8">
                
                <div>
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-9 h-9 rounded-xl bg-amber-500 flex items-center justify-center text-slate-900 font-bold text-lg">
                            <i class="fa-solid fa-taxi"></i>
                        </div>
                        <span class="text-xl font-bold text-white">Satya Tour & Travels</span>
                    </div>
                    <p class="text-xs text-slate-400 leading-relaxed mb-4">
                        Your trusted cab booking partner for Puri Jagannath Darshan, Konark Sun Temple tours, Chilika lake trips, and Odisha sightseeing.
                    </p>
                    <div class="text-xs text-amber-400 font-semibold flex items-center gap-2">
                        <i class="fa-solid fa-phone"></i> Direct Booking Hotline: 7978039882
                    </div>
                </div>

                <div>
                    <h4 class="text-sm font-bold text-white uppercase tracking-wider mb-3">Popular Tour Routes</h4>
                    <ul class="text-xs text-slate-400 space-y-2">
                        <li>• Puri to Konark Sun Temple Taxi</li>
                        <li>• Bhubaneswar Airport to Puri Hotel Cab</li>
                        <li>• Tour 1: Full Day Sightseeing (6:30 AM - 6:30 PM)</li>
                        <li>• Satapada Chilika Lake Dolphin Tour</li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-sm font-bold text-white uppercase tracking-wider mb-3">Office Location</h4>
                    <p class="text-xs text-slate-400 mb-2">
                        <i class="fa-solid fa-location-dot text-amber-500 mr-1"></i> Near Jagannath Temple / VIP Road, Puri, Odisha
                    </p>
                    <p class="text-xs text-slate-400 mb-4">
                        <i class="fa-solid fa-envelope text-amber-500 mr-1"></i> satyatourtravels.puri@gmail.com
                    </p>
                    <a href="tel:7978039882" class="inline-block bg-amber-500 hover:bg-amber-600 text-slate-900 px-4 py-2 rounded-xl text-xs font-bold transition-all">
                        Call 7978039882 Now
                    </a>
                </div>

            </div>

            <div class="pt-6 border-t border-slate-800 text-center text-xs text-slate-500">
                © <span id="year"></span> Satya Tour and Travels. All Rights Reserved. Designed for Odisha Tourism.
            </div>
        </div>
    </footer>

    <!-- STICKY MOBILE FLOATING BUTTONS -->
    <div class="fixed bottom-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-md border-t border-slate-200 p-2.5 flex items-center justify-around md:hidden shadow-lg">
        <a href="tel:7978039882" class="flex-1 mr-2 bg-slate-900 text-white py-2.5 rounded-xl text-xs font-bold flex items-center justify-center gap-2 shadow-sm">
            <i class="fa-solid fa-phone text-amber-400"></i> Direct Call
        </a>
        <a href="https://wa.me/917978039882?text=Hi%20Satya%20Tour%20and%20Travels,%20I%20want%20to%20book%20a%20taxi" target="_blank" class="flex-1 ml-2 bg-emerald-600 text-white py-2.5 rounded-xl text-xs font-bold flex items-center justify-center gap-2 shadow-sm">
            <i class="fa-brands fa-whatsapp text-sm"></i> WhatsApp
        </a>
    </div>

    <!-- BOOKING CONFIRMATION MODAL -->
    <div id="bookingModal" class="fixed inset-0 bg-slate-900/60 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl p-6 sm:p-8 max-w-md w-full shadow-2xl relative border border-slate-100 text-center animate-pulse-subtle">
            <div class="w-16 h-16 rounded-full bg-emerald-100 text-emerald-600 mx-auto flex items-center justify-center text-2xl font-bold mb-4">
                <i class="fa-solid fa-circle-check"></i>
            </div>
            
            <h3 class="text-2xl font-bold text-slate-900">Booking Request Sent!</h3>
            <p class="text-xs text-slate-500 mt-1 mb-6">Thank you for choosing Satya Tour and Travels.</p>

            <div id="modalDetails" class="bg-slate-50 rounded-2xl p-4 text-left text-xs space-y-2 mb-6 border border-slate-100">
                <!-- Injected JS Content -->
            </div>

            <div class="space-y-2">
                <a id="whatsappConfirmBtn" href="#" target="_blank" class="w-full py-3 bg-emerald-600 hover:bg-emerald-700 text-white font-bold rounded-xl text-sm flex items-center justify-center gap-2">
                    <i class="fa-brands fa-whatsapp"></i> Confirm on WhatsApp
                </a>
                <button onclick="closeModal()" class="w-full py-2.5 bg-slate-100 text-slate-700 font-semibold rounded-xl text-xs hover:bg-slate-200">
                    Close Window
                </button>
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT CODE -->
    <script>
        // Dynamic Year
        document.getElementById('year').textContent = new Date().getFullYear();

        // Initialize AOS Animation Library
        AOS.init({
            duration: 800,
            once: true,
            easing: 'ease-in-out'
        });

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('.mobile-link').forEach(link => {
            link.addEventListener('click', () => mobileMenu.classList.add('hidden'));
        });

        // Set default minimum date to today
        const today = new Date().toISOString().split('T')[0];
        document.getElementById('travelDate').min = today;

        // Toggle Booking Form Types (Tour Package vs Custom Ride)
        function setBookingType(type) {
            const btnTour = document.getElementById('btnTypeTour');
            const btnCustom = document.getElementById('btnTypeCustom');
            const tourGroup = document.getElementById('tourSelectGroup');
            const customGroup = document.getElementById('customLocGroup');
            const bookingTypeInput = document.getElementById('bookingType');

            if (type === 'tour') {
                btnTour.className = "py-2 rounded-lg bg-amber-500 text-white shadow-sm transition-all";
                btnCustom.className = "py-2 rounded-lg text-slate-600 hover:bg-slate-200 transition-all";
                tourGroup.classList.remove('hidden');
                customGroup.classList.add('hidden');
                bookingTypeInput.value = 'tour';
            } else {
                btnCustom.className = "py-2 rounded-lg bg-amber-500 text-white shadow-sm transition-all";
                btnTour.className = "py-2 rounded-lg text-slate-600 hover:bg-slate-200 transition-all";
                customGroup.classList.remove('hidden');
                tourGroup.classList.add('hidden');
                bookingTypeInput.value = 'custom';
            }
        }

        // Quick Select Specific Tour
        function quickSelectTour(tourName) {
            setBookingType('tour');
            document.getElementById('tourPackage').value = tourName;
        }

        // Quick Select Car Model
        function selectCarForBooking(carName) {
            document.getElementById('carType').value = carName;
            document.getElementById('booking').scrollIntoView({ behavior: 'smooth' });
        }

        // Handle Booking Submission
        function handleBookingSubmit(event) {
            event.preventDefault();

            const name = document.getElementById('custName').value.trim();
            const phone = document.getElementById('custPhone').value.trim();
            const date = document.getElementById('travelDate').value;
            const car = document.getElementById('carType').value;
            const type = document.getElementById('bookingType').value;
            
            let tourOrRoute = '';
            if (type === 'tour') {
                tourOrRoute = document.getElementById('tourPackage').value;
            } else {
                const pick = document.getElementById('pickupLoc').value.trim() || 'Not Specified';
                const drop = document.getElementById('dropLoc').value.trim() || 'Not Specified';
                tourOrRoute = `Pickup: ${pick} | Drop: ${drop}`;
            }

            // Populate Modal Content
            const modalDetails = document.getElementById('modalDetails');
            modalDetails.innerHTML = `
                <p><strong>Name:</strong> ${name}</p>
                <p><strong>Phone:</strong> ${phone}</p>
                <p><strong>Date:</strong> ${date}</p>
                <p><strong>Car Selected:</strong> ${car}</p>
                <p><strong>Package/Route:</strong> ${tourOrRoute}</p>
            `;

            // WhatsApp Message Text Construction
            const waText = encodeURIComponent(
                `*New Taxi Booking Request - Satya Tour & Travels*\n\n` +
                `*Name:* ${name}\n` +
                `*Phone:* ${phone}\n` +
                `*Travel Date:* ${date}\n` +
                `*Car Type:* ${car}\n` +
                `*Details:* ${tourOrRoute}`
            );

            document.getElementById('whatsappConfirmBtn').href = `https://wa.me/917978039882?text=${waText}`;

            // Show Modal
            document.getElementById('bookingModal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('bookingModal').classList.add('hidden');
        }
    </script>
</body>
</html>
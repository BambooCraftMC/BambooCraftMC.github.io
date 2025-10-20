<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BamboocraftMC - The Next Level Minecraft Experience</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Configure Tailwind for Inter font and custom colors -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        'bamboo-green': '#1E5631',
                        'bamboo-light': '#F9ECCA',
                        'bamboo-brown': '#A27035',
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0d0e0d; /* Dark background */
        }
        .hero-background {
            background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://placehold.co/1920x600/1E5631/F9ECCA?text=BAMBOO+FOREST');
            background-size: cover;
            background-position: center;
        }
        .bamboo-gradient {
            background: linear-gradient(135deg, #1E5631 0%, #A27035 100%);
        }
        .bamboo-shadow {
            box-shadow: 0 10px 15px -3px rgba(30, 86, 49, 0.5), 0 4px 6px -2px rgba(30, 86, 49, 0.2);
        }
        /* Specific styling for the Lifesteal/Vanilla icon */
        .lifesteal-icon {
            transform: rotate(45deg);
        }
    </style>
</head>
<body class="text-bamboo-light min-h-screen">

    <!-- Header & Navigation -->
    <header class="bg-gray-900 shadow-xl sticky top-0 z-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <a href="#" class="flex items-center space-x-2 text-2xl font-extrabold text-lime-400">
                <!-- Simple Bamboo Icon SVG -->
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-bamboo-green" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M10 20c0 1.1-.9 2-2 2s-2-.9-2-2v-3c0-1.1.9-2 2-2s2 .9 2 2v3zm4-12c0-1.1-.9-2-2-2s-2 .9-2 2v1c0 1.1.9 2 2 2s2-.9 2-2V8zm-2 10V9h-2v9c0 1.1-.9 2-2 2s-2-.9-2-2v-9h-2v9c0 2.2 1.8 4 4 4s4-1.8 4-4zM16 4v1c0 1.1.9 2 2 2s2-.9 2-2V4c0-1.1-.9-2-2-2s-2 .9-2 2z"/>
                </svg>
                <span>BamboocraftMC</span>
            </a>
            <nav class="hidden md:flex space-x-6">
                <a href="#features" class="text-gray-300 hover:text-lime-400 transition duration-300">Gamemodes</a>
                <a href="#join" class="px-4 py-2 bg-bamboo-green text-bamboo-light rounded-lg hover:bg-lime-600 transition duration-300 font-semibold shadow-md">Play Now</a>
            </nav>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section class="hero-background text-center py-20 md:py-32 rounded-b-2xl mb-12">
            <div class="max-w-4xl mx-auto px-4">
                <h1 class="text-5xl md:text-7xl font-extrabold mb-4 leading-tight text-white drop-shadow-lg">
                    Dual Adventure Awaits. <span class="text-lime-400">Join BamboocraftMC.</span>
                </h1>
                <p class="text-xl md:text-2xl text-gray-200 mb-10">
                    A welcoming, community-focused Java server offering two distinct modes: **Lifesteal PvP** and **Enhanced Survival**. **Zero Economy, Zero Pay-to-Win.**
                </p>

                <!-- Server IP Display & Copy Button -->
                <div class="inline-block p-2 bg-bamboo-light rounded-xl shadow-2xl transform hover:scale-[1.02] transition duration-500">
                    <div class="flex items-center bg-gray-900 rounded-lg p-3 md:p-4 border-2 border-lime-400/50">
                        <span id="server-ip" class="text-xl md:text-3xl font-mono font-bold text-lime-400 select-all mr-4">
                            play.bamboocraftmc.net
                        </span>
                        <button id="copy-button" class="bg-lime-500 text-gray-900 px-4 py-2 rounded-lg font-bold hover:bg-lime-400 transition duration-300 flex items-center shadow-lg">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-1" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M16 1h-4.14c-.65 0-1.28.25-1.76.73L4.73 7.24C4.25 7.72 4 8.35 4 9v12c0 1.1.9 2 2 2h12c1.1 0 2-.9 2-2V3c0-1.1-.9-2-2-2zm0 18H6V9h10v10zm-6-9H8v-2h2v2zm3 0h-2v-2h2v2z"/>
                            </svg>
                            Copy IP
                        </button>
                    </div>
                </div>

                <p id="copy-message" class="mt-4 text-sm text-lime-400 opacity-0 transition-opacity duration-300 h-5"></p>
            </div>
        </section>

        <!-- Features/Gamemodes Section -->
        <section id="features" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
            <h2 class="text-4xl font-bold text-center mb-12 text-bamboo-light">Two Ways to Play: Survival & Lifesteal</h2>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Feature 1: Enhanced Survival -->
                <div class="bg-gray-800 p-8 rounded-xl hover:bamboo-shadow transition duration-500 border-t-4 border-bamboo-green">
                    <div class="text-lime-400 mb-4">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 15h-2v-6h2v6zm0-8h-2V7h2v2z"/></svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-3 text-bamboo-light">Survival (QoL Focused)</h3>
                    <p class="text-gray-400">This is our Quality-of-Life Survival mode. Enjoy the classic game enhanced with essential features like **`/sethome`**, custom teleportation, and land claims to protect your massive builds from griefers. Play cooperatively and build safe.</p>
                </div>

                <!-- Feature 2: Lifesteal (Vanilla Focused) -->
                <div class="bg-gray-800 p-8 rounded-xl hover:bamboo-shadow transition duration-500 border-t-4 border-bamboo-brown">
                    <div class="text-red-500 mb-4 flex justify-center">
                        <!-- Custom heart/PVP icon -->
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10 lifesteal-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
                        </svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-3 text-bamboo-light">Lifesteal (Vanilla PvP)</h3>
                    <p class="text-gray-400">A pure, high-stakes combat experience. This mode is **MUCH more vanilla** with minimal plugins. Health is your currency; kill players to steal hearts and survive. A true test of skill and ruthlessness.</p>
                </div>

                <!-- Feature 3: Dedicated Community -->
                <div class="bg-gray-800 p-8 rounded-xl hover:bamboo-shadow transition duration-500 border-t-4 border-bamboo-green">
                    <div class="text-lime-400 mb-4">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 24 24" fill="currentColor"><path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/></svg>
                    </div>
                    <h3 class="text-2xl font-semibold mb-3 text-bamboo-light">Friendly & Active Staff</h3>
                    <p class="text-gray-400">Our staff team is dedicated to fostering a non-toxic environment across both game modes. Regular events, active Discord support, and fast response times ensure a smooth and fun experience for everyone.</p>
                </div>
            </div>
        </section>

        <!-- Secondary CTA/Join Section -->
        <section id="join" class="bamboo-gradient text-center py-20 mt-12 mb-12 rounded-xl max-w-6xl mx-auto px-4 shadow-2xl">
            <h2 class="text-4xl md:text-5xl font-extrabold mb-4 text-bamboo-light">Ready to choose your adventure?</h2>
            <p class="text-xl text-gray-200 mb-8">
                Whether you prefer peaceful building or competitive PvP, your spot awaits.
            </p>
            <a href="#" onclick="document.getElementById('copy-button').click(); return false;" class="inline-block px-10 py-4 bg-lime-400 text-gray-900 text-xl font-bold rounded-full hover:bg-lime-300 transition duration-300 shadow-xl transform hover:scale-105">
                Copy IP and Join Now!
            </a>
        </section>
    </main>

    <!-- JavaScript for Copy IP functionality -->
    <script>
        const copyButton = document.getElementById('copy-button');
        const serverIp = document.getElementById('server-ip').textContent;
        const copyMessage = document.getElementById('copy-message');

        /**
         * Writes the given text to the clipboard and shows a confirmation message.
         * Uses document.execCommand('copy') for compatibility in embedded environments.
         */
        function copyToClipboard(text) {
            try {
                // Use the modern API if available (though it might be restricted in an iframe)
                if (navigator.clipboard) {
                    navigator.clipboard.writeText(text).then(() => {
                        showCopyMessage("IP Copied!");
                    }).catch(() => {
                        // Fallback to execCommand if modern API fails
                        fallbackCopyTextToClipboard(text);
                    });
                } else {
                    // Fallback for older browsers or restricted environments
                    fallbackCopyTextToClipboard(text);
                }
            } catch (err) {
                console.error('Could not copy text: ', err);
                showCopyMessage("Copy failed. Try selecting the IP manually.", true);
            }
        }

        /**
         * Fallback mechanism using the deprecated but widely compatible execCommand.
         */
        function fallbackCopyTextToClipboard(text) {
            const textArea = document.createElement("textarea");
            textArea.value = text;
            textArea.style.position = "fixed";  // Avoid scrolling to bottom of page
            document.body.appendChild(textArea);
            textArea.focus();
            textArea.select();
            try {
                const successful = document.execCommand('copy');
                if (successful) {
                    showCopyMessage("IP Copied!");
                } else {
                    showCopyMessage("Copy failed. Try selecting the IP manually.", true);
                }
            } catch (err) {
                console.error('Fallback copy failed: ', err);
                showCopyMessage("Copy failed. Try selecting the IP manually.", true);
            }
            document.body.removeChild(textArea);
        }

        /**
         * Displays a temporary confirmation message.
         */
        function showCopyMessage(message, isError = false) {
            copyMessage.textContent = message;
            copyMessage.classList.remove('text-lime-400', 'text-red-500');
            copyMessage.classList.add(isError ? 'text-red-500' : 'text-lime-400', 'opacity-100');
            setTimeout(() => {
                copyMessage.classList.remove('opacity-100');
                copyMessage.classList.add('opacity-0');
            }, 2000);
        }

        // Attach the event listener to the button
        copyButton.addEventListener('click', () => {
            copyToClipboard(serverIp);
        });

    </script>
</body>
</html>

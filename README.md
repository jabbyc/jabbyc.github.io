<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Professional Virtual Assistant</title>
    <!-- Use Inter font for a modern, clean look -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Tailwind configuration for custom colors and font -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        'primary-blue': '#4a75ff',
                        'primary-purple': '#6c63ff',
                        'primary-pink': '#d4499d',
                        'secondary-gray': '#f5f5f7',
                        'dark-text': '#1f2937',
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom CSS for a clean scroll-snap effect and smooth transitions */
        html {
            scroll-behavior: smooth;
        }
        .section-padding {
            padding: 80px 16px;
        }
        /* Style for the button hover effect */
        .btn-hover-effect {
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
        }
        .btn-hover-effect:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
    </style>
</head>

<body class="bg-white font-inter text-dark-text">

    <!-- Header & Hero Section -->
    <header class="w-full min-h-screen flex items-center justify-center p-4 text-center text-white bg-gradient-to-br from-primary-blue via-primary-purple to-primary-pink rounded-b-[50px] md:rounded-b-[100px] lg:rounded-b-[150px]">
        <div class="container mx-auto max-w-4xl py-12 px-4 md:px-8">
            <h1 class="text-4xl sm:text-5xl md:text-6xl font-bold mb-4 leading-tight">Your Professional Virtual Assistant & Ebook Author</h1>
            <p class="text-lg sm:text-xl md:text-2xl font-light mb-8">
                I help you streamline your life and business, freeing up your time to focus on what truly matters.
            </p>
            <a href="#contact" class="inline-block bg-white text-primary-purple font-semibold text-lg py-3 px-8 rounded-full shadow-lg hover:bg-gray-100 btn-hover-effect">
                Get in Touch
            </a>
        </div>
    </header>

    <!-- Services Section -->
    <section id="services" class="section-padding bg-secondary-gray">
        <div class="container mx-auto max-w-6xl px-4">
            <h2 class="text-3xl sm:text-4xl font-bold text-center mb-12 text-dark-text">Virtual Assistant Services</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="bg-white p-6 rounded-2xl shadow-md btn-hover-effect">
                    <div class="flex items-center justify-center w-12 h-12 mb-4 bg-primary-blue rounded-full">
                        <!-- SVG for Administrative Support -->
                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2m-2 2h4m-4 0v2m0-2v2m-2-2h4m-4 0v2m0-2v2m-2-2h4m-4 0v2"></path></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Administrative Support</h3>
                    <p class="text-gray-600">
                        Managing schedules, email correspondence, data entry, and other essential administrative tasks.
                    </p>
                </div>
                <!-- Service 2 -->
                <div class="bg-white p-6 rounded-2xl shadow-md btn-hover-effect">
                    <div class="flex items-center justify-center w-12 h-12 mb-4 bg-primary-purple rounded-full">
                        <!-- SVG for Social Media Management -->
                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Social Media Management</h3>
                    <p class="text-gray-600">
                        Scheduling posts, community engagement, content planning, and platform analytics.
                    </p>
                </div>
                <!-- Service 3 -->
                <div class="bg-white p-6 rounded-2xl shadow-md btn-hover-effect">
                    <div class="flex items-center justify-center w-12 h-12 mb-4 bg-primary-pink rounded-full">
                        <!-- SVG for Content Creation -->
                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.572L15.232 5.232z"></path></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Content Creation</h3>
                    <p class="text-gray-600">
                        Drafting blog posts, articles, newsletters, and compelling website copy.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Ebooks Section -->
    <section id="ebooks" class="section-padding">
        <div class="container mx-auto max-w-6xl px-4">
            <h2 class="text-3xl sm:text-4xl font-bold text-center mb-12 text-dark-text">My Ebooks</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
                <!-- Ebook 1 -->
                <div class="bg-white p-6 rounded-2xl shadow-lg border border-gray-100 btn-hover-effect">
                    <img src="https://placehold.co/400x600/6c63ff/ffffff?text=Ebook+Cover+1" alt="Ebook Cover" class="w-full h-auto rounded-lg mb-4 shadow-sm">
                    <h3 class="text-xl font-semibold mb-2">The Ultimate VA Guide</h3>
                    <p class="text-gray-600 mb-4">
                        A comprehensive guide to starting and thriving in your virtual assistant career.
                    </p>
                    <a href="#" class="block text-center bg-primary-blue text-white font-semibold py-3 px-6 rounded-full hover:bg-primary-purple transition-colors">
                        Buy Now
                    </a>
                </div>
                <!-- Ebook 2 -->
                <div class="bg-white p-6 rounded-2xl shadow-lg border border-gray-100 btn-hover-effect">
                    <img src="https://placehold.co/400x600/d4499d/ffffff?text=Ebook+Cover+2" alt="Ebook Cover" class="w-full h-auto rounded-lg mb-4 shadow-sm">
                    <h3 class="text-xl font-semibold mb-2">Marketing Your Ebooks</h3>
                    <p class="text-gray-600 mb-4">
                        Learn the best strategies to market your digital products and reach a wider audience.
                    </p>
                    <a href="#" class="block text-center bg-primary-blue text-white font-semibold py-3 px-6 rounded-full hover:bg-primary-purple transition-colors">
                        Buy Now
                    </a>
                </div>
                <!-- Ebook 3 -->
                <div class="bg-white p-6 rounded-2xl shadow-lg border border-gray-100 btn-hover-effect">
                    <img src="https://placehold.co/400x600/4a75ff/ffffff?text=Ebook+Cover+3" alt="Ebook Cover" class="w-full h-auto rounded-lg mb-4 shadow-sm">
                    <h3 class="text-xl font-semibold mb-2">Productivity Hacks for VAs</h3>
                    <p class="text-gray-600 mb-4">
                        Unlock your full potential with proven productivity techniques for virtual assistants.
                    </p>
                    <a href="#" class="block text-center bg-primary-blue text-white font-semibold py-3 px-6 rounded-full hover:bg-primary-purple transition-colors">
                        Buy Now
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Me Section -->
    <section id="about" class="section-padding bg-secondary-gray">
        <div class="container mx-auto max-w-4xl px-4 text-center">
            <h2 class="text-3xl sm:text-4xl font-bold mb-6 text-dark-text">About Me</h2>
            <img src="https://placehold.co/200x200/ffffff/000000?text=Your+Photo" alt="Your Photo" class="w-36 h-36 rounded-full mx-auto mb-6 border-4 border-white shadow-lg">
            <p class="text-gray-600 text-lg leading-relaxed">
                Hi, I'm [Your Name]! With a passion for organization and a knack for creating engaging content,
                I've dedicated my career to helping entrepreneurs and small businesses succeed. As a virtual assistant,
                I handle the behind-the-scenes work so you can focus on your core mission. As an author, I've
                translated my knowledge into practical ebooks designed to help you grow. I'm excited to partner with you!
            </p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section-padding bg-white">
        <div class="container mx-auto max-w-3xl px-4 text-center">
            <h2 class="text-3xl sm:text-4xl font-bold mb-6 text-dark-text">Let's Connect</h2>
            <p class="text-gray-600 mb-8 text-lg">
                Ready to take the next step? Fill out the form below to discuss your needs or ask a question.
            </p>
            
            <form id="contact-form" class="space-y-6">
                <div>
                    <input type="text" id="name" name="name" placeholder="Your Name" class="w-full p-4 rounded-xl border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary-purple transition-colors" required>
                </div>
                <div>
                    <input type="email" id="email" name="email" placeholder="Your Email" class="w-full p-4 rounded-xl border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary-purple transition-colors" required>
                </div>
                <div>
                    <textarea id="message" name="message" rows="5" placeholder="Your Message" class="w-full p-4 rounded-xl border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary-purple transition-colors" required></textarea>
                </div>
                <button type="submit" class="w-full bg-primary-pink text-white font-semibold py-4 px-6 rounded-full hover:bg-primary-purple btn-hover-effect">
                    Send Message
                </button>
                <div id="form-message" class="mt-4 text-center text-green-600 font-semibold hidden">
                    Thank you! Your message has been received. I will get back to you shortly.
                </div>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark-text text-gray-400 py-8">
        <div class="container mx-auto px-4 text-center">
            <p>&copy; 2024 Your Name. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Get the form element and message div
        const form = document.getElementById('contact-form');
        const messageDiv = document.getElementById('form-message');

        // Listen for the form submission
        form.addEventListener('submit', function(event) {
            // Prevent the default form submission action
            event.preventDefault();

            // In a real-world scenario, you would send the form data to a server here.
            // For this example, we'll just show a success message.
            
            // Hide the form and show the success message
            form.classList.add('hidden');
            messageDiv.classList.remove('hidden');
        });
    </script>

</body>
</html>

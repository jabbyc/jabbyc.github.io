# Advising Profile Website – Full Code & Setup (Frontend + Email Relay Backend)

A colorful, high‑detail, fast website with an email relay + autoresponder. Built as a lightweight static frontend (HTML + Tailwind + vanilla JS) + secure Node/Express backend using Nodemailer.

> ✅ You can deploy the frontend as static hosting and the backend on Render/Railway/Vercel (Serverless) or a VPS. The contact form sends you an email and auto‑replies to the sender.

---

## 1) Project Structure

```
my-advising-site/
├─ frontend/
│  ├─ index.html
│  ├─ assets/
│  │  ├─ profile.jpg              # your profile photo
│  │  ├─ ebook-cover.png          # "Ashes of Us" cover
│  │  └─ services-poster.png      # Fastwork Services poster
│  └─ /favicon.ico (optional)
└─ backend/
   ├─ server.js
   ├─ package.json
   ├─ .env.example
   └─ emailTemplates/
      ├─ ownerNotification.html
      └─ userAutoReply.html
```

Place your provided files as:

* `frontend/assets/ebook-cover.png`  ← **Ashes of Us** cover you sent.
* `frontend/assets/services-poster.png`  ← your services poster.
* `frontend/assets/profile.jpg`  ← your profile picture.

---

## 2) FRONTEND – `frontend/index.html`

> A single-page site with smooth section navigation: Home, About, Services, Ebook, Contact. Colorful gradient header, glassy cards, and accessible design. Tailwind via CDN for simplicity.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Brian Wambugu – Advisor</title>
  <meta name="description" content="Advising, typing, assignments, CV writing, and ebook 'Ashes of Us'." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { sans: ['Poppins', 'ui-sans-serif', 'system-ui'] },
          colors: {
            primary: '#7C3AED',         // purple
            secondary: '#06B6D4',       // cyan
            accent: '#F97316',          // orange
            dark: '#0B1020'
          },
          boxShadow: {
            glow: '0 10px 30px rgba(124,58,237,0.4)'
          },
          backgroundImage: theme => ({
            hero: 'radial-gradient(1200px 600px at 20% -10%, rgba(124,58,237,0.35), transparent), radial-gradient(1000px 500px at 90% 10%, rgba(6,182,212,0.35), transparent), linear-gradient(180deg, #0B1020 0%, #0B1020 60%, #111827 100%)'
          })
        }
      }
    }
  </script>
  <style>
    html { scroll-behavior: smooth; }
    .glass { backdrop-filter: blur(10px); background: rgba(255,255,255,0.06); border: 1px solid rgba(255,255,255,0.12); }
  </style>
</head>
<body class="bg-dark text-white font-sans">
  <!-- NAVBAR -->
  <header class="fixed top-0 left-0 right-0 z-50 bg-black/40 glass">
    <nav class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 flex items-center justify-between h-16">
      <a href="#home" class="font-bold tracking-wide text-white"><span class="text-secondary">Brian</span> Wambugu</a>
      <div class="hidden md:flex items-center gap-6 text-sm">
        <a href="#about" class="hover:text-secondary">About</a>
        <a href="#services" class="hover:text-secondary">Services</a>
        <a href="#ebook" class="hover:text-secondary">Ebook</a>
        <a href="#contact" class="hover:text-secondary">Contact</a>
        <a href="#contact" class="ml-3 inline-block bg-primary px-4 py-2 rounded-xl hover:shadow-glow transition">Hire Me</a>
      </div>
      <button id="menuBtn" class="md:hidden p-2 rounded-lg bg-white/10">☰</button>
    </nav>
    <div id="mobileMenu" class="md:hidden hidden px-6 pb-4 space-y-2">
      <a href="#about" class="block py-2">About</a>
      <a href="#services" class="block py-2">Services</a>
      <a href="#ebook" class="block py-2">Ebook</a>
      <a href="#contact" class="block py-2">Contact</a>
    </div>
  </header>

  <!-- HERO -->
  <section id="home" class="bg-hero pt-28 pb-20">
    <div class="mx-auto max-w-7xl px-4 grid md:grid-cols-2 gap-10 items-center">
      <div>
        <h1 class="text-4xl sm:text-5xl font-extrabold leading-tight">
          Colorful Advising & <span class="text-secondary">Fastwork</span>
        </h1>
        <p class="mt-4 text-white/80 max-w-prose">I help students and professionals with typing, assignment help, and CV writing. Get quick support and a friendly experience. Pay via PayPal or M‑PESA.</p>
        <div class="mt-6 flex gap-3">
          <a href="#services" class="bg-primary px-5 py-3 rounded-xl hover:shadow-glow">View Services</a>
          <a href="#ebook" class="bg-white/10 px-5 py-3 rounded-xl hover:bg-white/20">See Ebook</a>
        </div>
      </div>
      <div class="relative">
        <div class="absolute -inset-4 bg-gradient-to-tr from-primary via-secondary to-accent rounded-3xl blur-xl opacity-40"></div>
        <div class="relative glass rounded-3xl p-2">
          <img src="assets/profile.jpg" alt="Brian Wambugu" class="rounded-2xl w-full object-cover"/>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" class="py-20 bg-gradient-to-b from-[#111827] to-[#0B1020]">
    <div class="mx-auto max-w-7xl px-4 grid md:grid-cols-2 gap-10 items-center">
      <div>
        <h2 class="text-3xl font-bold">About Me</h2>
        <p class="mt-4 text-white/80">I'm Brian Wambugu, an advisor focused on fast turnaround and clear communication. I also author fiction, including <em>Ashes of Us</em>. I value honesty, speed, and quality.</p>
        <ul class="mt-4 space-y-2 text-white/80 list-disc list-inside">
          <li>Reliable and responsive support</li>
          <li>Clean, modern deliverables</li>
          <li>Pay securely via PayPal or M‑PESA</li>
        </ul>
      </div>
      <div class="glass rounded-3xl p-4">
        <img src="assets/services-poster.png" alt="Services Poster" class="rounded-2xl w-full object-cover"/>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services" class="py-20 bg-[#0B1020]">
    <div class="mx-auto max-w-7xl px-4">
      <h2 class="text-3xl font-bold mb-8">Services</h2>
      <div class="grid md:grid-cols-3 gap-6">
        <div class="glass rounded-2xl p-6">
          <h3 class="font-semibold text-xl">Typing Services</h3>
          <p class="mt-2 text-white/80">Accurate typing, formatting, and clean PDFs or Docs.</p>
        </div>
        <div class="glass rounded-2xl p-6">
          <h3 class="font-semibold text-xl">Assignment Help</h3>
          <p class="mt-2 text-white/80">Guidance, structuring, and polishing to meet rubrics.</p>
        </div>
        <div class="glass rounded-2xl p-6">
          <h3 class="font-semibold text-xl">CV Writing</h3>
          <p class="mt-2 text-white/80">Professional CVs and cover letters that get noticed.</p>
        </div>
      </div>
      <div class="mt-8 flex flex-wrap items-center gap-4 text-white/80">
        <span class="px-3 py-1 rounded-full bg-white/10">PayPal Accepted</span>
        <span class="px-3 py-1 rounded-full bg-white/10">M‑PESA Accepted</span>
      </div>
    </div>
  </section>

  <!-- EBOOK -->
  <section id="ebook" class="py-20 bg-gradient-to-b from-[#0B1020] to-[#111827]">
    <div class="mx-auto max-w-7xl px-4 grid md:grid-cols-2 gap-10 items-center">
      <div class="glass rounded-3xl p-4">
        <img src="assets/ebook-cover.png" alt="Ashes of Us – Cover" class="rounded-2xl w-full object-cover"/>
      </div>
      <div>
        <h2 class="text-3xl font-bold">Ebook: Ashes of Us</h2>
        <p class="mt-4 text-white/80">Romantic suspense set in a post‑apocalyptic world. Intrigue, survival, and love against the odds.</p>
        <div class="mt-6 flex gap-3">
          <a href="#contact" class="bg-primary px-5 py-3 rounded-xl hover:shadow-glow">Request a Copy</a>
          <a href="#contact" class="bg-white/10 px-5 py-3 rounded-xl hover:bg-white/20">Ask a Question</a>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="py-20 bg-[#0B1020]">
    <div class="mx-auto max-w-3xl px-4">
      <h2 class="text-3xl font-bold">Contact</h2>
      <p class="mt-2 text-white/80">Fill the form and I’ll auto‑acknowledge instantly, then reply personally.</p>

      <form id="contactForm" class="mt-6 glass rounded-2xl p-6 space-y-4" novalidate>
        <div>
          <label class="block text-sm mb-1" for="name">Your Name</label>
          <input id="name" name="name" type="text" required class="w-full px-4 py-3 rounded-xl bg-white/10 focus:outline-none focus:ring-2 focus:ring-secondary" placeholder="John Doe"/>
        </div>
        <div>
          <label class="block text-sm mb-1" for="email">Email</label>
          <input id="email" name="email" type="email" required class="w-full px-4 py-3 rounded-xl bg-white/10 focus:outline-none focus:ring-2 focus:ring-secondary" placeholder="john@example.com"/>
        </div>
        <div>
          <label class="block text-sm mb-1" for="subject">Subject</label>
          <input id="subject" name="subject" type="text" required class="w-full px-4 py-3 rounded-xl bg-white/10 focus:outline-none focus:ring-2 focus:ring-secondary" placeholder="Service inquiry / Ebook / Other"/>
        </div>
        <div>
          <label class="block text-sm mb-1" for="message">Message</label>
          <textarea id="message" name="message" rows="5" required class="w-full px-4 py-3 rounded-xl bg-white/10 focus:outline-none focus:ring-2 focus:ring-secondary" placeholder="Tell me what you need…"></textarea>
        </div>
        <input type="hidden" id="honeypot" name="company" value="" />
        <button class="bg-gradient-to-r from-primary via-secondary to-accent px-6 py-3 rounded-xl font-semibold" type="submit">Send Message</button>
        <p id="status" class="text-sm mt-2"></p>
      </form>

      <p class="text-white/70 mt-6 text-sm">Direct email: <a id="directEmail" href="#" class="underline">(click to reveal)</a></p>
    </div>
  </section>

  <footer class="py-8 text-center text-white/60 bg-black/40">
    © <span id="year"></span> Brian Wambugu. All rights reserved.
  </footer>

  <script>
    // Mobile menu toggle
    document.getElementById('menuBtn').addEventListener('click', () => {
      document.getElementById('mobileMenu').classList.toggle('hidden');
    });

    // Direct email reveal (simple obfuscation against bots)
    const directEmail = document.getElementById('directEmail');
    const user = 'brian';
    const domain = 'example.com'; // TODO: replace with your real domain email
    directEmail.addEventListener('click', (e) => {
      e.preventDefault();
      directEmail.textContent = `${user}@${domain}`;
      directEmail.href = `mailto:${user}@${domain}`;
    });

    // Contact form handler
    const form = document.getElementById('contactForm');
    const statusEl = document.getElementById('status');

    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      statusEl.textContent = 'Sending…';

      //
```

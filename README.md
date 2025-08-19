{{CODE\_BLOCK\_START}}

\<\!DOCTYPE html\>

\<html lang="en"\>
\<head\>
\<meta charset="UTF-8"\>
\<meta name="viewport" content="width=device-width, initial-scale=1.0"\>
\<title\>Brian Wambugu - Freelance Transcription, Writing & Graphic Design\</title\>
\<meta name="description" content="Professional freelance transcription, writing, and graphic design services by Brian Wambugu in Kenya. Get accurate transcripts, compelling content, and stunning visuals to elevate your projects."\>
\<meta property="og:title" content="Brian Wambugu - Freelance Transcription, Writing & Graphic Design"\>
\<meta property="og:description" content="Professional freelance transcription, writing, and graphic design services by Brian Wambugu in Kenya. Get accurate transcripts, compelling content, and stunning visuals to elevate your projects."\>
\<meta property="og:type" content="website"\>
\<meta property="og:url" content="[https://brianwambugu.github.io/](https://www.google.com/search?q=https://brianwambugu.github.io/)"\> \<meta property="og:image" content="[https://images.unsplash.com/photo-1553799903-597b9419f86c?q=80\&w=3270\&auto=format\&fit=crop\&ixlib=rb-4.0.3\&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D](https://www.google.com/url?sa=E&source=gmail&q=https://images.unsplash.com/photo-1553799903-597b9419f86c?q=80%26w=3270%26auto=format%26fit=crop%26ixlib=rb-4.0.3%26ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)"\> \<meta name="twitter:card" content="summary\_large\_image"\>
\<meta name="twitter:title" content="Brian Wambugu - Freelance Transcription, Writing & Graphic Design"\>
\<meta name="twitter:description" content="Professional freelance transcription, writing, and graphic design services by Brian Wambugu in Kenya. Get accurate transcripts, compelling content, and stunning visuals to elevate your projects."\>
\<meta name="twitter:image" content="[https://images.unsplash.com/photo-1553799903-597b9419f86c?q=80\&w=3270\&auto=format\&fit=crop\&ixlib=rb-4.0.3\&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fA%3D%3D](https://www.google.com/search?q=https://images.unsplash.com/photo-1553799903-597b9419f86c%3Fq%3D80%26w%3D3270%26auto%3Dformat%26fit%3Dcrop%26ixlib%3Drb-4.0.3%26ixid%3DM3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fA%253D%253D)"\> \<link rel="icon" href="data:image/svg+xml,\<svg xmlns=%22[http://www.w3.org/2000/svg%22](https://www.google.com/search?q=http://www.w3.org/2000/svg%2522) viewBox=%220 0 100 100%22\>\<text y=%22.9em%22 font-size=%2290%22\>✍️\</text\>\</svg\>"\> \<style\>
/\* Mini Style Guide:
\--color-dark: \#121212;
\--color-green: \#16a34a;
\--color-text-primary: \#f4f4f4;
\--color-text-secondary: \#a1a1aa;
\--spacing-sm: 1rem;
\--spacing-md: 2rem;
\--spacing-lg: 3rem;
\--border-radius: 1rem;
\--box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
\*/

```
    *, *::before, *::after {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
    }

    html {
        scroll-behavior: smooth;
        font-size: 16px;
    }

    body {
        font-family: sans-serif;
        background-color: var(--color-dark);
        color: var(--color-text-primary);
        line-height: 1.6;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }

    /* Typography */
    h1, h2, h3 {
        font-weight: 700;
        line-height: 1.2;
        margin-bottom: var(--spacing-md);
    }

    h1 {
        font-size: 2.5rem;
    }

    h2 {
        font-size: 2rem;
    }

    h3 {
        font-size: 1.5rem;
    }

    p {
        margin-bottom: var(--spacing-sm);
        color: var(--color-text-secondary);
    }

    a {
        color: var(--color-green);
        text-decoration: none;
        transition: color 0.3s ease;
    }

    a:hover {
        color: #107c33;
    }

    /* Layout & Structure */
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: var(--spacing-lg);
    }

    section {
        padding: var(--spacing-lg) 0;
    }

    /* Header & Navigation */
    header {
        position: sticky;
        top: 0;
        background-color: rgba(18, 18, 18, 0.9);
        backdrop-filter: blur(10px);
        z-index: 100;
        padding: var(--spacing-sm) 0;
    }

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 var(--spacing-lg);
    }

    .brand {
        font-size: 1.5rem;
        font-weight: 700;
    }

    .nav-links {
        list-style: none;
        display: none; /* Hide on mobile */
    }

    .nav-links li {
        display: inline;
        margin-left: var(--spacing-md);
    }

    .nav-links li:first-child {
        margin-left: 0;
    }

    .mobile-menu-button {
        display: block; /* Show on mobile */
        background: none;
        border: none;
        color: var(--color-text-primary);
        font-size: 1.5rem;
        cursor: pointer;
    }

    .mobile-menu {
        display: none;
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background-color: var(--color-dark);
        padding: var(--spacing-md);
        text-align: center;
        box-shadow: var(--box-shadow);
    }

    .mobile-menu.open {
        display: block;
    }

    .mobile-menu a {
        display: block;
        padding: var(--spacing-sm) 0;
        border-bottom: 1px solid #222;
    }

    .mobile-menu a:last-child {
        border-bottom: none;
    }

    @media (min-width: 768px) {
        .nav-links {
            display: block;
        }

        .mobile-menu-button {
            display: none;
        }
    }

    /* Hero Section */
    #hero {
        position: relative;
        overflow: hidden;
        padding: 6rem 0;
        display: flex;
        align-items: center;
        justify-content: center;
        min-height: 80vh;
    }

    #hero::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url([https://images.unsplash.com/photo-1553799903-597b9419f86c?q=80&w=3270&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D](https://images.unsplash.com/photo-1553799903-597b9419f86c?q=80&w=3270&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D));
        background-size: cover;
        background-position: center;
        opacity: 0.3;
        z-index: -1;
    }

    .hero-content {
        text-align: center;
        padding: 0 var(--spacing-lg);
        max-width: 800px;
    }

    .hero-content h1 {
        font-size: 3rem;
        margin-bottom: var(--spacing-sm);
    }

    .hero-content p {
        font-size: 1.2rem;
        margin-bottom: var(--spacing-lg);
    }

    .hero-ctas {
        display: flex;
        justify-content: center;
        gap: var(--spacing-sm);
        margin-bottom: var(--spacing-lg);
    }

    .hero-ctas a {
        display: inline-block;
        padding: 1rem 2rem;
        border-radius: var(--border-radius);
        font-weight: 500;
        transition: background-color 0.3s ease;
    }

    .hero-ctas a.primary-cta {
        background-color: var(--color-green);
        color: var(--color-text-primary);
    }

    .hero-ctas a.primary-cta:hover {
        background-color: #107c33;
    }

    .hero-ctas a.secondary-cta {
        border: 1px solid var(--color-green);
        color: var(--color-green);
    }

    .hero-ctas a.secondary-cta:hover {
        background-color: rgba(22, 163, 74, 0.1);
    }

    .trust-badges {
        display: flex;
        justify-content: center;
        gap: var(--spacing-sm);
    }

    .trust-badge {
        background-color: #222;
        color: var(--color-text-secondary);
        padding: 0.5rem 1rem;
        border-radius: calc(var(--border-radius) / 2);
        font-size: 0.8rem;
    }

    /* Logos/Trust Strip */
    #logos {
        padding: var(--spacing-md) 0;
        background-color: #222;
        text-align: center;
        color: var(--color-text-secondary);
        font-size: 0.9rem;
    }

    .logo-strip {
        display: flex;
        justify-content: space-around;
        align-items: center;
        max-width: 900px;
        margin: 0 auto;
        padding: var(--spacing-sm) var(--spacing-lg);
        opacity: 0.5;
    }

    .logo-placeholder {
        width: 80px;
        height: 30px;
        background-color: #333;
        border-radius: calc(var(--border-radius) / 4);
    }

    /* Services Section */
    #services {
        text-align: center;
    }

    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: var(--spacing-lg);
        margin-top: var(--spacing-lg);
    }

    .service-card {
        background-color: #222;
        padding: var(--spacing-md);
        border-radius: var(--border-radius);
        box-shadow: var(--box-shadow);
        text-align: left;
    }

    .service-card img {
        width: 100%;
        height: auto;
        border-radius: calc(var(--border-radius) / 2);
        margin-bottom: var(--spacing-sm);
        display: block;
    }

    .service-card h3 {
        margin-top: 0;
        margin-bottom: var(--spacing-sm);
    }

    .service-card ul {
        list-style: none;
        padding-left: 0;
        color: var(--color-text-secondary);
    }

    .service-card ul li {
        margin-bottom: 0.5rem;
        display: flex;
        align-items: center;
    }

    .service-card ul li::before {
        content: "✔";
        color: var(--color-green);
        margin-right: 0.5rem;
    }

    .service-price {
        margin-top: var(--spacing-sm);
        font-weight: 500;
        color: var(--color-green);
    }

    /* Featured Work / Portfolio */
    #work {
        text-align: center;
    }

    .portfolio-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: var(--spacing-md);
        margin-top: var(--spacing-lg);
    }

    .portfolio-item {
        position: relative;
        overflow: hidden;
        border-radius: var(--border-radius);
        box-shadow: var(--box-shadow);
        cursor: pointer;
    }

    .portfolio-item img {
        width: 100%;
        height: auto;
        display: block;
        transition: transform 0.3s ease-in-out;
    }

    .portfolio-item:hover img {
        transform: scale(1.05);
    }

    .portfolio-overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(18, 18, 18, 0.8);
        display: flex;
        align-items: center;
        justify-content: center;
        opacity: 0;
        transition: opacity 0.3s ease-in-out;
    }

    .portfolio-item:hover .portfolio-overlay {
        opacity: 1;
    }

    .portfolio-caption {
        color: var(--color-text-primary);
        text-align: center;
        padding: var(--spacing-md);
    }

    .portfolio-caption h4 {
        font-size: 1.2rem;
        margin-bottom: 0.5rem;
    }

    .portfolio-modal {
        display: none;
        position: fixed;
        z-index: 1000;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        overflow: auto;
        background-color: rgba(0, 0, 0, 0.9);
    }

    .modal-content {
        position: relative;
        background-color: #fefefe;
        margin: 15% auto;
        padding: var(--spacing-lg);
        border: 1px solid #888;
        width: 80%;
        border-radius: var(--border-radius);
        color: var(--color-dark);
    }

    .close-button {
        color: #aaa;
        position: absolute;
        top: 10px;
        right: 20px;
        font-size: 2rem;
        font-weight: bold;
        cursor: pointer;
    }

    .modal-image {
        width: 100%;
        height: auto;
        border-radius: calc(var(--border-radius) / 2);
    }

    /* Testimonials */
    #testimonials {
        background-color: #222;
        text-align: center;
    }

    .testimonials-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: var(--spacing-lg);
        margin-top: var(--spacing-lg);
    }

    .testimonial-card {
        background-color: #333;
        padding: var(--spacing-md);
        border-radius: var(--border-radius);
        box-shadow: var(--box-shadow);
        text-align: left;
    }

    .testimonial-avatar {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        object-fit: cover;
        margin-bottom: var(--spacing-sm);
    }

    .testimonial-quote {
        font-style: italic;
        margin-bottom: var(--spacing-sm);
        color: var(--color-text-secondary);
    }

    .testimonial-author {
        font-weight: 500;
        color: var(--color-text-primary);
        margin-bottom: 0.25rem;
    }

    .testimonial-meta {
        font-size: 0.9rem;
        color: var(--color-text-secondary);
    }

    .star-rating {
        color: gold;
        font-size: 1rem;
    }

    /* Pricing */
    #pricing {
        text-align: center;
    }

    .pricing-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: var(--spacing-lg);
        margin-top: var(--spacing-lg);
    }

    .pricing-card {
        background-color: #222;
        padding: var(--spacing-md);
        border-radius: var(--border-radius);
        box-shadow: var(--box-shadow);
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .pricing-card.featured {
        background-color: var(--color-green);
        color: var(--color-text-primary);
        transform: scale(1.05);
        transition: transform 0.3s ease-in-out;
    }

    .pricing-card.featured * {
        color: var(--color-text-primary);
    }

    .pricing-title {
        font-size: 1.5rem;
        margin-bottom: var(--spacing-sm);
    }

    .pricing-price {
        font-size: 2rem;
        font-weight: 700;
        margin-bottom: var(--spacing-sm);
    }

    .pricing-price span {
        font-size: 1rem;
        color: var(--color-text-secondary);
    }

    .pricing-includes {
        list-style: none;
        padding-left: 0;
        margin-bottom: var(--spacing-md);
        color: var(--color-text-secondary);
    }

    .pricing-includes li {
        margin-bottom: 0.5rem;
    }

    .pricing-includes li::before {
        content: "✔";
        color: var(--color-green);
        margin-right: 0.5rem;
    }

    .pricing-button {
        display: inline-block;
        padding: 1rem 2rem;
        border-radius: var(--border-radius);
        background-color: #333;
        color: var(--color-text-primary);
        text-decoration: none;
        font-weight: 500;
        transition: background-color 0.3s ease;
        cursor: pointer;
        border: none;
    }

    .pricing-card.featured .pricing-button {
        background-color: #107c33;
    }

    .pricing-button:hover {
        background-color: #444;
    }

    .pricing-card.featured .pricing-button:hover {
        background-color: #0d6629;
    }

    /* About */
    #about {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: var(--spacing-lg);
        align-items: center;
    }

    .about-image {
        border-radius: var(--border-radius);
        box-shadow: var(--box-shadow);
        overflow: hidden;
    }

    .about-image img {
        width: 100%;
        height: auto;
        display: block;
    }

    .about-content {
        padding: 0 var(--spacing-md);
    }

    /* FAQ */
    #faq {
        background-color: #222;
        text-align: center;
    }

    .faq-accordion {
        margin-top: var(--spacing-lg);
        max-width: 800px;
        margin-left: auto;
        margin-right: auto;
    }

    .faq-item {
        margin-bottom: 1rem;
        border: 1px solid #333;
        border-radius: calc(var(--border-radius) / 2);
        overflow: hidden;
    }

    .faq-question {
        background-color: #333;
        color: var(--color-text-primary);
        padding: var(--spacing-sm);
        display: flex;
        justify-content: space-between;
        align-items: center;
        cursor: pointer;
        font-weight: 500;
    }

    .faq-question::after {
        content: "+";
        font-size: 1.2rem;
    }

    .faq-question.open::after {
        content: "−";
    }

    .faq-answer {
        padding: var(--spacing-sm);
        background-color: #444;
        color: var(--color-text-secondary);
        display: none;
    }

    .faq-answer.open {
        display: block;
    }

    /* Contact */
    #contact {
        text-align: center;
    }

    .contact-form {
        margin-top: var(--spacing-lg);
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
        padding: var(--spacing-md);
        background-color: #222;
        border-radius: var(--border-radius);
        box-shadow: var(--box-shadow);
        text-align: left;
    }

    .form-group {
        margin-bottom: var(--spacing-sm);
    }

    .form-group label {
        display: block;
        color: var(--color-text-secondary);
        margin-bottom: 0.25rem;
    }

    .form-group input,
    .form-group textarea,
    .form-group select {
        width: 100%;
        padding: 0.75rem;
        border: 1px solid #333;
        border-radius: calc(var(--border-radius) / 4);
        background-color: #333;
        color: var(--color-text-primary);
        font-family: inherit;
        font-size: 1rem;
    }

    .form-group textarea {
        resize: vertical;
    }

    .submit-button {
        display: inline-block;
        padding: 1rem 2rem;
        border-radius: var(--border-radius);
        background-color: var(--color-green);
        color: var(--color-text-primary);
        text-decoration: none;
        font-weight: 500;
        transition: background-color 0.3s ease;
        cursor: pointer;
        border: none;
        width: 100%;
    }

    .submit-button:hover {
        background-color: #107c33;
    }

    .form-message {
        margin-top: var(--spacing-sm);
        padding: 1rem;
        border-radius: calc(var(--border-radius) / 4);
        text-align: center;
    }

    .form-success {
        background-color: rgba(22, 163, 74, 0.2);
        color: var(--color-green);
    }

    .form-error {
        background-color: rgba(220, 38, 38, 0.2);
        color: #dc2626;
    }

    /* Footer */
    footer {
        background-color: #1a1a1a;
        padding: var(--spacing-md) 0;
        text-align: center;
        color: var(--color-text-secondary);
        font-size: 0.9rem;
    }

    .footer-links {
        margin-bottom: var(--spacing-sm);
    }

    .footer-links a {
        color: var(--color-text-secondary);
        margin: 0 var(--spacing-sm);
    }

    .footer-links a:hover {
        color: var(--color-green);
    }

    .social-links a {
        display: inline-block;
        margin: 0 var(--spacing-sm);
        font-size: 1.2rem;
        color: var(--color-text-secondary);
    }

    .social-links a:hover {
        color: var(--color-green);
    }

    /* Floating WhatsApp Button */
    .whatsapp-float {
        position: fixed;
        bottom: var(--spacing-lg);
        right: var(--spacing-lg);
        background-color: #25d366;
        color: white;
        border-radius: 50%;
        width: 60px;
        height: 60px;
        text-align: center;
        font-size: 2rem;
        line-height: 60px;
        z-index: 99;
        box-shadow: var(--box-shadow);
    }

    .whatsapp-float:hover {
```

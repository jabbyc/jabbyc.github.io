:root {
    /* Color Palette */
    --color-primary-600: #1d4ed8;
    --color-primary-700: #1e40af;
    --color-primary-800: #1e3a8a;
    --color-secondary-500: #6b7280;
    --color-secondary-100: #f3f4f6;
    --color-neutral-100: #ffffff;
    --color-neutral-900: #1f2937;
    --color-accent-600: #ef4444;

    /* Spacing */
    --space-sm: 0.5rem;
    --space-md: 1rem;
    --space-lg: 1.5rem;
    --space-xl: 2rem;
    --space-2xl: 4rem;
    --space-3xl: 6rem;
    --space-4xl: 8rem;

    /* Typography */
    --font-sans: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif;
    --font-heading: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif;
}

/* Base Styles */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
    font-size: 16px;
}

body {
    font-family: var(--font-sans);
    line-height: 1.6;
    color: var(--color-neutral-900);
    background-color: var(--color-neutral-100);
}

/* Accessibility */
:focus-visible {
    outline: 2px solid var(--color-primary-600);
    outline-offset: 2px;
    border-radius: 4px;
}

.skip-link {
    position: absolute;
    top: -40px;
    left: 0;
    background-color: var(--color-primary-600);
    color: var(--color-neutral-100);
    padding: var(--space-md);
    z-index: 1000;
}

.skip-link:focus {
    top: 0;
}

/* Layout */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 var(--space-md);
}

.section {
    padding: var(--space-3xl) 0;
    animation: fade-in 1s ease-in-out;
}

.section:nth-of-type(even) {
    background-color: var(--color-secondary-100);
}

h1, h2, h3 {
    font-family: var(--font-heading);
    line-height: 1.2;
    font-weight: 700;
}

h1 { font-size: 2.5rem; }
h2 { font-size: 2rem; }
h3 { font-size: 1.5rem; }

@media (min-width: 768px) {
    h1 { font-size: 3rem; }
    h2 { font-size: 2.5rem; }
}

.section-title {
    text-align: center;
    margin-bottom: var(--space-md);
}

.section-subtitle {
    text-align: center;
    max-width: 800px;
    margin: 0 auto var(--space-2xl);
    color: var(--color-secondary-500);
}

/* Navbar */
.navbar {
    position: sticky;
    top: 0;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(8px);
    z-index: 50;
    padding: var(--space-md) 0;
    border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

.navbar-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-weight: 700;
    font-size: 1.5rem;
    text-decoration: none;
    color: var(--color-primary-700);
}

.nav-links {
    display: none;
    gap: var(--space-lg);
}

.nav-links a {
    text-decoration: none;
    color: var(--color-neutral-900);
    padding: var(--space-sm) 0;
    transition: color 0.3s ease;
    font-weight: 500;
}

.nav-links a:hover {
    color: var(--color-primary-600);
}

.nav-links a.cta-link {
    background-color: var(--color-primary-600);
    color: var(--color-neutral-100);
    padding: var(--space-sm) var(--space-md);
    border-radius: 9999px;
}

.menu-toggle {
    display: block;
    border: none;
    background: none;
    cursor: pointer;
    padding: var(--space-sm);
    color: var(--color-neutral-900);
}

@media (min-width: 768px) {
    .nav-links {
        display: flex;
    }
    .menu-toggle {
        display: none;
    }
}

/* Mobile Floating CTA Button */
.mobile-cta-btn {
    position: fixed;
    bottom: var(--space-xl);
    right: var(--space-xl);
    z-index: 40;
    background-color: #25D366; /* WhatsApp brand color */
    color: var(--color-neutral-100);
    padding: var(--space-md) var(--space-lg);
    border-radius: 9999px;
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: var(--space-sm);
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    transition: transform 0.3s ease;
}

.mobile-cta-btn:hover {
    transform: translateY(-2px);
}

.mobile-cta-btn svg {
    width: 20px;
    height: 20px;
}

@media (min-width: 768px) {
    .mobile-cta-btn {
        display: none;
    }
}

/* Hero Section */
.hero-section {
    min-height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    background-color: var(--color-secondary-100);
    padding: var(--space-2xl) 0;
}

.hero-title {
    font-size: 2.5rem;
    font-weight: 800;
    margin-bottom: var(--space-md);
    max-width: 800px;
}

.hero-subtitle {
    font-size: 1.125rem;
    color: var(--color-secondary-500);
    margin-bottom: var(--space-xl);
    max-width: 700px;
}

.hero-ctas {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: var(--space-lg);
}

.btn {
    padding: var(--space-md) var(--space-xl);
    text-decoration: none;
    font-weight: 600;
    border-radius: 9999px;
    border: 2px solid transparent;
    transition: all 0.3s ease;
    display: inline-flex;
    align-items: center;
    gap: var(--space-sm);
}

.btn-primary {
    background-color: var(--color-primary-600);
    color: var(--color-neutral-100);
}

.btn-primary:hover {
    background-color: var(--color-primary-700);
}

.btn-secondary {
    background-color: transparent;
    color: var(--color-primary-600);
    border-color: var(--color-primary-600);
}

.btn-secondary:hover {
    background-color: var(--color-primary-600);
    color: var(--color-neutral-100);
}

.trust-badges {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: var(--space-lg);
    margin-top: var(--space-4xl);
}

.trust-badges span {
    display: flex;
    align-items: center;
    gap: var(--space-sm);
    color: var(--color-secondary-500);
    font-weight: 500;
}

.trust-badges svg {
    width: 20px;
    height: 20px;
    color: var(--color-primary-600);
}

/* Quick Stats */
.stats-section {
    background-color: var(--color-neutral-100);
    padding: var(--space-2xl) 0;
}

.stat-card {
    text-align: center;
    padding: var(--space-lg);
}

.stat-number {
    font-size: 3rem;
    font-weight: 800;
    color: var(--color-primary-600);
}

.stat-label {
    font-size: 1rem;
    color: var(--color-neutral-900);
}

/* Services */
.services-grid {
    gap: var(--space-xl);
}

.service-card {
    background-color: var(--color-neutral-100);
    padding: var(--space-xl);
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.service-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
}

.card-header {
    display: flex;
    align-items: center;
    gap: var(--space-md);
    margin-bottom: var(--space-lg);
}

.card-header svg {
    width: 48px;
    height: 48px;
    color: var(--color-primary-600);
}

.card-header h3 {
    margin: 0;
}

.card-list {
    list-style: none;
    padding: 0;
    margin: 0 0 var(--space-xl) 0;
    color: var(--color-secondary-500);
}

.card-list li {
    margin-bottom: var(--space-sm);
}

.card-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.btn-card {
    padding: var(--space-sm) var(--space-md);
    background-color: var(--color-primary-600);
    color: var(--color-neutral-100);
    border-radius: 9999px;
    text-decoration: none;
    font-weight: 600;
    transition: background-color 0.3s ease;
}

.btn-card:hover {
    background-color: var(--color-primary-700);
}

/* Portfolio */
.portfolio-grid {
    gap: var(--space-xl);
}

.portfolio-item {
    background-color: var(--color-neutral-100);
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
    display: flex;
    flex-direction: column;
    overflow: hidden;
}

.portfolio-image-placeholder {
    width: 100%;
    height: 200px;
    background-color: var(--color-secondary-100);
    display: flex;
    justify-content: center;
    align-items: center;
}

.portfolio-image-placeholder svg {
    width: 64px;
    height: 64px;
    color: var(--color-secondary-500);
}

.portfolio-content {
    padding: var(--space-lg);
}

.project-details {
    color: var(--color-secondary-500);
    margin-bottom: var(--space-md);
}

.btn-ghost {
    background-color: transparent;
    color: var(--color-primary-600);
    text-decoration: none;
    font-weight: 600;
    transition: color 0.3s ease;
}

.btn-ghost:hover {
    color: var(--color-primary-800);
}

/* Testimonials */
.testimonials-section {
    background-color: var(--color-secondary-100);
}

.testimonials-grid {
    gap: var(--space-xl);
}

.testimonial-card {
    background-color: var(--color-neutral-100);
    padding: var(--space-xl);
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
}

.star-rating {
    color: gold;
    display: flex;
    gap: var(--space-sm);
    margin-bottom: var(--space-md);
}

.star-rating svg {
    width: 20px;
    height: 20px;
}

.quote {
    font-style: italic;
    margin-bottom: var(--space-md);
}

.quote::before {
    content: "“";
    font-size: 2rem;
    line-height: 0;
    vertical-align: sub;
    margin-right: var(--space-sm);
}
.quote::after {
    content: "”";
    font-size: 2rem;
    line-height: 0;
    vertical-align: sub;
    margin-left: var(--space-sm);
}


/* Pricing */
.pricing-grid {
    gap: var(--space-xl);
}

.pricing-card {
    background-color: var(--color-neutral-100);
    padding: var(--space-xl);
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.pricing-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
}

.featured-pricing {
    border: 2px solid var(--color-primary-600);
}

.price-value {
    font-size: 2.5rem;
    font-weight: 700;
    color: var(--color-primary-600);
    margin: var(--space-sm) 0;
}

.price-desc {
    color: var(--color-secondary-500);
    margin-bottom: var(--space-xl);
}

.pricing-features {
    list-style: none;
    padding: 0;
    text-align: left;
    margin-bottom: var(--space-xl);
}

.pricing-features li {
    display: flex;
    align-items: center;
    gap: var(--space-sm);
    margin-bottom: var(--space-sm);
    color: var(--color-neutral-900);
}

.pricing-features li svg {
    width: 20px;
    height: 20px;
}

.pricing-features li .lucide-check-circle {
    color: #22c55e;
}

.pricing-features li .lucide-x-circle {
    color: #ef4444;
}

.btn-pricing {
    width: 100%;
    display: block;
    text-align: center;
    background-color: var(--color-primary-600);
    color: var(--color-neutral-100);
    padding: var(--space-md) var(--space-xl);
    border-radius: 9999px;
    text-decoration: none;
    font-weight: 600;
    transition: background-color 0.3s ease;
}

.btn-pricing:hover {
    background-color: var(--color-primary-700);
}

/* About */
.about-section {
    background-color: var(--color-secondary-100);
}

.about-content {
    max-width: 800px;
    margin: 0 auto;
}

.about-text p {
    margin-bottom: var(--space-md);
    text-align: center;
}

/* FAQ */
.faq-container {
    max-width: 800px;
    margin: 0 auto;
}

.faq-item {
    border-bottom: 1px solid var(--color-secondary-500);
    padding: var(--space-md) 0;
}

.faq-question {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: none;
    border: none;
    text-align: left;
    cursor: pointer;
    font-size: 1.125rem;
    font-weight: 600;
    color: var(--color-neutral-900);
    padding: var(--space-sm) 0;
}

.faq-question .faq-icon {
    transition: transform 0.3s ease;
}

.faq-question[aria-expanded="true"] .faq-icon {
    transform: rotate(180deg);
}

.faq-answer {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
}

.faq-answer p {
    padding: var(--space-md) 0;
}

/* Contact */
.contact-section {
    background-color: var(--color-neutral-100);
    text-align: center;
}

.contact-methods {
    display: flex;
    flex-direction: column;
    gap: var(--space-md);
    margin-bottom: var(--space-xl);
}

.btn-large {
    padding: var(--space-md) var(--space-2xl);
    font-size: 1.125rem;
}

.contact-hr {
    border: none;
    height: 1px;
    background-color: var(--color-secondary-100);
    margin: var(--space-2xl) auto;
    width: 50%;
}

.section-subtitle-small {
    margin-bottom: var(--space-md);
    color: var(--color-secondary-500);
}

#contact-form {
    max-width: 600px;
    margin: 0 auto;
    text-align: left;
}

.form-group {
    margin-bottom: var(--space-md);
}

.form-group label {
    display: block;
    font-weight: 600;
    margin-bottom: var(--space-sm);
}

.form-group input,
.form-group textarea,
.form-group select {
    width: 100%;
    padding: var(--space-sm);
    border: 1px solid var(--color-secondary-500);
    border-radius: 4px;
    font-family: var(--font-sans);
}

.form-group input:focus,
.form-group textarea:focus,
.form-group select:focus {
    border-color: var(--color-primary-600);
    outline: none;
}

.form-group input:invalid:not(:placeholder-shown),
.form-group textarea:invalid:not(:placeholder-shown) {
    border-color: var(--color-accent-600);
}

.form-group .error-message {
    font-size: 0.875rem;
    color: var(--color-accent-600);
    display: none;
    margin-top: var(--space-sm);
}

.form-status {
    padding: var(--space-md);
    margin-top: var(--space-md);
    border-radius: 4px;
    text-align: center;
    display: none;
}

.form-status.success {
    background-color: #d1fae5;
    color: #065f46;
}

.form-status.error {
    background-color: #fee2e2;
    color: #991b1b;
}

.form-note {
    font-size: 0.875rem;
    color: var(--color-secondary-500);
    text-align: center;
    margin-top: var(--space-md);
}

.btn-submit {
    width: 100%;
    background-color: var(--color-primary-600);
    color: var(--color-neutral-100);
    border: none;
    cursor: pointer;
    font-weight: 600;
    padding: var(--space-md) var(--space-xl);
    border-radius: 4px;
    transition: background-color 0.3s ease;
}

.btn-submit:hover {
    background-color: var(--color-primary-700);
}

/* Footer */
.footer {
    background-color: var(--color-neutral-900);
    color: var(--color-secondary-100);
    padding: var(--space-2xl) 0;
}

.footer-content {
    display: flex;
    flex-direction: column;
    text-align: center;
    gap: var(--space-xl);
}

.footer-col h4 {
    margin-bottom: var(--space-md);
    color: var(--color-neutral-100);
}

.footer-col a {
    display: block;
    color: var(--color-secondary-500);
    text-decoration: none;
    margin-bottom: var(--space-sm);
}

.footer-col a:hover {
    color: var(--color-neutral-100);
}

.made-in {
    font-size: 0.875rem;
    color: var(--color-secondary-500);
}

.social-links {
    display: flex;
    justify-content: center;
    gap: var(--space-md);
}

.social-links a {
    color: var(--color-secondary-500);
    transition: color 0.3s ease;
}

.social-links a:hover {
    color: var(--color-neutral-100);
}

@media (min-width: 768px) {
    .grid-2-col {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: var(--space-xl);
    }
    
    .grid-3-col {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: var(--space-xl);
    }

    .footer-content {
        flex-direction: row;
        justify-content: space-between;
        text-align: left;
    }
}


/* Fade-in Animation */
.fade-in {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.fade-in.is-visible {
    opacity: 1;
    transform: translateY(0);
}

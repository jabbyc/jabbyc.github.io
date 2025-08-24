import React, { useState } from 'react';

// Main App component that holds the entire website structure.
function App() {
  const [activeSection, setActiveSection] = useState('home');

  // Renders the correct section based on the current activeSection state.
  const renderSection = () => {
    switch (activeSection) {
      case 'home':
        return <HomeSection setActiveSection={setActiveSection} />;
      case 'services':
        return <ServicesSection />;
      case 'portfolio':
        return <PortfolioSection />;
      case 'contact':
        return <ContactSection />;
      default:
        return <HomeSection setActiveSection={setActiveSection} />;
    }
  };

  return (
    <div className="bg-gray-50 min-h-screen font-inter flex flex-col">
      <Header setActiveSection={setActiveSection} />
      <main className="flex-grow p-4 md:p-8 flex items-center justify-center">
        {renderSection()}
      </main>
      <Footer />
    </div>
  );
}

// Navigational Header component.
const Header = ({ setActiveSection }) => {
  const [isMenuOpen, setIsMenuOpen] = useState(false);

  const navItems = [
    { name: 'Home', id: 'home' },
    { name: 'Services', id: 'services' },
    { name: 'Portfolio', id: 'portfolio' },
    { name: 'Contact', id: 'contact' },
  ];

  return (
    <header className="bg-white shadow-lg py-4 px-6 md:px-12 rounded-b-xl sticky top-0 z-50">
      <nav className="flex items-center justify-between flex-wrap">
        <div className="flex items-center flex-shrink-0 text-blue-600 mr-6">
          <span className="font-bold text-2xl tracking-tight">John Doe</span>
        </div>
        <div className="block md:hidden">
          <button
            onClick={() => setIsMenuOpen(!isMenuOpen)}
            className="flex items-center px-3 py-2 border rounded text-blue-600 border-blue-400 hover:text-blue-800 hover:border-blue-800 transition-colors duration-300"
            aria-label="Toggle navigation"
          >
            <svg className="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v15z" />
            </svg>
          </button>
        </div>
        <div className={`w-full md:block flex-grow md:flex md:items-center md:w-auto ${isMenuOpen ? 'block' : 'hidden'}`}>
          <div className="text-sm md:flex-grow">
            {navItems.map((item) => (
              <a
                key={item.id}
                href="#"
                onClick={(e) => {
                  e.preventDefault();
                  setActiveSection(item.id);
                  setIsMenuOpen(false); // Close menu on click
                }}
                className="block mt-4 md:inline-block md:mt-0 text-gray-700 hover:text-blue-600 mr-4 transition-colors duration-300 font-medium"
              >
                {item.name}
              </a>
            ))}
          </div>
        </div>
      </nav>
    </header>
  );
};

// Reusable Section Component with animations.
const Section = ({ id, title, children }) => (
  <section id={id} className="p-8 md:p-12 rounded-xl shadow-lg w-full max-w-5xl bg-white animate-fadeIn">
    <h2 className="text-4xl font-bold mb-8 text-center text-blue-600">{title}</h2>
    {children}
  </section>
);

// Home Section with a hero component.
const HomeSection = ({ setActiveSection }) => (
  <Section id="home" title="Freelance Web Developer & Designer">
    <div className="flex flex-col md:flex-row items-center justify-center space-y-8 md:space-y-0 md:space-x-12">
      <div className="flex-1 text-center md:text-left">
        <h1 className="text-5xl md:text-6xl font-extrabold text-gray-900 leading-tight mb-4">
          Bring Your Ideas to Life
        </h1>
        <p className="text-lg text-gray-600 mb-6">
          I craft stunning, high-performing websites and digital experiences tailored to your business needs. Let's build something amazing together.
        </p>
        <div className="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
          <button
            onClick={() => setActiveSection('services')}
            className="bg-blue-600 text-white font-semibold py-3 px-8 rounded-lg shadow-md hover:bg-blue-700 transition-colors duration-300 transform hover:scale-105"
          >
            Explore Services
          </button>
          <button
            onClick={() => setActiveSection('contact')}
            className="bg-white text-blue-600 font-semibold py-3 px-8 rounded-lg shadow-md border border-blue-600 hover:bg-blue-50 transition-colors duration-300 transform hover:scale-105"
          >
            Contact Me
          </button>
        </div>
      </div>
      <div className="flex-1 flex justify-center">
        {/* Placeholder for an image or avatar */}
        <div className="bg-blue-100 w-64 h-64 rounded-full flex items-center justify-center text-blue-400 text-6xl font-bold">JD</div>
      </div>
    </div>
  </Section>
);

// Services Section component.
const ServicesSection = () => (
  <Section id="services" title="My Services">
    <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <ServiceCard
        title="Custom Web Development"
        description="Building scalable, secure, and performant websites from scratch using modern frameworks like React."
      />
      <ServiceCard
        title="UI/UX Design"
        description="Designing intuitive and visually appealing user interfaces that provide a seamless user experience."
      />
      <ServiceCard
        title="E-commerce Solutions"
        description="Creating robust online stores with secure payment gateways and easy-to-manage product catalogs."
      />
      <ServiceCard
        title="SEO & Performance Optimization"
        description="Ensuring your website ranks high on search engines and loads quickly on all devices."
      />
      <ServiceCard
        title="Content Management"
        description="Implementing easy-to-use content management systems (CMS) so you can update your site effortlessly."
      />
      <ServiceCard
        title="Website Maintenance"
        description="Providing ongoing support, updates, and security patches to keep your site running smoothly."
      />
    </div>
  </Section>
);

// Reusable Service Card component.
const ServiceCard = ({ title, description }) => (
  <div className="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300">
    <h3 className="text-xl font-semibold text-blue-700 mb-2">{title}</h3>
    <p className="text-gray-600">{description}</p>
  </div>
);

// Portfolio Section component with mock data.
const PortfolioSection = () => {
  const projects = [
    { title: 'Project Alpha', description: 'A custom e-commerce site for a small business.', image: 'https://placehold.co/400x300/e0e7ff/1d4ed8?text=Project+Alpha' },
    { title: 'Project Beta', description: 'A responsive blog platform built with a modern CMS.', image: 'https://placehold.co/400x300/e0e7ff/1d4ed8?text=Project+Beta' },
    { title: 'Project Gamma', description: 'A portfolio site for a freelance photographer.', image: 'https://placehold.co/400x300/e0e7ff/1d4ed8?text=Project+Gamma' },
    { title: 'Project Delta', description: 'A landing page for a new SaaS product.', image: 'https://placehold.co/400x300/e0e7ff/1d4ed8?text=Project+Delta' },
  ];

  return (
    <Section id="portfolio" title="My Recent Work">
      <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
        {projects.map((project, index) => (
          <div key={index} className="bg-gray-50 rounded-lg shadow-md overflow-hidden">
            <img src={project.image} alt={project.title} className="w-full h-auto object-cover" />
            <div className="p-6">
              <h3 className="text-2xl font-semibold text-blue-700 mb-2">{project.title}</h3>
              <p className="text-gray-600">{project.description}</p>
            </div>
          </div>
        ))}
      </div>
    </Section>
  );
};

// Contact Section with a simple form.
const ContactSection = () => (
  <Section id="contact" title="Get in Touch">
    <p className="mb-6 text-center text-gray-600">I'm excited to hear about your project! Please fill out the form below and I'll get back to you as soon as possible.</p>
    <form className="space-y-4 max-w-lg mx-auto">
      <input type="text" placeholder="Your Name" className="w-full p-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-200" />
      <input type="email" placeholder="Your Email" className="w-full p-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-200" />
      <textarea rows="4" placeholder="Your Message" className="w-full p-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-200"></textarea>
      <button type="submit" className="w-full bg-blue-600 text-white font-semibold py-3 px-6 rounded-lg shadow-md hover:bg-blue-700 transition-colors duration-300">Send Message</button>
    </form>
  </Section>
);

// Footer component.
const Footer = () => (
  <footer className="bg-white shadow-lg py-4 px-6 md:px-12 mt-8 rounded-t-xl text-center text-gray-500 text-sm">
    &copy; {new Date().getFullYear()} John Doe. All rights reserved.
  </footer>
);

export default App;

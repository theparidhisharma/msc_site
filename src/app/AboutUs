import React from 'react';
import { Menu, Zap } from 'lucide-react';
 

// --- MOCK DATA ---
const navItems = ['ABOUT US', 'EVENTS', 'BLOGS', 'TEAM', 'CONTACT US', 'FAQ'];

const galleryItems = [
  {
    title: 'Engaging Sessions',
    imagePlaceholder: '/images/gallery-auditorium.jpg', 
  },
  {
    title: 'Core Team',
    imagePlaceholder: '/images/gallery-team.jpg', 
  },
  {
    title: 'Hack-It-Up 2025',
    imagePlaceholder: '/images/gallery-hackitup.jpg', 
  },
];
// --- END MOCK DATA ---

// Helper component for the Navigation Bar
const Navbar = () => { // Changed to standard function/const declaration without explicit React.FC type
  const logoPlaceholderPath = '/images/mlsa-shield-logo.png';

  return (
    // The main nav wrapper covers the full width and is fixed at the top
    <nav className="fixed top-0 left-0 right-0 z-50 p-4">
      {/* Container to center content and control spacing */}
      <div className="max-w-7xl mx-auto flex justify-start items-center h-16 relative">
        
        {/* 1. Logo and Shield (Left Aligned - EXACT MATCH) */}
        <div className="flex items-center backdrop-blur-sm bg-black/40 rounded-lg p-1.5 border border-blue-700/30">
          
          {/* Logo container matching the screenshot's shape and style */}
          <div className="w-12 h-12 flex items-center justify-center rounded-lg shadow-lg">
            <img 
              src={logoPlaceholderPath} 
              alt="Microsoft Learn Student Ambassador Logo" 
              className="w-full h-full object-contain rounded-lg" 
              onError={(e) => {
                  // Fallback for placeholder image loading
                  (e.target as HTMLImageElement).onerror = null;
                  (e.target as HTMLImageElement).src = 'https://placehold.co/48x48/0a0a20/ffffff?text=MLSA';
              }}
            />
          </div>
        </div>

        {/* 2. Desktop Navigation Pill (Centered - EXACT MATCH) */}
        {/* Uses absolute positioning and translate to ensure it's precisely centered */}
        <div className="absolute left-1/2 -translate-x-1/2 hidden lg:flex items-center justify-center 
                        py-3 px-6 rounded-full border border-gray-700/50 
                        bg-black/50 backdrop-blur-sm shadow-2xl">
          <ul className="flex items-center text-sm font-bold text-white/95 uppercase tracking-wide">
            {navItems.map((item, index) => (
              <React.Fragment key={item}>
                <li
                  className="cursor-pointer hover:text-blue-400 transition duration-300 px-3 py-1 whitespace-nowrap"
                >
                  {item}
                </li>
                {/* Custom dot separator for aesthetic matching */}
                {index < navItems.length - 1 && (
                    <span className="text-white/50 text-base font-extrabold px-1 select-none">
                        •
                    </span>
                )}
              </React.Fragment>
            ))}
          </ul>
        </div>

        {/* 3. Mobile Menu Icon (Hidden on desktop - Right Aligned) */}
        <div className="lg:hidden absolute right-4 text-white p-2 backdrop-blur-sm bg-black/40 rounded-lg border border-blue-700/30">
          <Menu className="w-6 h-6 cursor-pointer" />
        </div>
      </div>
    </nav>
  );
};

// Main Component (Next.js Page/Component)
export default function AboutUsPage() { // Changed to standard function declaration
  
  // -- PLACEHOLDER FOR BACKGROUND IMAGE --
  const backgroundPlaceholderPath = '/images/background.jpg';
  
  return (
    <div
      className="min-h-screen text-white font-inter bg-gray-950"
      style={{ 
        // Use the placeholder path for the background image
        backgroundImage: `url(${backgroundPlaceholderPath})`,
        backgroundSize: 'cover',
        backgroundPosition: 'center',
        backgroundRepeat: 'no-repeat',
        // Adds the dark filter/overlay seen in the screenshot
        backgroundColor: '#0d1222', 
        backgroundBlendMode: 'multiply',
      }}
    >
      <Navbar />

      <main className="pt-24 pb-16 px-4 md:px-8 max-w-7xl mx-auto">
        {/* Title Section - EXACTLY AS SHOWN */}
        <div className="text-center mb-16 pt-16">
          <h1 className="text-7xl md:text-[6.5rem] font-black mb-4 tracking-tighter leading-none text-white/95 drop-shadow-lg">
            ABOUT US
          </h1>
          <p className="text-lg md:text-2xl text-gray-300 max-w-4xl mx-auto font-medium">
            We are here, to be the perfect guidance you need to ace the engineering journey you are on!
          </p>
        </div>

        {/* Static Gallery Section - Horizontal Layout Match and rounded container */}
        <section className="relative w-full py-8 md:py-16">
          {/* Main wrapper matching the rounded, dark outline of the gallery section */}
          <div className="flex flex-col lg:flex-row justify-center items-center lg:space-x-6 space-y-6 lg:space-y-0 p-4 md:p-8 
                        bg-black/20 border border-gray-700/50 rounded-[2.5rem] shadow-2xl 
                        shadow-blue-900/50">
            {galleryItems.map((item, index) => (
              <div
                key={index}
                // Aspect ratio is key to matching the image container shape
                className="w-full lg:w-1/3 aspect-video flex-shrink-0 cursor-pointer overflow-hidden 
                         transition duration-300 hover:scale-[1.01] rounded-[2rem] 
                         shadow-xl border-2 border-transparent hover:border-blue-400"
              >
                <img
                  src={item.imagePlaceholder}
                  alt={item.title}
                  // Use object-cover and a defined aspect ratio to maintain shape consistency 
                  className="w-full h-full object-cover rounded-[2rem]" 
                  onError={(e) => {
                      (e.target as HTMLImageElement).onerror = null;
                      // Fallback image source if the placeholder doesn't load
                      (e.target as HTMLImageElement).src = 'https://placehold.co/400x250/0f172a/ffffff?text=Image+Placeholder';
                  }}
                />
              </div>
            ))}
          </div>
        </section>

        {/* Content Text Section - EXACTLY AS SHOWN */}
        <div className="pt-8"> 
          <div className="max-w-6xl mx-auto">
            <p className="text-xl md:text-2xl leading-relaxed text-gray-200">
              We are the <span className="text-blue-400 font-extrabold">MICROSOFT LEARN STUDENT AMBASSADOR STUDENT CHAPTER</span>, your one stop spot for all the amazing sessions and events. This is where you can grow by learning from the mistakes, experiences, success and failure of the experts, your seniors, and peers.
            </p>
          </div>
        </div>
      </main>

      {/* Footer Placeholder (Keeping this for completeness) */}
      <footer className="py-6 mt-16 text-center text-gray-500 text-sm">
        {/* You can add footer content here if needed */}
      </footer>
    </div>
  );
}

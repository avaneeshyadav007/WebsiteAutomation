import React, { useState, useEffect } from 'react';
import { Link, useLocation } from 'react-router-dom';
import { Compass, PenTool, Layout, Mail } from 'lucide-react';

export default function Header() {
  const [scrolled, setScrolled] = useState(false);
  const location = useLocation();

  useEffect(() => {
    const handleScroll = () => {
      setScrolled(window.scrollY > 20);
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  }, []);

  return (
    <header className={`site-header ${scrolled ? 'scrolled' : ''}`}>
      <div className="container nav-container">
        <Link to="/" className="logo text-gradient">
          OmniAgent
        </Link>
        <nav className="nav-links">
          <Link to="/" className={`nav-link ${location.pathname === '/' ? 'active' : ''}`}>Product</Link>
          <a href="/#use-cases" className="nav-link">Use Cases</a>
          <a href="/#core-capabilities" className="nav-link">Capabilities</a>
          <button className="btn-primary" style={{ marginLeft: '1rem' }} onClick={() => {
            if (location.pathname !== '/') {
              window.location.href = '/#demo-access'
            } else {
              document.getElementById('demo-access')?.scrollIntoView({ behavior: 'smooth' })
            }
          }}>Get Access</button>
        </nav>
      </div>
    </header>
  );
}

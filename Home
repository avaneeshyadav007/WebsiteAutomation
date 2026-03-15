import React, { useState } from 'react';
import { Link } from 'react-router-dom';
import { ArrowRight, Sparkles, Cpu, Eye, Activity, TerminalSquare } from 'lucide-react';
import { posts, featuredPost } from '../data';

export default function Home() {
  const [isSubmitted, setIsSubmitted] = useState(false);
  const recentPosts = posts.filter(post => post.id !== featuredPost.id);

  return (
    <div className="animate-fade-in">
      {/* Hero Section */}
      <section className="container hero-section">
        <div style={{ display: 'inline-block', marginBottom: '1.5rem', background: 'rgba(139, 92, 246, 0.15)', padding: '0.4rem 1rem', borderRadius: '100px', border: '1px solid rgba(139, 92, 246, 0.3)', color: 'var(--accent-primary)', fontSize: '0.85rem', fontWeight: 'bold', letterSpacing: '0.05em' }}>
          <Sparkles size={14} style={{ display: 'inline', marginRight: '5px', verticalAlign: 'text-bottom' }} />
          VISION ENGINE 2.0 IS LIVE
        </div>
        <h1 className="hero-title animate-fade-in animate-delay-1">
          Your Hands on the Screen.<br />
          <span className="text-gradient">Powered by Vision AI.</span>
        </h1>
        <p className="hero-subtitle animate-fade-in animate-delay-2" style={{ maxWidth: '750px' }}>
          Meet the autonomous agent that observes your browser and device display, interprets visual elements instantly without relying on APIs or the DOM, and performs complex actions based solely on your intent.
        </p>
        <div className="hero-actions animate-fade-in animate-delay-3">
          <button className="btn-primary" onClick={() => document.getElementById('demo-access')?.scrollIntoView({ behavior: 'smooth' })}>
            Start Automating
            <ArrowRight size={18} />
          </button>
          <button className="btn-secondary" onClick={() => document.getElementById('core-capabilities')?.scrollIntoView({ behavior: 'smooth' })}>
            <TerminalSquare size={18} />
            Explore Capabilities
          </button>
        </div>
      </section>

      {/* Feature Highlight Grid */}
      <div className="container" style={{ padding: '0 2rem', marginTop: '3rem', marginBottom: '6rem' }}>
        <div style={{ display: 'grid', gridTemplateColumns: 'repeat(auto-fit, minmax(300px, 1fr))', gap: '2rem' }}>
          <div className="glass-panel" style={{ padding: '2rem' }}>
            <Eye size={32} className="text-gradient" style={{ marginBottom: '1rem' }} />
            <h3 style={{ fontSize: '1.25rem', marginBottom: '0.75rem' }}>Visual Interpretation</h3>
            <p style={{ color: 'var(--text-secondary)' }}>Reads the screen exactly like a human does. Zero DOM parsing, and no API keys required. It understands context purely from pixels.</p>
          </div>
          <div className="glass-panel" style={{ padding: '2rem' }}>
            <Activity size={32} className="text-gradient" style={{ marginBottom: '1rem' }} />
            <h3 style={{ fontSize: '1.25rem', marginBottom: '0.75rem' }}>Intent-Driven Action</h3>
            <p style={{ color: 'var(--text-secondary)' }}>Tell the agent what your goal is ("Book a flight to NYC") and watch as it clicks, types, and navigates autonomously to achieve it.</p>
          </div>
          <div className="glass-panel" style={{ padding: '2rem' }}>
            <Cpu size={32} className="text-gradient" style={{ marginBottom: '1rem' }} />
            <h3 style={{ fontSize: '1.25rem', marginBottom: '0.75rem' }}>Cross-App Workflows</h3>
            <p style={{ color: 'var(--text-secondary)' }}>Unbound by browser tabs. The agent seamlessly transitions between desktop applications, terminal windows, and the web.</p>
          </div>
        </div>
      </div>

      <div id="core-capabilities" className="container" style={{ padding: '0 2rem' }}>
        <div className="section-header">
          <h2 className="section-title">
            <Sparkles className="text-gradient" size={28} />
            Core Capabilities
          </h2>
        </div>
      </div>

      {/* Featured Capability */}
      <section className="container">
        <Link to={`/post/${featuredPost.slug}`}>
          <div className="featured-article glass-panel">
            <div className="featured-image-wrapper">
              <img src={featuredPost.image} alt={featuredPost.title} className="featured-image" />
            </div>
            <div className="featured-content">
              <div style={{ marginBottom: '1.5rem', display: 'flex', gap: '1rem', alignItems: 'center' }}>
                <span className="tag">{featuredPost.category}</span>
                <span className="article-date">{featuredPost.readingTime}</span>
              </div>
              <h2 className="featured-title">{featuredPost.title}</h2>
              <p className="featured-excerpt">{featuredPost.excerpt}</p>
              
              <div className="author-info" style={{ marginTop: '2.5rem' }}>
                <div className="read-more" style={{ opacity: 1, transform: 'none', background: 'var(--accent-gradient)', padding: '0.75rem 1.5rem', borderRadius: '100px', color: 'white' }}>
                  Explore Capability
                  <ArrowRight size={18} />
                </div>
              </div>
            </div>
          </div>
        </Link>
      </section>

      {/* Other Use Cases Grid */}
      <section id="use-cases" className="container" style={{ marginTop: '6rem' }}>
        <div className="section-header">
          <h2 className="section-title">Explore Use Cases</h2>
        </div>
        
        <div className="articles-grid">
          {recentPosts.map((post) => (
            <Link to={`/post/${post.slug}`} key={post.id} className="article-card">
              <div className="article-image-wrapper">
                <img src={post.image} alt={post.title} className="article-image" loading="lazy" />
              </div>
              <div className="article-content">
                <div className="article-meta">
                  <span className="tag" style={{ border: 'none', background: 'transparent', padding: 0 }}>{post.category}</span>
                  <span className="article-date">{post.readingTime}</span>
                </div>
                <h3 className="article-title">{post.title}</h3>
                <p className="article-excerpt">{post.excerpt}</p>
                <div className="article-footer">
                  <div className="read-more">
                    View Details
                    <ArrowRight size={14} />
                  </div>
                </div>
              </div>
            </Link>
          ))}
        </div>
      </section>

      {/* Demo Access */}
      <section id="demo-access" className="newsletter-section">
        <div className="container glass-panel" style={{ padding: '5rem 2rem', maxWidth: '800px', borderRadius: 'var(--radius-lg)' }}>
          <h2 style={{ fontSize: '2.5rem', marginBottom: '1rem' }}>Ready to deploy the agent?</h2>
          <p style={{ color: 'var(--text-secondary)', fontSize: '1.1rem', marginBottom: '2rem' }}>
            Request API access or download the desktop client to start automating your workflows instantly.
          </p>
          {isSubmitted ? (
            <div style={{ padding: '2rem', background: 'rgba(139, 92, 246, 0.1)', borderRadius: 'var(--radius-md)', border: '1px solid rgba(139, 92, 246, 0.3)', color: 'var(--accent-primary)', fontSize: '1.2rem', fontWeight: '500' }}>
              <Sparkles size={24} style={{ display: 'inline', marginRight: '10px', verticalAlign: 'text-bottom' }} />
              Request received. Our team will be in touch shortly.
            </div>
          ) : (
            <form className="newsletter-form" onSubmit={(e) => { e.preventDefault(); setIsSubmitted(true); }} style={{ display: 'flex', gap: '1rem', justifyContent: 'center' }}>
              <input type="email" placeholder="Enter your work email..." className="newsletter-input" style={{ maxWidth: '300px' }} required />
              <button type="submit" className="btn-primary">Request Access</button>
            </form>
          )}
        </div>
      </section>
    </div>
  );
}

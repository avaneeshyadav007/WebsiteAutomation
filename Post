import React, { useEffect } from 'react';
import { useParams, Link } from 'react-router-dom';
import { ArrowLeft, Play, Terminal } from 'lucide-react';
import { posts } from '../data';

export default function Post() {
  const { slug } = useParams();
  const post = posts.find(p => p.slug === slug);

  useEffect(() => {
    window.scrollTo(0, 0);
  }, [slug]);

  if (!post) {
    return (
      <div className="container" style={{ textAlign: 'center', padding: '8rem 0' }}>
        <h2>Feature not found</h2>
        <Link to="/" className="btn-primary" style={{ marginTop: '2rem' }}>Go Back Home</Link>
      </div>
    );
  }

  return (
    <div className="animate-fade-in" style={{ paddingBottom: '4rem' }}>
      <div className="container">
        <Link to="/" className="btn-secondary" style={{ display: 'inline-flex', marginTop: '2rem', border: 'none' }}>
          <ArrowLeft size={18} /> Back to Product
        </Link>
        
        <header className="post-header">
          <div className="post-meta-top">
            <span className="tag">{post.category}</span>
            <span style={{ color: 'var(--text-muted)' }}>•</span>
            <span style={{ color: 'var(--text-secondary)' }}>{post.readingTime}</span>
          </div>
          <h1 className="post-title">{post.title}</h1>
          
          <div style={{ display: 'flex', gap: '1rem', justifyContent: 'center', marginTop: '2rem' }}>
            <button className="btn-primary" style={{ padding: '0.75rem 1.5rem', borderRadius: '100px' }} onClick={() => window.location.href = '/#demo-access'}>
              <Play size={18} style={{ marginRight: '8px' }} />
              Watch Demo
            </button>
            <button className="btn-secondary" style={{ padding: '0.75rem 1.5rem', borderRadius: '100px' }} onClick={() => window.location.href = '/#demo-access'}>
              <Terminal size={18} style={{ marginRight: '8px' }} />
              View API Docs
            </button>
          </div>
        </header>

        <img src={post.image} alt={post.title} className="post-hero-image glass-panel" />

        <div className="post-content">
          {post.content.split('\n\n').map((paragraph, idx) => {
            if (idx === 1) {
              return (
                <div key={idx}>
                  <blockquote>
                    "The OmniAgent effectively turns any visual interface into an API. If a human can see it and click it, the agent can automate it."
                  </blockquote>
                  <p>{paragraph}</p>
                </div>
              );
            }
            return <p key={idx}>{paragraph}</p>;
          })}
        </div>

        <div className="post-author-box glass-panel">
          <img src={post.author.avatar} alt={post.author.name} />
          <div>
            <h4 style={{ fontSize: '1.25rem', marginBottom: '0.5rem' }}>Powered by {post.author.name}</h4>
            <p style={{ color: 'var(--text-secondary)' }}>
              Our proprietary vision-action model trained on millions of human-computer interaction sequences to understand context and syntax perfectly.
            </p>
          </div>
        </div>
      </div>
    </div>
  );
}

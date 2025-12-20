---
layout: default
title: Blog
permalink: /blog/
custom_css:
  - /assets/css/blog.css
---

<section class="blog-page">
  <!-- Hero Section -->
  <div class="blog-hero">
    <div class="hero-card">
      <h1 class="hero-heading">
        <span class="highlight"> Blog</span>
      </h1>
      <p class="hero-subtitle">
Welcome to my blog! Here, I share updates about my projects, experiences in web development, content creation, and other creative endeavors. Follow along as I document my journey and showcase what I’m working on.      </p>
    </div>
  </div>

  <!-- Blog Posts Grid -->
  <div class="blog-container">
    <div class="blog-grid">
      {% if site.posts.size > 0 %}
        {% for post in site.posts limit: 6 %}
          <article class="blog-card">
            <div class="blog-image-wrapper">
              {% if post.image %}
                <img
                  src="{{ post.image | relative_url }}"
                  alt="{{ post.title }}"
                  class="blog-image"
                />
              {% else %}
                <img
                  src="{{ '/assets/images/blog-placeholder.jpg' | relative_url }}"
                  alt="{{ post.title }}"
                  class="blog-image"
                  onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22250%22%3E%3Crect fill=%22%23f3f4f6%22 width=%22400%22 height=%22250%22/%3E%3Ctext fill=%22%239ca3af%22 font-family=%22sans-serif%22 font-size=%2218%22 dy=%2210.5%22 font-weight=%22bold%22 x=%2250%25%22 y=%2250%25%22 text-anchor=%22middle%22%3EBlog Post%3C/text%3E%3C/svg%3E'"
                />
              {% endif %}
            </div>
            <div class="blog-content">
              <h3 class="blog-title">
                <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
              </h3>
              <p class="blog-description">
                {% if post.excerpt %}
                  {{ post.excerpt | strip_html | truncatewords: 25 }}
                {% else %}
                  {{ post.content | strip_html | truncatewords: 25 }}
                {% endif %}
              </p>
              <div class="blog-meta">
                <time datetime="{{ post.date | date: '%Y-%m-%d' }}" class="blog-date">
                  {{ post.date | date: "%B %d, %Y" }}
                </time>
              </div>
            </div>
          </article>
        {% endfor %}
      {% else %}
        <!-- Placeholder posts if no blog posts exist -->

        <article class="blog-card">
          <div class="blog-image-wrapper">
            <img
              src="{{ '/assets/images/porshe911gt3.jpeg' | relative_url }}"
              alt="Blog post"
              class="blog-image"
              onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22250%22%3E%3Crect fill=%22%23f3f4f6%22 width=%22400%22 height=%22250%22/%3E%3Ctext fill=%22%239ca3af%22 font-family=%22sans-serif%22 font-size=%2218%22 dy=%2210.5%22 font-weight=%22bold%22 x=%2250%25%22 y=%2250%25%22 text-anchor=%22middle%22%3EBlog Post%3C/text%3E%3C/svg%3E'"
            />
          </div>
          <div class="blog-content">
            <h3 class="blog-title">
              <a href="#">Building Modern Web Applications</a>
            </h3>
            <p class="blog-description">
The members of Group 76 at SITE1101 gave me a Porsche 911 GT3 as a present. I was so happy that I can’t even put it into words. Thank you so much!            </p>
            <div class="blog-meta">
              <time datetime="2025-01-10" class="blog-date">December 19, 2025</time>
            </div>
          </div>
        </article>

        
        <article class="blog-card">
          <div class="blog-image-wrapper">
            <img
              src="{{ '/assets/images/blog2.png' | relative_url }}"
              alt="Blog post"
              class="blog-image"
              onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22250%22%3E%3Crect fill=%22%23f3f4f6%22 width=%22400%22 height=%22250%22/%3E%3Ctext fill=%22%239ca3af%22 font-family=%22sans-serif%22 font-size=%2218%22 dy=%2210.5%22 font-weight=%22bold%22 x=%2250%25%22 y=%2250%25%22 text-anchor=%22middle%22%3EBlog Post%3C/text%3E%3C/svg%3E'"
            />
          </div>
          <div class="blog-content">
            <h3 class="blog-title">
              <a href="#">Building Modern Web Applications</a>
            </h3>
            <p class="blog-description">
          Currently, I am actively working on BrainFit.az’s website, helping to design and develop its layout, improve user experience, and implement new features. This project allows me to apply my programming and design skills while contributing to a real-world digital platform.
            </p>
            <div class="blog-meta">
              <time datetime="2025-01-10" class="blog-date">December 10, 2025</time>
            </div>
          </div>
        </article>

        <article class="blog-card">
          <div class="blog-image-wrapper">
            <img
              src="{{ '/assets/images/blog1.PNG' | relative_url }}"
              alt="Blog post"
              class="blog-image"
              onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22250%22%3E%3Crect fill=%22%23f3f4f6%22 width=%22400%22 height=%22250%22/%3E%3Ctext fill=%22%239ca3af%22 font-family=%22sans-serif%22 font-size=%2218%22 dy=%2210.5%22 font-weight=%22bold%22 x=%2250%25%22 y=%2250%25%22 text-anchor=%22middle%22%3EBlog Post%3C/text%3E%3C/svg%3E'"
            />
          </div>
          <div class="blog-content">
            <h3 class="blog-title">
              <a href="#">Content Creation Tips for Developers</a>
            </h3>
            <p class="blog-description">
Hi! I also manage the Instagram account BrainFit.az. I create, shoot, and edit videos for their content, making sure each post is engaging and visually appealing. Alongside filming, I handle the editing process, adding effects, transitions, and polishing the final videos to ensure they stand out.
            </p>
            <div class="blog-meta">
              <time datetime="2025-01-05" class="blog-date">January 5, 2025</time>
            </div>
          </div>
        </article>
      {% endif %}
    </div>
  </div>

  <!-- Bottom Button -->
  <div class="blog-footer">
    <a href="https://github.com/nilaliva" class="btn-view-more" target="_blank" rel="noopener noreferrer">
      View More Posts
    </a>
  </div>
</section>


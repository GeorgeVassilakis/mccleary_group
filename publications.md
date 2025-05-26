---
layout: page
title: Publications
permalink: /publications/
---

<section class="section">
    <div class="container">
        <div class="section-header">
            <h1>Publications</h1>
            <div class="section-line"></div>
        </div>
        
        <div class="publications-note">
            <p>
                For a complete list of publications, please visit 
                <a href="{{ site.pi.scholar }}" target="_blank">Professor McCleary's Google Scholar profile</a>.
            </p>
        </div>
        
        <div class="publications-list">
            {% for pub in site.data.publications %}
            <div class="publication-item">
                <div class="publication-year">{{ pub.year }}</div>
                <h3 class="publication-title">
                    {% if pub.link %}
                    <a href="{{ pub.link }}" target="_blank">{{ pub.title }}</a>
                    {% else %}
                    {{ pub.title }}
                    {% endif %}
                </h3>
                <p class="publication-authors">{{ pub.authors }}</p>
                <p class="publication-journal">{{ pub.journal }}</p>
                {% if pub.tags %}
                <div class="publication-tags">
                    {% for tag in pub.tags %}
                    <span class="tag">{{ tag }}</span>
                    {% endfor %}
                </div>
                {% endif %}
            </div>
            {% endfor %}
        </div>
        
        <div class="publications-footer">
            <h3>Adding Publications</h3>
            <p>
                To add new publications, edit the <code>_data/publications.yml</code> file. Publications should be added in reverse chronological order (newest first).
            </p>
        </div>
    </div>
</section>

<style>
.publications-note {
    text-align: center;
    padding: 2rem;
    background: #1a1f2e;
    border-radius: 12px;
    border: 1px solid #2d3748;
    margin-bottom: 3rem;
}

.publications-note p {
    font-size: 1.125rem;
    margin: 0;
}

.publications-footer {
    max-width: 700px;
    margin: 4rem auto 0;
    padding: 2rem;
    background: rgba(99, 102, 241, 0.1);
    border-radius: 12px;
    border: 1px solid rgba(99, 102, 241, 0.3);
}

.publications-footer h3 {
    color: #6366f1;
    margin-bottom: 1rem;
}

.publications-footer code {
    background: rgba(255, 255, 255, 0.1);
    padding: 0.25rem 0.5rem;
    border-radius: 4px;
    font-family: monospace;
}
</style>
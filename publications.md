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
        
        {% comment %} Group publications by year and sort in descending order {% endcomment %}
        {% assign sorted_publications = site.data.publications | sort: 'year' | reverse %}
        {% assign grouped_publications = sorted_publications | group_by: 'year' %}
        
        <div class="publications-list">
            {% for year_group in grouped_publications %}
                {% if year_group.name %}
                    {% assign year_num = year_group.name | plus: 0 %}
                    
                    {% comment %} Create section header based on year {% endcomment %}
                    {% if year_num <= 2021 %}
                        {% unless year_2021_shown %}
                            <h2 class="year-header">2021 and Earlier</h2>
                            {% assign year_2021_shown = true %}
                        {% endunless %}
                    {% else %}
                        <h2 class="year-header">{{ year_group.name }}</h2>
                    {% endif %}
                    
                    {% comment %} Display publications for this year {% endcomment %}
                    {% for pub in year_group.items %}
                    <div class="publication-item">
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
                {% endif %}
            {% endfor %}
        </div>
        
        <div class="publications-footer">
            <h3>Adding Publications</h3>
            <p>
                To add new publications, edit the <code>_data/publications.yml</code> file. Publications will be automatically grouped by year.
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

.year-header {
    color: #6366f1;
    font-size: 2rem;
    margin-top: 3rem;
    margin-bottom: 1.5rem;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid #2d3748;
}

.year-header:first-of-type {
    margin-top: 0;
}

.publication-item {
    background: #1a1f2e;
    border-radius: 12px;
    padding: 2rem;
    margin-bottom: 1.5rem;
    border: 1px solid #2d3748;
    transition: all 0.3s ease;
}

.publication-item:hover {
    transform: translateY(-2px);
    border-color: rgba(99, 102, 241, 0.3);
    box-shadow: 0 4px 12px rgba(99, 102, 241, 0.1);
}

.publication-title {
    font-size: 1.25rem;
    margin-bottom: 0.5rem;
}

.publication-authors {
    color: #94a3b8;
    margin-bottom: 0.5rem;
}

.publication-journal {
    font-style: italic;
    color: #94a3b8;
}

.publication-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 1rem;
}

.tag {
    background: rgba(99, 102, 241, 0.2);
    color: #818cf8;
    padding: 0.25rem 0.75rem;
    border-radius: 20px;
    font-size: 0.875rem;
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
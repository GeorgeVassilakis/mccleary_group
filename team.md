---
layout: page
title: Team
permalink: /team/
---

<section class="section">
    <div class="container">
        <div class="section-header">
            <h1>Our Team</h1>
            <div class="section-line"></div>
        </div>
        
        <div class="team-grid">
            {% for member in site.data.team %}
            <div class="team-card">
                <img src="{{ member.image }}" alt="{{ member.name }}" class="team-image">
                <h3 class="team-name">{{ member.name }}</h3>
                <p class="team-role">{{ member.role }}</p>
                <p class="team-research">{{ member.research }}</p>
            </div>
            {% endfor %}
        </div>
        
        <div class="join-section">
            <h2>Join Our Group</h2>
            <p>
                We are always looking for motivated graduate students and postdocs interested in observational cosmology, gravitational lensing, and galaxy cluster physics. If you're interested in joining our group, please contact Professor McCleary at <a href="mailto:{{ site.pi.email }}">{{ site.pi.email }}</a>.
            </p>
        </div>
    </div>
</section>

<style>
.join-section {
    max-width: 800px;
    margin: 5rem auto 0;
    text-align: center;
    padding: 3rem;
    background: #1a1f2e;
    border-radius: 12px;
    border: 1px solid #2d3748;
}

.join-section h2 {
    color: #6366f1;
    margin-bottom: 1.5rem;
}

.join-section p {
    font-size: 1.125rem;
    line-height: 1.8;
}
</style>
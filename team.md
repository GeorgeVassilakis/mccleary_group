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
        
        <!-- Current Members -->
        <h2 class="team-section-title">Current Members</h2>
        <div class="team-grid">
            {% assign current_members = site.data.team | where: "status", "current" %}
            {% for member in current_members %}
            <div class="team-card">
                <div class="team-image-wrapper">
                    <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" class="team-image">
                </div>
                <h3 class="team-name">{{ member.name }}</h3>
                <p class="team-role">{{ member.role }}</p>
                {% if member.affiliation %}
                <p class="team-affiliation">{{ member.affiliation }}</p>
                {% endif %}
                <p class="team-research">{{ member.research }}</p>
            </div>
            {% endfor %}
        </div>
        
        <!-- Past Members -->
        <h2 class="team-section-title">Past Members</h2>
        <div class="team-grid past-members">
            {% assign past_members = site.data.team | where: "status", "past" %}
            {% for member in past_members %}
            <div class="team-card past-member-card">
                <div class="team-image-wrapper">
                    <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" class="team-image">
                </div>
                <h3 class="team-name">{{ member.name }}</h3>
                <p class="team-role">Former {{ member.role }}</p>
                <p class="team-current">Currently: {{ member.current_position }}</p>
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
.team-section-title {
    font-size: 1.75rem;
    color: #6366f1;
    margin-top: 3rem;
    margin-bottom: 2rem;
    text-align: center;
}

.team-section-title:first-of-type {
    margin-top: 0;
}

/* Past member cards styling */
.past-member-card {
    background: #1a1f2e;
    border: 1px solid rgba(45, 55, 72, 0.5);
    opacity: 0.95;
}

.past-member-card .team-role {
    color: #94a3b8;
    font-style: italic;
}

.team-current {
    color: #6366f1;
    font-weight: 500;
    font-size: 0.95rem;
    margin-top: 0.25rem;
}

/* Remove research text from past members */
.past-member-card .team-research {
    display: none;
}

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
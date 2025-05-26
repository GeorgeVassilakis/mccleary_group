---
layout: page
title: Teaching
---

<!-- NOTE: This page is optional. To remove the teaching section:
     1. Delete this file (teaching.md)
     2. Remove the Teaching link from navigation in _layouts/default.html
-->

<section class="section">
    <div class="container">
        <div class="section-header">
            <h1>Teaching</h1>
            <div class="section-line"></div>
        </div>
        
        <p class="lead-text">
            Courses taught at Northeastern University, Department of Physics
        </p>
        
        <div class="courses-list">
            
            <div class="course-card">
                <img src="/assets/images/teaching/advanced-astro.jpg" alt="Advanced Astrophysics" class="course-image">
                <div class="course-content">
                    <h2>PHYS 5117: Advanced Astrophysics Topics</h2>
                    <p class="course-term">Graduate Course • Spring Semester</p>
                    <p class="course-description">
                        An advanced graduate course exploring cutting-edge topics in modern astrophysics, including gravitational lensing, cosmological parameter estimation, and observational techniques. Students engage with current research literature and develop independent research projects related to observational cosmology.
                    </p>
                    <div class="course-topics">
                        <span class="topic-tag">Gravitational Lensing</span>
                        <span class="topic-tag">Dark Matter</span>
                        <span class="topic-tag">Cosmology</span>
                        <span class="topic-tag">Data Analysis</span>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <img src="/assets/images/teaching/multimessenger.jpg" alt="Multimessenger Astrophysics" class="course-image">
                <div class="course-content">
                    <h2>PHYS 4111: Multimessenger Astrophysics</h2>
                    <p class="course-term">Upper-level Undergraduate • Fall Semester</p>
                    <p class="course-description">
                        An exploration of modern astrophysics through the lens of multimessenger observations. Students learn how electromagnetic radiation, gravitational waves, neutrinos, and cosmic rays provide complementary views of astronomical phenomena. Includes hands-on data analysis projects using real astronomical data.
                    </p>
                    <div class="course-topics">
                        <span class="topic-tag">Gravitational Waves</span>
                        <span class="topic-tag">High-Energy Astrophysics</span>
                        <span class="topic-tag">Data Analysis</span>
                        <span class="topic-tag">Observational Techniques</span>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <img src="/assets/images/teaching/intro-astronomy.jpg" alt="Introduction to Astronomy" class="course-image">
                <div class="course-content">
                    <h2>PHYS 1111: Introduction to Astronomy</h2>
                    <p class="course-term">Introductory Course • Fall & Spring Semesters</p>
                    <p class="course-description">
                        A comprehensive introduction to astronomy for non-science majors. Topics include the solar system, stellar evolution, galaxies, and cosmology. Emphasis on understanding our place in the universe and the methods astronomers use to study distant objects. Includes observational projects and planetarium visits.
                    </p>
                    <div class="course-topics">
                        <span class="topic-tag">Solar System</span>
                        <span class="topic-tag">Stars & Galaxies</span>
                        <span class="topic-tag">Cosmology</span>
                        <span class="topic-tag">Observational Astronomy</span>
                    </div>
                </div>
            </div>
            
        </div>
    </div>
</section>

<style>
.courses-list {
    max-width: 900px;
    margin: 0 auto;
}

.course-card {
    background: #1a1f2e;
    border-radius: 12px;
    padding: 2rem;
    margin-bottom: 2rem;
    border: 1px solid #2d3748;
    display: flex;
    gap: 2rem;
    align-items: start;
}

.course-image {
    width: 200px;
    height: 150px;
    object-fit: cover;
    border-radius: 8px;
    flex-shrink: 0;
}

.course-content {
    flex: 1;
}

.course-term {
    color: #6366f1;
    font-weight: 500;
    margin-bottom: 1rem;
}

.course-description {
    color: #94a3b8;
    line-height: 1.8;
    margin-bottom: 1.5rem;
}

.course-topics {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
}

.topic-tag {
    background: rgba(99, 102, 241, 0.2);
    color: #818cf8;
    padding: 0.375rem 1rem;
    border-radius: 20px;
    font-size: 0.875rem;
}

@media (max-width: 768px) {
    .course-card {
        flex-direction: column;
    }
    
    .course-image {
        width: 100%;
    }
}
</style>
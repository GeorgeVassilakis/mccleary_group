---
layout: page
title: Teaching
permalink: /teaching/
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
                <img src="{{ '/assets/images/teaching/phys5117-textbook.jpg' | relative_url }}" alt="Advanced Astrophysics" class="course-image">
                <div class="course-content">
                    <h2>PHYS 5117: Advanced Astrophysics Topics</h2>
                    <p class="course-term">Graduate Course</p>
                    <p class="course-description">
                        This course focuses on stellar structure and properties, the interstellar medium and the formation of stars and planets, and galaxies. Topics include astronomical distance and brightness measures, stellar spectra analysis, magnetic activity on the Sun including flares and coronal mass ejections, complete star formation and evolution from molecular clouds to compact objects, planetary systems, galaxy formation and evolution, dark matter implications from galaxy clusters, and the large-scale structure of the universe.
                    </p>
                    <div class="course-topics">
                        <span class="topic-tag">Stellar Evolution</span>
                        <span class="topic-tag">Galaxy Formation</span>
                        <span class="topic-tag">Dark Matter</span>
                        <span class="topic-tag">Large-Scale Structure</span>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <img src="{{ '/assets/images/teaching/phys4111-textbook.jpg' | relative_url }}" alt="Multimessenger Astrophysics" class="course-image">
                <div class="course-content">
                    <h2>PHYS 4111: Multimessenger Astrophysics</h2>
                    <p class="course-term">Advanced Undergraduate Level</p>
                    <p class="course-description">
                        The detection of gravitational waves and high-energy cosmic neutrinos has revolutionized astronomy. This course explores how astrophysical processes produce electromagnetic radiation, cosmic rays, neutrinos, and gravitational waves - each carrying distinct information about their sources. Students investigate signals from stars, active galactic nuclei, supernovae, and black holes, while learning about the detectors and techniques used to observe these different messengers. The course provides a solid introduction to the newest discoveries in astrophysics, covering the production, transmission, and detection of these various astrophysical signals.
                    </p>
                    <div class="course-topics">
                        <span class="topic-tag">Gravitational Waves</span>
                        <span class="topic-tag">Neutrino Astronomy</span>
                        <span class="topic-tag">Cosmic Rays</span>
                        <span class="topic-tag">Multi-wavelength Observations</span>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <img src="{{ '/assets/images/teaching/phys1111-textbook.jpg' | relative_url }}" alt="Introduction to Astronomy" class="course-image">
                <div class="course-content">
                    <h2>PHYS 1111: Introduction to Astronomy</h2>
                    <p class="course-term">Introductory Level</p>
                    <p class="course-description">
                        Astrophysics is "the science of everything that isn't nailed down." This course surveys the Universe from our solar system to its infancy, with stops to explore galaxies and extreme objects like black holes and neutron stars. Topics include an introduction to the cosmos, Earth's place in the universe, our solar system (planets, moons, asteroids, and comets), stellar physics and classification, and stellar evolution. Students learn about astronomical tools including the nature of light and radiation, telescopes, and spectroscopy. In-class demonstrations and activities illuminate concepts from lectures.
                    </p>
                    <div class="course-topics">
                        <span class="topic-tag">Solar System</span>
                        <span class="topic-tag">Stellar Physics</span>
                        <span class="topic-tag">Galaxies</span>
                        <span class="topic-tag">Observational Techniques</span>
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
    width: 150px;
    height: 196px;
    aspect-ratio: 13/17;
    object-fit: cover;
    border-radius: 8px;
    flex-shrink: 0;
    background: #141927;
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
        height: auto;
        aspect-ratio: 13/17;
        max-width: 200px;
        margin: 0 auto;
    }
}
</style>
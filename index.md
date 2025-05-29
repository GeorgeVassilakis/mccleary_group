---
layout: home
---

<section class="hero">
    <div class="container">
        <div class="hero-content">
            <h1>Cosmology & Astrophysics Group</h1>
            <p class="tagline">Exploring the Universe through Gravitational Lensing and Galaxy Clusters</p>
            <p class="hero-description">
                Our research group at Northeastern University develops and applies cutting-edge techniques to understand dark matter, galaxy clusters, and the large-scale structure of the universe through gravitational lensing observations from ground, stratosphere, and space.
            </p>
            <div class="cta-buttons">
                <a href="{{ '/research' | relative_url }}" class="btn btn-primary">Our Research</a>
                <a href="{{ '/publications' | relative_url }}" class="btn btn-secondary">Latest Publications</a>
            </div>
        </div>
    </div>
</section>

<!-- About the PI Section -->
<section class="section">
    <div class="container">
        <div class="about-pi">
            <h2>About the PI</h2>
            <div class="pi-content">
                <p>
                    Professor <strong>Jacqueline McCleary</strong> is an observational cosmologist who uses galaxy clusters as a laboratory in which to explore the nature of dark matter and its interaction with galaxies. Her group develops tools to measure galaxy clusters' weak gravitational lensing: the small but coherent distortion of light from distant galaxies by massive foreground objects. Professor McCleary uses data from observatories on mountaintops, in the stratosphere, and in space. She is a collaborator in the Local Volume Complete Cluster Survey (LoVoCCS), the Superpressure Balloon-borne Imaging Telescope (SuperBIT), and COSMOS-Web (a JWST collaboration).
                </p>
                <p>
                    Jacqueline first joined the Department of Physics as a Northeastern ADVANCE Future Faculty Fellow before "graduating" to an assistant professorship in 2022. She has received an MS in astronomy from New Mexico State University, an MS and PhD in physics from Brown University, and was a post-doctoral fellow at NASA's Jet Propulsion Laboratory.
                </p>
            </div>
        </div>
    </div>
</section>

<!-- Research Preview -->
<section class="section section-alt">
    <div class="container">
        <div class="section-header">
            <h2>Our Research</h2>
            <div class="section-line"></div>
        </div>
        <div class="research-grid">
            <div class="research-card">
                <img src="/assets/images/research/superbit-logo.jpeg" alt="Stratospheric observations" class="research-image">
                <h3>Galaxy Cluster Cosmology from the Stratosphere</h3>
                <p>Leading weak gravitational lensing analysis of merging clusters observed with SuperBIT, a stratospheric NUV-to-NIR telescope. We're also developing GigaBIT, its successor mission.</p>
                <a href="{{ '/research#stratosphere' | relative_url }}">Learn more →</a>
            </div>
            
            <div class="research-card">
                <img src="/assets/images/research/cweb-logo.png" alt="COSMOS-Web" class="research-image">
                <h3>Gravitational Lensing with COSMOS-Web</h3>
                <p>Using JWST NIRCam and MIRI observations to characterize PSFs for gravitational lensing analysis and conduct cosmological parameter estimation using 3x2-point correlation functions.</p>
                <a href="{{ '/research#cosmos-web' | relative_url }}">Learn more →</a>
            </div>
            
            <div class="research-card">
                <img src="/assets/images/research/cgm-preview.jpg" alt="Circumgalactic dust" class="research-image">
                <h3>Circumgalactic Dust Halos</h3>
                <p>Exploring dust in the extended circumgalactic and intergalactic medium, studying its effects on distance estimates as a function of galaxy type.</p>
                <a href="{{ '/research#dust' | relative_url }}">Learn more →</a>
            </div>
        </div>
    </div>
</section>

<!-- Team Preview -->
<section class="section">
    <div class="container">
        <div class="section-header">
            <h2>Our Team</h2>
            <div class="section-line"></div>
        </div>
        <div class="team-grid">
            {% for member in site.data.team limit:6 %}
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
        <div style="text-align: center; margin-top: 3rem;">
            <a href="{{ '/team/' | relative_url }}" class="btn btn-primary">View All Team Members</a>
        </div>
    </div>
</section>

<!-- Recent Publications -->
<section class="section section-alt">
    <div class="container">
        <div class="section-header">
            <h2>Recent Publications</h2>
            <div class="section-line"></div>
        </div>
        <div class="publications-list">
            {% for pub in site.data.publications limit:3 %}
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
        <div style="text-align: center; margin-top: 3rem;">
            <a href="{{ '/publications' | relative_url }}" class="btn btn-primary">View All Publications</a>
        </div>
    </div>
</section>
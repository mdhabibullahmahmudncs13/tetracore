<section class="section">
    <h2>Join Our Team</h2>
    <p>We're always looking for talented individuals who are passionate about technology and innovation. Check out our current openings or send us your resume.</p>

    <div class="flex-container" style="margin-top: 2rem;">
        <div class="flex-item">
            <h3>Why Work With Us?</h3>
            <ul style="list-style-position: inside; margin-top: 1rem;">
                <li>Collaborative and innovative work environment</li>
                <li>Opportunity to work on cutting-edge projects</li>
                <li>Professional growth and development opportunities</li>
                <li>Competitive compensation and benefits</li>
                <li>Flexible work arrangements</li>
            </ul>
        </div>

        <div class="flex-item">
            <h3>Current Openings</h3>
            <div style="margin-top: 1rem;">
                <div style="padding: 1rem; background: rgba(255, 255, 255, 0.05); border-radius: var(--border-radius); margin-bottom: 1rem;">
                    <h4>Senior Full-Stack Developer</h4>
                    <p>Join our development team and work on innovative web applications.</p>
                    <a href="#" class="btn" style="margin-top: 0.5rem;">Apply Now</a>
                </div>

                <div style="padding: 1rem; background: rgba(255, 255, 255, 0.05); border-radius: var(--border-radius); margin-bottom: 1rem;">
                    <h4>UX/UI Designer</h4>
                    <p>Help create intuitive and engaging user experiences for our products.</p>
                    <a href="#" class="btn" style="margin-top: 0.5rem;">Apply Now</a>
                </div>

                <div style="padding: 1rem; background: rgba(255, 255, 255, 0.05); border-radius: var(--border-radius);">
                    <h4>Project Manager</h4>
                    <p>Lead our projects from concept to completion with your expertise.</p>
                    <a href="#" class="btn" style="margin-top: 0.5rem;">Apply Now</a>
                </div>
            </div>
        </div>
    </div>

    <div style="text-align: center; margin-top: 2rem;">
        <h3>Don't see a position that fits your skills?</h3>
        <p>We're always interested in meeting talented people. Send us your resume and cover letter.</p>
        <a href="mailto:careers@tetracore.com" class="btn">Send Your Resume</a>
    </div>
</section>

<style>
    .section {
        margin: 2rem 0;
        padding: 2rem;
        background: var(--secondary-bg);
        border-radius: var(--border-radius);
        box-shadow: var(--shadow);
    }

    .section h2 {
        margin-bottom: 1rem;
        color: var(--accent-color);
    }

    .flex-container {
        display: flex;
        flex-wrap: wrap;
        gap: 2rem;
        justify-content: space-between;
    }

    .flex-item {
        flex: 1;
        min-width: 250px;
    }

    .btn {
        display: inline-block;
        margin-top: 1rem;
        padding: 0.75rem 1.5rem;
        background: var(--accent-color);
        color: white;
        text-decoration: none;
        border-radius: 5px;
        transition: background 0.3s, transform 0.2s;
        border: none;
        cursor: pointer;
    }

    .btn:hover {
        background: #5a9aff;
        transform: translateY(-2px);
    }

    @media (max-width: 768px) {
        .section {
            padding: 1.5rem;
        }
    }

    @media (max-width: 480px) {
        .section {
            padding: 1rem;
        }
    }
</style>
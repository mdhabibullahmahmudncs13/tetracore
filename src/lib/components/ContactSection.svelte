<script>
    export let handleFormSubmit;
</script>

<section class="section">
    <h2>Contact Us</h2>
    <p>We'd love to hear from you! Whether you have a question about our services, want to collaborate on a project, or are interested in joining our team, get in touch with us.</p>

    <div class="flex-container" style="margin-top: 2rem;">
        <div class="flex-item">
            <div class="info-box">
                <h3>Ready to innovate?</h3>
                <p>Fill out the form and our team will get back to you within 24 hours. We're excited to learn about your project and explore how we can help you achieve your goals.</p>
            </div>

            <div class="contact-info">
                <h3>Contact Information</h3>
                <div class="contact-info-item">
                    <i>📍</i>
                    <div>
                        <strong>Address:</strong>
                        <p>123 Tech Park Avenue, Innovation District, San Francisco, CA 94105</p>
                    </div>
                </div>

                <div class="contact-info-item">
                    <i>📞</i>
                    <div>
                        <strong>Phone:</strong>
                        <p>+1 (555) 123-4567</p>
                    </div>
                </div>

                <div class="contact-info-item">
                    <i>✉️</i>
                    <div>
                        <strong>Email:</strong>
                        <p>info@tetracore.com</p>
                    </div>
                </div>

                <div class="contact-info-item">
                    <i>⏰</i>
                    <div>
                        <strong>Hours:</strong>
                        <p>Monday - Friday: 9:00 AM - 6:00 PM</p>
                        <p>Saturday: 10:00 AM - 3:00 PM</p>
                    </div>
                </div>

                <h4 style="margin-top: 1.5rem;">Connect With Us</h4>
                <div class="social-links">
                    <a href="#" class="social-link" title="Facebook">fb</a>
                    <a href="#" class="social-link" title="Twitter">tw</a>
                    <a href="#" class="social-link" title="LinkedIn">in</a>
                    <a href="#" class="social-link" title="Instagram">ig</a>
                    <a href="#" class="social-link" title="GitHub">gh</a>
                </div>
            </div>

            <div class="map-container">
                <div class="map-placeholder">
                    <p>Map location of Tetra Core HQ</p>
                </div>
            </div>
        </div>

        <div class="flex-item">
            <h3>Send Us a Message</h3>
            <form class="contact-form" on:submit={handleFormSubmit}>
                <div class="form-group">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" class="form-control" placeholder="Enter your full name" required>
                </div>

                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" class="form-control" placeholder="Enter your email address" required>
                </div>

                <div class="form-group">
                    <label for="phone">Phone Number (Optional)</label>
                    <input type="tel" id="phone" class="form-control" placeholder="Enter your phone number">
                </div>

                <div class="form-group">
                    <label for="subject">Subject</label>
                    <select id="subject" class="form-control" required>
                        <option value="" disabled selected>Select a subject</option>
                        <option value="general">General Inquiry</option>
                        <option value="services">Services</option>
                        <option value="partnership">Partnership Opportunity</option>
                        <option value="career">Career Information</option>
                        <option value="support">Technical Support</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="message">Your Message</label>
                    <textarea id="message" class="form-control" placeholder="Enter your message here..." required></textarea>
                </div>

                <div class="form-group">
                    <label>
                        <input type="checkbox" required>
                        I agree to the processing of my personal data in accordance with the <a href="#" style="color: var(--accent-color);">Privacy Policy</a>
                    </label>
                </div>

                <button type="submit" class="btn">Send Message</button>
            </form>
        </div>
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

    .contact-form {
        margin-top: 2rem;
    }

    .form-group {
        margin-bottom: 1.5rem;
    }

    .form-group label {
        display: block;
        margin-bottom: 0.5rem;
        font-weight: bold;
    }

    .form-control {
        width: 100%;
        padding: 0.75rem;
        border: 1px solid var(--input-border);
        background-color: var(--input-bg);
        color: var(--text-color);
        border-radius: 5px;
        font-family: inherit;
        font-size: 1rem;
        transition: border-color 0.3s, box-shadow 0.3s;
    }

    .form-control:focus {
        outline: none;
        border-color: var(--accent-color);
        box-shadow: 0 0 0 2px rgba(66, 135, 245, 0.3);
    }

    textarea.form-control {
        min-height: 150px;
        resize: vertical;
    }

    .contact-info {
        background: rgba(255, 255, 255, 0.05);
        padding: 1.5rem;
        border-radius: var(--border-radius);
        margin-bottom: 1.5rem;
    }

    .contact-info-item {
        margin-bottom: 1rem;
        display: flex;
        align-items: flex-start;
    }

    .contact-info-item i {
        margin-right: 1rem;
        color: var(--accent-color);
        font-size: 1.2rem;
    }

    .social-links {
        display: flex;
        gap: 1rem;
        margin-top: 1.5rem;
    }

    .social-link {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.1);
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text-color);
        text-decoration: none;
        transition: background 0.3s, transform 0.2s;
    }

    .social-link:hover {
        background: var(--accent-color);
        transform: translateY(-3px);
    }

    .info-box {
        background: rgba(255, 255, 255, 0.05);
        padding: 1.5rem;
        border-radius: var(--border-radius);
        margin-bottom: 1.5rem;
        border-left: 4px solid var(--accent-color);
    }

    .map-container {
        width: 100%;
        height: 300px;
        background: var(--input-bg);
        border-radius: var(--border-radius);
        overflow: hidden;
        margin-top: 2rem;
    }

    .map-placeholder {
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        background: url('/api/placeholder/800/300') center/cover;
        color: var(--text-color);
        font-weight: bold;
        text-align: center;
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
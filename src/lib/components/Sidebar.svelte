<div class="sidebar">
    <div class="sidebar-section">
        <h3>Categories</h3>
        <ul class="popular-posts">
            <li><a href="#">Technology (15)</a></li>
            <li><a href="#">Innovation (12)</a></li>
            <li><a href="#">AI & Machine Learning (9)</a></li>
            <li><a href="#">IoT (7)</a></li>
            <li><a href="#">Company News (5)</a></li>
            <li><a href="#">Case Studies (4)</a></li>
        </ul>
    </div>

    <div class="sidebar-section">
        <h3>Popular Posts</h3>
        <ul class="popular-posts">
            <li><a href="#">How AI is Transforming Modern Education</a></li>
            <li><a href="#">The Future of AI in Educational Technology</a></li>
            <li><a href="#">Ethical Considerations in AI Development</a></li>
            <li><a href="#">The Connected Home: Beyond Convenience</a></li>
            <li><a href="#">Blockchain Applications Beyond Cryptocurrency</a></li>
        </ul>
    </div>

    <div class="sidebar-section">
        <h3>Tags</h3>
        <div class="tag-cloud">
            <span class="tag">AI</span>
            <span class="tag">Machine Learning</span>
            <span class="tag">IoT</span>
            <span class="tag">Blockchain</span>
            <span class="tag">Education</span>
            <span class="tag">Innovation</span>
            <span class="tag">Technology</span>
            <span class="tag">Smart Homes</span>
            <span class="tag">Manufacturing</span>
            <span class="tag">Ethics</span>
            <span class="tag">Data Science</span>
        </div>
    </div>

    <div class="sidebar-section">
        <h3>Subscribe</h3>
        <p>Stay updated with our latest articles and news.</p>
        <form style="margin-top: 1rem;">
            <input type="email" class="search-input" placeholder="Your email address" style="margin-bottom: 1rem;">
            <button type="submit" class="btn" style="width: 100%;">Subscribe</button>
        </form>
    </div>
</div>

<style>
    .sidebar {
        position: sticky;
        top: 90px;
        height: fit-content;
    }

    .sidebar-section {
        background: var(--secondary-bg);
        border-radius: var(--border-radius);
        padding: 1.5rem;
        margin-bottom: 2rem;
        box-shadow: var(--shadow);
    }

    .sidebar-section h3 {
        margin-bottom: 1rem;
        color: var(--accent-color);
    }

    .tag-cloud {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
    }

    .tag {
        background: rgba(255, 255, 255, 0.1);
        color: var(--text-color);
        padding: 0.25rem 0.75rem;
        border-radius: 20px;
        font-size: 0.8rem;
        display: inline-block;
        transition: background 0.3s, color 0.3s;
    }

    .tag:hover {
        background: var(--accent-color);
        color: white;
        cursor: pointer;
    }

    .popular-posts li {
        margin-bottom: 1rem;
        list-style: none;
    }

    .popular-posts a {
        color: var(--text-color);
        text-decoration: none;
        transition: color 0.3s;
    }

    .popular-posts a:hover {
        color: var(--accent-color);
    }
</style>
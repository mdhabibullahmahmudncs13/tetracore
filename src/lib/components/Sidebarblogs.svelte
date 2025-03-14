<script>
    // Example data for categories, popular posts, and tags
    const categories = [
        { name: "Technology", count: 15 },
        { name: "Innovation", count: 12 },
        { name: "AI & Machine Learning", count: 9 },
        { name: "IoT", count: 7 },
        { name: "Company News", count: 5 },
        { name: "Case Studies", count: 4 },
    ];

    const popularPosts = [
        "How AI is Transforming Modern Education",
        "The Future of AI in Educational Technology",
        "Ethical Considerations in AI Development",
        "The Connected Home: Beyond Convenience",
        "Blockchain Applications Beyond Cryptocurrency",
    ];

    const tags = [
        "AI",
        "Machine Learning",
        "IoT",
        "Blockchain",
        "Education",
        "Innovation",
        "Technology",
        "Smart Homes",
        "Manufacturing",
        "Ethics",
        "Data Science",
    ];

    // Function to handle subscription form submission
    function handleSubscribe(event) {
        event.preventDefault();
        const email = event.target.email.value;
        console.log("Subscribed with email:", email);
        alert(`Thank you for subscribing! We'll send updates to ${email}.`);
        event.target.reset(); // Reset the form
    }
</script>

<div class="sidebar-section">
    <h3>Categories</h3>
    <ul class="popular-posts">
        {#each categories as category}
            <li>
                <a href="#">{category.name} ({category.count})</a>
            </li>
        {/each}
    </ul>
</div>

<div class="sidebar-section">
    <h3>Popular Posts</h3>
    <ul class="popular-posts">
        {#each popularPosts as post}
            <li>
                <a href="#">{post}</a>
            </li>
        {/each}
    </ul>
</div>

<div class="sidebar-section">
    <h3>Tags</h3>
    <div class="tag-cloud">
        {#each tags as tag}
            <span class="tag">{tag}</span>
        {/each}
    </div>
</div>

<div class="sidebar-section">
    <h3>Subscribe</h3>
    <p>Stay updated with our latest articles and news.</p>
    <form on:submit={handleSubscribe} style="margin-top: 1rem;">
        <input
            type="email"
            name="email"
            class="search-input"
            placeholder="Your email address"
            style="margin-bottom: 1rem;"
            required
        />
        <button type="submit" class="btn" style="width: 100%;">Subscribe</button>
    </form>
</div>

<style>
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

    .popular-posts {
        list-style: none;
        padding: 0;
    }

    .popular-posts li {
        margin-bottom: 1rem;
    }

    .popular-posts a {
        color: var(--text-color);
        text-decoration: none;
        transition: color 0.3s;
    }

    .popular-posts a:hover {
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

    .search-input {
        width: 100%;
        padding: 0.75rem;
        border: none;
        background: rgba(255, 255, 255, 0.1);
        color: var(--text-color);
        border-radius: var(--border-radius);
        font-size: 1rem;
    }

    .search-input::placeholder {
        color: rgba(255, 255, 255, 0.5);
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
</style>
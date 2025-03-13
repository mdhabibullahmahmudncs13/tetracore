<script>
    import Header from './components/Header.svelte';
    import Nav from './components/Nav.svelte';
    import Footer from './components/Footer.svelte';
    import BlogCard from './components/BlogCard.svelte';
    import Sidebar from './components/Sidebar.svelte';

    let activeFilter = 'all';
    let searchQuery = '';

    const featuredPost = {
        image: "/asset/AI-Powered Job Recruitment & Skill Matching_ Transforming the Hiring Landscape.jpg",
        title: "AI-Powered Job Recruitment & Skill Matching: Transforming the Hiring Landscape",
        date: "March 5, 2025",
        author: "Sarah Chen",
        readTime: "8 min read",
        category: "Featured",
        link: "/more/blog/blog1.html"
    };

    const posts = [
        {
            image: "/api/placeholder/400/200",
            title: "How AI is Transforming Modern Education",
            date: "March 8, 2025",
            author: "John Doe",
            category: "Technology",
            excerpt: "Explore how artificial intelligence technologies are revolutionizing classroom learning and making education more accessible and personalized than ever before.",
            link: "#"
        },
        {
            image: "/api/placeholder/400/200",
            title: "The Rise of Smart Manufacturing",
            date: "March 2, 2025",
            author: "Jane Smith",
            category: "Innovation",
            excerpt: "Manufacturing is undergoing a digital transformation with IoT sensors, real-time analytics, and predictive maintenance reshaping factory floors worldwide.",
            link: "#"
        },
        {
            image: "/api/placeholder/400/200",
            title: "Ethical Considerations in AI Development",
            date: "February 25, 2025",
            author: "Alice Johnson",
            category: "AI & ML",
            excerpt: "As AI becomes more integrated into our daily lives, we must address the ethical implications and build frameworks for responsible innovation.",
            link: "#"
        },
        {
            image: "/api/placeholder/400/200",
            title: "Tetra Core Partners with Global Education Initiative",
            date: "February 20, 2025",
            author: "Tetra Core",
            category: "Company News",
            excerpt: "We're proud to announce our partnership with the Global Education Initiative to bring tech education to underserved communities worldwide.",
            link: "#"
        },
        {
            image: "/api/placeholder/400/200",
            title: "The Connected Home: Beyond Convenience",
            date: "February 15, 2025",
            author: "Bob Brown",
            category: "IoT",
            excerpt: "Smart home technology is evolving beyond simple convenience features to address energy efficiency, security, and accessibility concerns.",
            link: "#"
        },
        {
            image: "/api/placeholder/400/200",
            title: "Blockchain Applications Beyond Cryptocurrency",
            date: "February 10, 2025",
            author: "Charlie Davis",
            category: "Technology",
            excerpt: "Discover how blockchain technology is being leveraged in supply chain, healthcare, voting systems, and more to increase transparency and security.",
            link: "#"
        }
    ];

    function filterPosts(category) {
        activeFilter = category;
    }

    function isActive(filter) {
        return activeFilter === filter ? 'active' : '';
    }

    const filteredPosts = posts.filter(post => 
        (activeFilter === 'all' || post.category === activeFilter) &&
        (searchQuery === '' || post.title.toLowerCase().includes(searchQuery.toLowerCase()))
    );
</script>

<Header />
<Nav />

<div class="container">
    <div class="featured-blog">
        <img src={featuredPost.image} alt={featuredPost.title} />
        <div class="featured-content">
            <span class="featured-tag">{featuredPost.category}</span>
            <h2>{featuredPost.title}</h2>
            <p class="meta">{featuredPost.date} | By {featuredPost.author} | {featuredPost.readTime}</p>
            <a href={featuredPost.link} class="btn">Read Article</a>
        </div>
    </div>

    <div class="blog-layout">
        <div class="main-content">
            <section class="section">
                <h2>Latest Articles</h2>

                <div class="search-container">
                    <input type="text" class="search-input" placeholder="Search articles..." bind:value={searchQuery}>
                </div>

                <div class="blog-filter">
                    <button class="filter-btn {isActive('all')}" on:click={() => filterPosts('all')}>All</button>
                    <button class="filter-btn {isActive('Technology')}" on:click={() => filterPosts('Technology')}>Technology</button>
                    <button class="filter-btn {isActive('Innovation')}" on:click={() => filterPosts('Innovation')}>Innovation</button>
                    <button class="filter-btn {isActive('AI & ML')}" on:click={() => filterPosts('AI & ML')}>AI & ML</button>
                    <button class="filter-btn {isActive('IoT')}" on:click={() => filterPosts('IoT')}>IoT</button>
                    <button class="filter-btn {isActive('Company News')}" on:click={() => filterPosts('Company News')}>Company News</button>
                </div>

                <div class="blog-grid">
                    {#each filteredPosts as post}
                        <BlogCard {...post} />
                    {/each}
                </div>

                <div class="pagination">
                    <a href="#" class="page-link active">1</a>
                    <a href="#" class="page-link">2</a>
                    <a href="#" class="page-link">3</a>
                    <a href="#" class="page-link">4</a>
                    <a href="#" class="page-link">></a>
                </div>
            </section>
        </div>

        <Sidebar />
    </div>
</div>

<Footer />

<style>
    :root {
        --primary-bg: #121212;
        --secondary-bg: #1e1e1e;
        --text-color: #e0e0e0;
        --accent-color: #4287f5;
        --shadow: 0px 2px 5px rgba(0, 0, 0, 0.5);
        --border-radius: 10px;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem 1rem;
    }

    .featured-blog {
        margin-bottom: 3rem;
        border-radius: var(--border-radius);
        overflow: hidden;
        position: relative;
    }

    .featured-blog img {
        width: 100%;
        height: 400px;
        object-fit: cover;
    }

    .featured-content {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        padding: 2rem;
        background: linear-gradient(to top, rgba(0,0,0,0.9), rgba(0,0,0,0));
    }

    .featured-tag {
        background: var(--accent-color);
        color: white;
        padding: 0.25rem 0.75rem;
        border-radius: 20px;
        font-size: 0.8rem;
        display: inline-block;
        margin-bottom: 0.5rem;
    }

    .blog-layout {
        display: grid;
        grid-template-columns: 1fr 300px;
        gap: 2rem;
    }

    .search-container {
        margin-bottom: 2rem;
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

    .blog-filter {
        display: flex;
        flex-wrap: wrap;
        gap: 1rem;
        margin-bottom: 2rem;
    }

    .filter-btn {
        padding: 0.5rem 1rem;
        background: rgba(255, 255, 255, 0.1);
        border: none;
        color: var(--text-color);
        border-radius: 20px;
        cursor: pointer;
        transition: background 0.3s, color 0.3s;
    }

    .filter-btn:hover, .filter-btn.active {
        background: var(--accent-color);
        color: white;
    }

    .blog-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
        gap: 2rem;
        margin-top: 2rem;
    }

    .pagination {
        display: flex;
        justify-content: center;
        margin-top: 3rem;
        gap: 0.5rem;
    }

    .page-link {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: 40px;
        background: rgba(255, 255, 255, 0.1);
        color: var(--text-color);
        text-decoration: none;
        border-radius: 50%;
        transition: background 0.3s, color 0.3s;
    }

    .page-link:hover, .page-link.active {
        background: var(--accent-color);
        color: white;
    }

    @media (max-width: 992px) {
        .blog-layout {
            grid-template-columns: 1fr;
        }
    }

    @media (max-width: 768px) {
        .featured-blog img {
            height: 300px;
        }
    }

    @media (max-width: 480px) {
        .featured-blog img {
            height: 250px;
        }

        .blog-grid {
            grid-template-columns: 1fr;
        }
    }
</style>
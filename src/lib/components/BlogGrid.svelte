<script lang="ts">
    let activeFilter = 'All';
    let currentPage = 1;

    function setFilter(filter: string) {
        activeFilter = filter;
        console.log('Filter selected:', filter);
    }

    function searchArticles(event: KeyboardEvent) {
        if (event.key === 'Enter') {
            console.log('Search for:', (event.target as HTMLInputElement).value);
        }
    }

    function goToPage(page: number) {
        currentPage = page;
        console.log('Navigating to page:', page);
    }
</script>

<section class="section">
    <h2>Latest Articles</h2>

    <div class="search-container">
        <input type="text" class="search-input" placeholder="Search articles..." on:keyup={searchArticles}>
    </div>

    <div class="blog-filter">
        <button class="filter-btn" class:active={activeFilter === 'All'} on:click={() => setFilter('All')}>All</button>
        <button class="filter-btn" class:active={activeFilter === 'Technology'} on:click={() => setFilter('Technology')}>Technology</button>
        <button class="filter-btn" class:active={activeFilter === 'Innovation'} on:click={() => setFilter('Innovation')}>Innovation</button>
        <button class="filter-btn" class:active={activeFilter === 'AI & ML'} on:click={() => setFilter('AI & ML')}>AI & ML</button>
        <button class="filter-btn" class:active={activeFilter === 'IoT'} on:click={() => setFilter('IoT')}>IoT</button>
        <button class="filter-btn" class:active={activeFilter === 'Company News'} on:click={() => setFilter('Company News')}>Company News</button>
    </div>
    
    <div class="blog-grid">
        <!-- Blog posts will go here -->
    </div>

    <div class="pagination">
        <a href="#" class="page-link active">1</a>
        <a href="#" class="page-link">2</a>
        <a href="#" class="page-link">3</a>
        <a href="#" class="page-link">4</a>
        <a href="#" class="page-link">></a>
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

    @media (max-width: 480px) {
        .blog-grid {
            grid-template-columns: 1fr;
        }
    }
</style>
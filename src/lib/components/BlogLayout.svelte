<script>
    import BlogGrid from '$lib/components/BlogGrid.svelte';
    import Sidebar from './Sidebarblogs.svelte';
</script>

<div class="blog-layout">
    <div class="main-content">
        <BlogGrid />
    </div>
    <div class="sidebar">
        <Sidebar />
    </div>
</div>

<style>
    .blog-layout {
        display: grid;
        grid-template-columns: 1fr 300px;
        gap: 2rem;
    }

    .sidebar {
        position: sticky;
        top: 90px;
        height: fit-content;
    }

    @media (max-width: 992px) {
        .blog-layout {
            grid-template-columns: 1fr;
        }

        .sidebar {
            position: static;
        }
    }
</style>
<script>
    export let image;
    export let title;
    export let date;
    // svelte-ignore export_let_unused
        export let author;
    export let category;
    export let excerpt;
    export let link;
</script>

<div class="blog-card">
    <img src={image} alt={title} />
    <div class="content">
        <span class="meta">{date} | {category}</span>
        <h3>{title}</h3>
        <p class="excerpt">{excerpt}</p>
        <a href={link} class="btn">Read More</a>
    </div>
</div>

<style>
    .blog-card {
        background: rgba(255, 255, 255, 0.05);
        border-radius: var(--border-radius);
        overflow: hidden;
        transition: transform 0.3s, box-shadow 0.3s;
        display: flex;
        flex-direction: column;
    }

    .blog-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
    }

    .blog-card img {
        width: 100%;
        height: 200px;
        object-fit: cover;
    }

    .blog-card .content {
        padding: 1.5rem;
        flex-grow: 1;
        display: flex;
        flex-direction: column;
    }

    .blog-card .meta {
        font-size: 0.9rem;
        color: #aaa;
        margin-bottom: 0.5rem;
    }

    .blog-card .excerpt {
        margin: 1rem 0;
        flex-grow: 1;
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
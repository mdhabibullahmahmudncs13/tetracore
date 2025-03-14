<script>
    import Header from '$lib/components/Header.svelte';
    import Nav from '$lib/components/Nav.svelte';
    import ContactSection from '$lib/components/ContactSection.svelte';
    import JoinTeamSection from '$lib/components/JoinTeamSection.svelte';
    import FAQSection from '$lib/components/FAQSection.svelte';
    import Footer from '$lib/components/Footer.svelte';

    function toggleMenu() {
        const menu = document.querySelector('.menu');
        if (menu) {
            menu.classList.toggle('active');
        }
    }

    // @ts-ignore
    function handleFormSubmit(e) {
        e.preventDefault();
        alert('Thank you for your message! We will get back to you soon.');
        e.target.reset();
    }
</script>

<svelte:head>
    <title>Tetra Core | Contact Us</title>
    <link rel="icon" href="/asset/z.png" type="image/png">
</svelte:head>

<Header />
<Nav />

<main class="container">
    <ContactSection {handleFormSubmit} />
    <JoinTeamSection />
    <FAQSection />
</main>

<Footer />
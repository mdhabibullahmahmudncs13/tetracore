<script>
    import Header from '$lib/components/Header.svelte';
    import Nav from '$lib/components/Nav.svelte';
    import Section from '$lib/components/Section.svelte';
    import ProjectCard from '$lib/components/ProjectCard.svelte';
    import AchievementItem from '$lib/components/AchievementItem.svelte';
    import Footer from '$lib/components/Footer.svelte';
    import Button from '$lib/components/Button.svelte';

    const projects = [
        {
            image: "/asset/DIG THE DATA 3.0.png",
            title: "Dig The Data 3.0",
            description: "An Education Exam System that enables teams to join quizzes, request hints, track scores, and manage users using Django for secure authentication."
        },
        {
            image: "/asset/unihub.png",
            title: "UNI-HUB",
            description: "A comprehensive application for managing university resources, courses, and student information."
        },
        {
            image: "/api/placeholder/400/200",
            title: "Smart IoT Solutions",
            description: "Connected devices and sensors that work together to create intelligent environments for homes, offices, and industrial settings."
        }
    ];

    const achievements = [
        {
            title: "Winner - Tech Innovation Awards 2024",
            description: "Recognized for our outstanding contribution to educational technology solutions."
        },
        {
            title: "Featured in Tech Today Magazine",
            description: "Our AI Analytics Platform was highlighted as one of the most promising innovations of the year."
        },
        {
            title: "Community Impact Award",
            description: "Honored for developing accessible technology solutions for underserved communities."
        }
    ];
</script>

<Header />
<Nav />

<div class="container">
    <Section id="about" title="About Us">
        <div class="flex-container">
            <div class="flex-item">
                <h3>Our Mission</h3>
                <p>We aim to innovate and create cutting-edge technology solutions that make a difference in people's lives and address real-world challenges.</p>
            </div>
            <div class="flex-item">
                <h3>Our Vision</h3>
                <p>To be a leader in technology and innovation, driving progress, fostering creativity, and making a positive impact globally.</p>
            </div>
        </div>
    </Section>

    <Section id="projects" title="Our Projects">
        <p>We have worked on a variety of innovative projects, from AI-driven applications to smart robotic solutions.</p>
        <div class="projects-container">
            {#each projects as project}
                <ProjectCard {...project} />
            {/each}
        </div>
        <div class="text-center">
            <Button href="#" text="Explore All Projects" />
        </div>
    </Section>

    <Section id="achievements" title="Our Achievements">
        <div class="achievement-items">
            {#each achievements as achievement}
                <AchievementItem {...achievement} />
            {/each}
        </div>
        <div class="text-center">
            <Button href="#" text="View More Achievements" />
        </div>
    </Section>

    <Section id="contact" title="Join Us">
        <p>If you're passionate about technology and innovation, be a part of our journey to shape the future.</p>
        <div class="flex-container" style="margin-top: 2rem;">
            <div class="flex-item">
                <h3>Get in Touch</h3>
                <p>Have questions or want to collaborate? We'd love to hear from you!</p>
                <Button href="/contact" text="Contact Us" />
            </div>
            <div class="flex-item">
                <h3>Join Our Team</h3>
                <p>Looking for talented individuals who are passionate about making a difference through technology.</p>
                <Button href="/contact" text="View Opportunities" />
            </div>
        </div>
    </Section>
</div>

<Footer />

<style>
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem 1rem;
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

    .projects-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
        margin-top: 2rem;
    }

    .text-center {
        text-align: center;
        margin-top: 2rem;
    }

    

    @media (max-width: 480px) {
        .projects-container {
            grid-template-columns: 1fr;
        }
    }
</style>
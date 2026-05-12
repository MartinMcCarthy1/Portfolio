<script>
    import {base} from '$app/paths';

    const socials = [
        {name: 'YouTube', link: '#'},
         { name: 'Twitter', link: '#' },
        { name: 'Instagram', link: '#' },
        { name: 'LinkedIn', link: '#' }
    ];
</script>

<svelte:head>
    <title>Martin McCarhty Portfolio</title>
    <meta
        name="description"
        content="personal portfolio website"
    />
</svelte:head>

<div class="page">

<!-- NAVBAR -->
 <nav>
    <h1>Portfolio</h1>

    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About Me</a></li>
        <li><a href="#work">My Work</a></li>
        <li><a href="#contact">Contacts</a></li>
    </ul>
 </nav>

 <!--HERO-->
 <section id="home" class="hero">
    <h2>Martin McCarthy</h2>
    <p>Designer & Digital Artist</p>

    <a href="#work" class="work-button">View My Work</a>
 </section>

 <!--ABOUT-->
 <section id="about" class="section">
    <h3>About Me</h3>

    <div class="about-container">

        <img
            src={base + '/headshot.jpeg'}
            alt="Martin McCarthy headshot"
            class="headshot"
        />

        <div class="about-text">
            <p>
                I am an IDAD student at SETU Carlow with a passion for animation,
                digital art, game design, and voice acting.
            </p>

            <p>
                Alongside my studies, I work as a barman in a hotel and perform
                in productions with my local musical society. These experiences
                have helped me develop strong communication, teamwork, and
                creative skills.
            </p>

        </div>

    </div>
 </section>

 <!--WORK-->
 <section id="work" class="section">
    <h3>My Work</h3>

    <div class="projects">
        <div class="card">
            <h4>Art</h4>
            <p>Physical & Digital art.</p>
        </div>

        <div class="card">
            <h4>Animations</h4>
            <p>assignment & person animations.</p>
        </div>

        <div class="card">
            <h4>Games</h4>
            <p>games ive made or worked on.</p>
        </div>

    </div>
 </section>

 <!--CONTACT-->
 <section id="contact" class="contact">
    <h3>Contacts</h3>

    <p>Email: murt200293@gmail.com</p>
    <p>Phone Number: 087 4467729</p>

    <div class="socials">
        {#each socials as social}
        <a href={social.link}>
            {social.name}
        </a>
        {/each}
    </div>
 </section>

</div>

<style>
    :global(body) {
        margin: 0;
        font-family: Arial, sans-serif;
        background: #202020;
        color: white;
        scroll-behavior: smooth;
    }

    .page{
        width: 100%;
    }

    /*NAVBAR*/

    nav{
        position: sticky;
        top: 0;

        display: flex;
        justify-content: space-between;
        align-items: center;

        padding: 1.5rem 3rem;

        background: #2d49b9;
        box-shadow: 0 2px 10px rgba(0,0,0,0.05);

        z-index: 1000;
    }

    nav h1{
        margin: 0;
        font-size: 1.8rem;
    }

    nav ul{
        display: flex;
        gap: 2rem;
        list-style: none;
        margin: 0;
        padding: 0;
    }

    nav a{
        text-decoration: none;
        color: white;
        transition: 0.3s;
    }

    nav a:hover{
        opacity: 0.6;
    }

    /*HERO*/

    .hero{
        min-height: 90vh;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        text-align: center;
        padding: 2rem;
    }

    .hero h2{
        font-size: 5rem;
        margin-bottom: 1rem;
    }

    .hero p{
        font-size: 1.3rem;
        margin-bottom: 2rem;
    }

    .work-button {
        padding: 1rem 2rem;
        border: none;
        border-radius: 10px;

        background: black;
        color: white;

        cursor: pointer;
        transition: 0.3s;
    }

    .work-button:hover {
        transform: translateY(-2px);
    }

    /*SECTIONS*/

    .section{
        padding: 6rem 2rem;
        text-align: center;
    }

    .section h3 {
        font-size: 2.5rem;
        margin-bottom: 2rem;
    }

    .about-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 3rem;

    max-width: 1000px;
    margin: auto;

    flex-wrap: wrap;
    }

    .about-container p {
        max-width: 500px;
        line-height: 1.8;
        font-size: 1.1rem;
        text-align: left;
    }

    .about-text {
    max-width: 500px;
    text-align: left;
    }

    .about-text p {
    line-height: 1.8;
    margin-bottom: 1.5rem;
    }
    
    .headshot {
    width: 250px;
    height: 250px;

    object-fit: cover;

    border-radius: 50%;

    border: 4px solid #2d49b9;

    box-shadow: 0 5px 20px rgba(0,0,0,0.3);
    }

    /*PROJECTS*/

    .projects {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));

        gap: 2rem;
        margin-top: 3rem;
    }

    .card {
        background: #747883;
        padding: 2rem;
        border-radius: 16px;

        box-shadow: 0 5px 20px rgba(0,0,0,0.05);

        transition: 0.3s;
    }

    .card:hover {
        transform: translateY(-5px);
    }

    /*CONTACT*/

    .contact {
        background: #2d49b9;
        color: white;

        text-align: center;
        padding: 5rem 2rem;
    }

    .socials {
        display: flex;
        justify-content: center;
        gap: 2rem;

        margin-top: 2rem;
        flex-wrap: wrap;
    }

    .socials a {
        color: white;
        text-decoration: none;
    }


    /* MOBILE */

  @media (max-width: 768px) {

    nav {
      flex-direction: column;
      gap: 1rem;
    }

    nav ul {
      flex-wrap: wrap;
      justify-content: center;
    }

    .hero h2 {
      font-size: 3rem;
    }

  }
</style>
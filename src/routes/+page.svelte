<script>
    const socials = [
        {name: 'YouTube', limk: '#'},
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

    <button>Veiw My Work</button>
 </section>

 <!--ABOUT-->
 <section id="about" class="section">
    <h3>About Me</h3>

    <p>
        I am an IDAD student at SETU carlow with a specific intrest in animation,
        digital art and voice  acting.
    </p>
 </section>

 <!--WORK-->
 <section id="work" class="section">
    <h3>My Work</h3>

    <div class="Projects">
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
        background: #f4f4f4;
        color: #111;
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

        background: white;
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
        color: black;
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

    button {
        padding: 1rem 2rem;
        border: none;
        border-radius: 10px;

        background: black;
        color: white;

        cursor: pointer;
        transition: 0.3s;
    }

    button:hover {
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

    /*PROJECTS*/

    .projects {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));

        gap: 2rem;
        margin-top: 3rem;
    }

    .card {
        background: white;
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
        background: #111;
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
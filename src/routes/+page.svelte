<script lang="ts">
    import "../styles/global.css"
    import Footer from './components/footer.svelte'

    let tituloDoJogo: string = "TERMO"
</script>

<title>{tituloDoJogo}</title>

<header class="header">
    <div class="logoHeader">
        <h1>TERMO</h1>
    </div>
</header>

<article class="block">
    <figure class="logo">
        <img src="\images\Logo.png" alt="Logo T">
    </figure>
    <nav class="menuHomePage">
        <a class="menu" href="/play">Play</a>
        <a class="menu" href="/about">About</a>
    </nav>
</article>

<Footer />
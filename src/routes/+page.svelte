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
    <div class="menuHomePage">
        <a class="menu" href="/jogar">Play</a>
        <a class="menu" href="/sobre">About</a>
    </div>
</article>

<Footer />
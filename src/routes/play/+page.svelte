<script lang="ts">
    import "../../styles/global.css"
    import "../../styles/play.css"
	import Footer from "../components/footer.svelte";
    import Keyboard from "../components/gamePage/keyboard.svelte";
    import TableGame from "../components/gamePage/tableGame.svelte";

    let tituloDoJogo: string = "TERMO"
</script>

<title>{tituloDoJogo}</title>

<header class="header">
    <h1>TERMO</h1>
    <nav class="navigationMenu">
        <a class="menu" href="/">Home Page</a>
        <a class="menu" href="/about">About</a>
    </nav>
</header>

<main id="game">
    <TableGame />
    <Keyboard />
</main>

<Footer />
<script lang="ts">
	import '../../styles/global.css';
	import '../../styles/play.css';
	import Footer from '../components/footer.svelte';
	import TableGame from '../components/gamePage/tableGame.svelte';
	import Instructions from '../components/instructions.svelte';

	let tituloDoJogo: string = 'TERMO';
	let modalClose: boolean = false;

	function toggleModal(): void {
		modalClose = !modalClose;
	}

	function reloadPage(): void {
		window.location.reload();
	}
</script>

<title>{tituloDoJogo}</title>

<header class="header">
	<h1>TERMO</h1>
	<nav class="navigationMenu">
		<a class="menu" href="/">Home Page</a>
		<a class="menu" href="/play" on:click={reloadPage}>Play</a>
		<a class="menu" href="/about">About</a>
	</nav>
</header>

<main id="game">
	<TableGame />
	<button type="button" class="rules" on:click={toggleModal}>Show Instructions</button>
</main>

<Footer />
<Instructions {modalClose} {toggleModal}/>

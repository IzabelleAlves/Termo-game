<script lang="ts">
	import '../../styles/global.css';
	import '../../styles/play.css';
	import Footer from '../components/footer.svelte';
	import TableGame from '../components/gamePage/tableGame.svelte';

	let tituloDoJogo: string = 'TERMO';
	let modalClose: boolean = false

	function toggleModal() {
		modalClose = !modalClose
	}

	function reloadPage() {
		window.location.reload()
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

<section class:close={modalClose} class="bg-intructions">
	<section class="game-instructions">
		<h3>How it works:</h3>
		<p>
			Find the right word in 6 (six) tries. After each attempt, The tiles show how close you are to
			the solution.
		</p>
	
		<p>
			<span class="letter right">t</span>
			<span class="letter">u</span>
			<span class="letter">r</span>
			<span class="letter">m</span>
			<span class="letter">a</span>
		</p>
	
		<p>
			The letter <span class="letter right alone">t</span> is part of the word and is in the correct position.
		</p>
	
		<p>
			<span class="letter">v</span>
			<span class="letter">i</span>
			<span class="letter wrong">o</span>
			<span class="letter">l</span>
			<span class="letter">a</span>
		</p>
	
		<p>
			The letter <span class="letter wrong alone">o</span> is part of the word, but, in other position.
		</p>
	
		<p>
			<span class="letter wrong">g</span>
			<span class="letter">r</span>
			<span class="letter wrong">i</span>
			<span class="letter">l</span>
			<span class="letter right">o</span>
		</p>
	
		<p>If the letter doesn't be green or yellow, it means that it doesn't be part of word.</p>
	
		<p>Have fun!</p>
		<button type="button" class="x_icon" on:click={toggleModal}>x</button>
	</section>
</section>

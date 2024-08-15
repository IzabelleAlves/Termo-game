<script lang="ts">
	import '../../styles/global.css';
	import '../../styles/about.css';
	import Footer from '../components/footer.svelte';

	let tituloDoJogo: string = 'TERMO';
</script>

<title>{tituloDoJogo}</title>

<header class="header">
	<nav class="navigationMenu">
		<h1 class="menu">TERMO</h1>
		<a class="menu" href="/">Home Page</a>
		<a class="menu" href="/play">Play</a>
	</nav>
</header>
<section class="game-instructions">
	<div class="font1">
	  <h3>How it works:</h3>
	  <br>
	  <p>
		Find the right word in 6 (six) tries. After each attempt,
		The tiles show how close you are to the solution.
	  </p>
	  <img class="about" src="/images/letraCorreta.png" alt="Exemple 1" />
	
	  <p> The letter <img class="about-icon" src="/images/letraCorretaUnica.png" alt="Exemplo 2" /> is part of the word and is in the correct position. </p>
	
	  <img class="about" src="/images/LetraPosicaoErrada.png" alt="Exemple 3" />
	
	  <p> The letter <img class="about-icon" src="/images/LetraPosicaoErradaUnica.png" alt="Exemplo 4" /> is part of the word, but, in other position. </p>
	
	  <img class="about" src="/images/palavraCompleta.png" alt="Exemple 5" />
	  <p>If the letter doesn't be green or yellow, it means that it doesn't be part of word.</p>
	  <br>
	  <p>Have fun!</p>
	
	</div>
	
  </section>

<section class="developers">
	<h3>Developers:</h3>
	<div class="developer-grid">
		<div class="developer">
			<img class="about" src="/images/Dylan.png" alt="Dylan Borges" />
			<p>Dylan Borges</p>
		</div>
		<div class="developer">
			<img class="about" src="/images/Izabelle.png" alt="Izabelle Alves" />
			<p>Izabelle Alves</p>
		</div>
		<div class="developer">
			<img class="about" src="/images/Keila.png" alt="Keila Isabelle" />
			<p>Keila Isabelle</p>
		</div>
		<div class="developer">
			<img class="about" src="/images/Maviael.png" alt="Maviael Melo" />
			<p>Maviael Melo</p>
		</div>
		<div class="developer">
			<img class="about" src="/images/Rubens.png" alt="Rubens Lira" />
			<p>Rubens Lira</p>
		</div>
	</div>
</section>

<section class="institution">
	<h3>Institution:</h3>
	<img class="about" src="/images/logoIFPE.png" alt="Logo IFPE" />
</section>

<Footer />

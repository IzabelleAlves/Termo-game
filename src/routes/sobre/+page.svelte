<script lang="ts">
	import '../../styles/global.css';
	import '../../styles/sobre.css';
	import Footer from '../components/footer.svelte';

	let tituloDoJogo: string = 'TERMO';
</script>

<title>{tituloDoJogo}</title>

<header class="header">
	<nav class="navigationMenu">
		<h1 class="menu">TERMO</h1>
		<a class="menu" href="/">Home Page</a>
		<a class="menu" href="/jogar">Play</a>
	</nav>
</header>
<!-- <section class="instrutions"> -->
<!-- <input type="checkbox" id="checkbox">
	<label for="checkbox"><h2>Ver intruções</h2></label> -->
<section class="game-instructions">
	<h3>Como funciona:</h3>

	<p>
		Descubra a palavra certa em 6 (seis) tentativas. Depois de cada tentativa, as peças mostram o
		quão perto você está da solução.
	</p>

	<p>
		<span class="letter right">T</span>
		<span class="letter">U</span>
		<span class="letter">R</span>
		<span class="letter">M</span>
		<span class="letter">A</span>
	</p>

	<p>
		A letra <span class="letter right alone">T</span> faz parte da palavra e está na posição correta.
	</p>

	<img class="about" src="/images/LetraPosicaoErrada.png" alt="Exemplo 3" />

	<p>
		A letra <img class="about-icon" src="/images/LetraPosicaoErradaUnica.png" alt="Exemplo 4" /> faz
		parte da palavra, porém, em outra posição.
	</p>

	<img class="about" src="/images/palavraCompleta.png" alt="Exemplo 5" />

	<p>Se a letra não ficar verde ou amarela, significa que ela não faz parte da palavra.</p>

	<p>Divirta-se!</p>
</section>
<!-- </section> -->

<section class="developers">
	<h3>Desenvolvedores:</h3>
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
	<h3>Instituição:</h3>
	<img class="about" src="/images/logoIFPE.png" alt="Logo IFPE" />
</section>

<Footer />

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
		<a class="menu" href="/about">About</a>
	</nav>
</header>

<section class="developers">
	
  <h3>Developers: </h3>
	<div class="developer-grid">
		<div class="developer">
			<img class="aboutUs" src="/images/Dylan.png" alt="Dylan Borges" />
			<p>Dylan Borges</p>
		</div>
		<div class="developer">
			<img class="aboutUs" src="/images/Izabelle.png" alt="Izabelle Alves" />
			<p>Izabelle Alves</p>
		</div>
		<div class="developer">
			<img class="aboutUs" src="/images/Keila.png" alt="Keila Isabelle" />
			<p>Keila Isabelle</p>
		</div>
		<div class="developer">
			<img class="aboutUs" src="/images/Maviael.png" alt="Maviael Melo" />
			<p>Maviael Melo</p>
		</div>
		<div class="developer">
			<img class="aboutUs" src="/images/Rubens.png" alt="Rubens Lira" />
			<p>Rubens Lira</p>
		</div>
	</div>
</section>

<div class="button">
	<a class="buttonUnique" href="/play">Play</a>
</div>

<section class="institution">
	<h3>Institution:</h3>
	<img class="aboutIf" src="/images/logoIFPE.png" alt="Logo IFPE" />
</section>

<Footer /> 

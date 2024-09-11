<script>
	import Footer from '../components/footer.svelte'
	import '../../styles/global.css';
	import "../../styles/about.css"
</script>

<header class="header">
	<h1 class="menu">TERMO</h1>
	<nav class="navigationMenu">
		<a class="menu" href="/">Home Page</a>
		<a class="menu" href="/play">Play</a>
		<a class="menu" href="/about">About</a>
	</nav>
</header>

<main>
	<section class="developers">
	
	  <h2>Developers:</h2>
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
	
	<section class="institution">
		<h3>Institution:</h3>
		<img class="aboutIf" src="/images/logoIFPE.png" alt="Logo IFPE" />
	</section>
</main>

<Footer /> 
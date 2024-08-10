<script lang="ts">
  import "../../styles/global.css"
  import Footer from "../components/footer.svelte";

  let tituloDoJogo: string = "TERMO"

</script>
<title>{tituloDoJogo}</title>

<header class="header">
  <h1>TERMO</h1>
  <nav class="navigationMenu">
      <a class="menu" href="/">Home Page</a>
      <a class="menu" href="/sobre">About</a>
  </nav>
</header>

<h1>About</h1>

<img class="sobre" src="/images/logoIFPE.png" alt="logo IPFE"/>

<p>
    Autor: Allan Diego Silva Lima
</p>
<p>
  <a href="allan.lima@igarassu.ifpe.edu.br">allan.lima@igarassu.ifpe.edu.br</a>
</p>

<a class="menu" href="/">Voltar ao Menu</a>

<Footer />
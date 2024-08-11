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
      <a class="menu" href="/jogar">Play</a>
  </nav>
</header>

<h1>About</h1>

<table>
  <tr>
    <th>
      <img class="sobre" src="/images/logoIFPE.png" alt="logo IPFE"  style="width: 20%; height: auto;"/>
    </th>
  </tr>
</table>

<br>

<table>
  <tr>
    <th><img class="sobre" src="/images/powerRosa.png" alt="01" style="width: 30%; height: auto;"/></th>
    <th><img class="sobre" src="/images/powerVermelho.png" alt="02" style="width: 30%; height: auto;"/></th>
    <th><img class="sobre" src="/images/powerAmarelo.png" alt="03" style="width: 30%; height: auto;"/></th>
  </tr>
  <tr>
    <th><p>Izabele</p></th>
    <th><p>Rubens Lira</p></th>
    <th><p>Keila Isabelle</p></th>

  </tr>
</table>

<table>
  <tr>
    <th><img class="sobre" src="/images/powerAzul.png" alt="04" style="width: 20%; height: auto;"/></th>
    <th><img class="sobre" src="/images/powerPreto.png" alt="05" style="width: 20%; height: auto;"/></th>
  </tr>
  <tr>
    <th><p>Dylan Borges</p></th>
    <th><p>Maviael Melo</p></th>

  </tr>
</table>

<br><br>

<p>
    Autor: Allan Diego Silva Lima
</p>
<p>
  <a href="allan.lima@igarassu.ifpe.edu.br">allan.lima@igarassu.ifpe.edu.br</a>
</p>

<a class="menu" href="/">Voltar ao Menu</a>

<Footer />
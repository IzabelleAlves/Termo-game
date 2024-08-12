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

<br><br>

<table>
  <tr>
    <th>
      <h3>Como funciona:</h3>
      <br><p>Descubra a palavra certa em 6 (seis) tentativas. Depois de cada 
      <br>tentativa,
      as peças mostram o quão perto você está da solução.</p>
      <br>
    <th>  
  </tr>
  <tr>
      <th>
        <img class="sobre" src="/images/Captura1.png" alt="t1"  style="width: 30%; height: auto;"/>
        
      </th> 
  </tr>
  <tr>
    <th>
      <br><p>A letra <img class="sobre" src="/images/Captura2.png" alt="t2"  style="width: 6%; height: auto;"/> faz parte da palavra e está na posição correta.</p>
      <br><br>
    <th>
  </tr>
  <tr>
    <th>
      <img class="sobre" src="/images/Captura3.png" alt="t3"  style="width: 30%; height: auto;"/>
    </th>
  </tr>
  <tr>
    <th>
      <br><p>A letra <img class="sobre" src="/images/Captura4.png" alt="t4"  style="width: 6%; height: auto;"/> faz parte da palavra, porém, em outra posição.</p>
      <br><br>
    </th>
  <tr>
  <tr>
    <th>
      <img class="sobre" src="/images/Captura5.png" alt="t5"  style="width: 30%; height: auto;"/>
    </th>
  </tr>
  <tr>
    <th>
      <br><br><p>Divirta-se!</p>
    </th>
  </tr>
</table>

<br><br><br><br>

<table>
  <tr>
    <th>
      <img class="sobre" src="/images/logoIFPE.png" alt="logo IPFE"  style="width: 15%; height: auto;"/>
    </th>
  </tr>
</table>

<br>

<table>
  <tr>
    <th><img class="sobre" src="/images/Izabelle.png" alt="01" style="width: 30%; height: auto;"/></th>
    <th><img class="sobre" src="/images/Rubens.png" alt="02" style="width: 30%; height: auto;"/></th>
    <th><img class="sobre" src="/images/Keila.png" alt="03" style="width: 30%; height: auto;"/></th>
  </tr>
  <tr>
    <th><p>Izabele</p></th>
    <th><p>Rubens Lira</p></th>
    <th><p>Keila Isabelle</p></th>

  </tr>
</table>

<table>
  <tr>
    <th><img class="sobre" src="/images/Dylan.png" alt="04" style="width: 20%; height: auto;"/></th>
    <th><img class="sobre" src="/images/Maviael.png" alt="05" style="width: 20%; height: auto;"/></th>
  </tr>
  <tr>
    <th><p>Dylan Borges</p></th>
    <th><p>Maviael Melo</p></th>

  </tr>
</table>

<br><br>

<!--
<p>
    Autor: Allan Diego Silva Lima
</p>
<p>
  <a href="allan.lima@igarassu.ifpe.edu.br">allan.lima@igarassu.ifpe.edu.br</a>
</p>

<a class="menu" href="/">Voltar ao Menu</a>

-->
<br><br><br><b></b>
<Footer />
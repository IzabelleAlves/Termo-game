<script lang="ts">
  import "../../styles/global.css"
  import Footer from "../components/footer.svelte";

  let tituloDoJogo: string = "TERMO"

</script>


<header> 
  <title>{tituloDoJogo}</title>
 
  
</header>

<div class="header">
  <h1>TERMO</h1>
  <nav class="navigationMenu">
      <a class="menu" href="/">Home Page</a>
      <a class="menu" href="/jogar">Play</a>
  </nav>
</div>

<section class="game-instructions">
  <div class="font1">
    <h3>Como funciona:</h3>
    <br>
    <p>
      Descubra a palavra certa em 6 (seis) tentativas. Depois de cada tentativa,
      as peças mostram o quão perto você está da solução.
    </p>
    <img class="sobre" src="/images/letraCorreta.png" alt="Exemplo 1" />
  
    <p> A letra <img class="sobre-icon" src="/images/letraCorretaUnica.png" alt="Exemplo 2" /> faz parte da palavra e está na posição correta. </p>
  
    <img class="sobre" src="/images/LetraPosicaoErrada.png" alt="Exemplo 3" />
  
    <p> A letra <img class="sobre-icon" src="/images/LetraPosicaoErradaUnica.png" alt="Exemplo 4" /> faz parte da palavra, porém, em outra posição. </p>
  
    <img class="sobre" src="/images/palavraCompleta.png" alt="Exemplo 5" />
    <p>Se a letra não ficar verde ou amarela, significa que ela não faz parte da palavra.</p>
    <br>
    <p>Divirta-se!</p>
  </div>
  
</section>

<section class="developers">
  <div class="font1">
    <h3 >Desenvolvedores:</h3>
    <div class="developer-grid">
     <div class="developer">
       <img class="sobre" src="/images/Dylan.png" alt="Dylan Borges" />
       <p >Dylan Borges</p>
     </div>
     <div class="developer">
       <img class="sobre" src="/images/Izabelle.png" alt="Izabelle Alves" />
       <p >Izabelle Alves</p>
     </div>
     <div class="developer">
       <img class="sobre" src="/images/Keila.png" alt="Keila Isabelle" />
       <p >Keila Isabelle</p>
     </div>
     <div class="developer">
       <img class="sobre" src="/images/Maviael.png" alt="Maviael Melo" />
       <p >Maviael Melo</p>
     </div>
     <div class="developer">
       <img class="sobre" src="/images/Rubens.png" alt="Rubens Lira" />
       <p >Rubens Lira</p>
     </div>
   </div>
  </div>
</section>

<section class="institution">
  <h3 class="font1">Instituição:</h3>
  <img class="sobre" src="/images/logoIFPE.png" alt="Logo IFPE" />
</section>

<Footer />
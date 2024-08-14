<script lang="ts">
    import "../../styles/global.css"
    import "../../styles/jogar.css"
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

<main id="game">
    <table class="tabelaJogo">
        <tr>
            <td class="cell characterWrongPosition">O</td>
            <td class="cell characterEmpty">D</td>
            <td class="cell characterEmpty">E</td>
            <td class="cell characterWrongPosition">I</td>
            <td class="cell characterEmpty">A</td>
        </tr>
        <tr>
            <td class="cell characterEmpty">C</td>
            <td class="cell characterWrongPosition">O</td>
            <td class="cell characterEmpty">U</td>
            <td class="cell characterEmpty">V</td>
            <td class="cell characterEmpty">E</td>
        </tr>
        <tr>
            <td class="cell characterWrongPosition">G</td>
            <td class="cell characterEmpty">R</td>
            <td class="cell characterWrongPosition">I</td>
            <td class="cell characterEmpty">L</td>
            <td class="cell characterCorrect">O</td>
        </tr>
        <tr>
            <td class="cell characterCorrect">P</td>
            <td class="cell characterCorrect">I</td>
            <td class="cell characterCorrect">N</td>
            <td class="cell characterCorrect">G</td>
            <td class="cell characterCorrect">O</td>
        </tr>
        <tr>
            <td class="cell"></td>
            <td class="cell"></td>
            <td class="cell"></td>
            <td class="cell"></td>
            <td class="cell"></td>
        </tr>
        <tr>
            <td class="cell"> </td>
            <td class="cell"> </td>
            <td class="cell"> </td>
            <td class="cell"> </td>
            <td class="cell"> </td>
        </tr>
    </table>
    
    <aside id="keyboard">
        <div class="row">
            <button class="key">Q</button>
            <button class="key">W</button>
            <button class="key">E</button>
            <button class="key">R</button>
            <button class="key">T</button>
            <button class="key">Y</button>
            <button class="key">U</button>
            <button class="key">I</button>
            <button class="key">O</button>
            <button class="key">P</button>
        </div>
        <div class="row">
            <button class="key">A</button>
            <button class="key">S</button>
            <button class="key">D</button>
            <button class="key">F</button>
            <button class="key">G</button>
            <button class="key">H</button>
            <button class="key">J</button>
            <button class="key">K</button>
            <button class="key">L</button>
            <button class="key special">Del</button>
        </div>
        <div class="row">
            <button class="key">Z</button>
            <button class="key">X</button>
            <button class="key">C</button>
            <button class="key">V</button>
            <button class="key">B</button>
            <button class="key">N</button>
            <button class="key">M</button>
            <button class="key special">Enter</button>
        </div>
    </aside>
</main>

<Footer />
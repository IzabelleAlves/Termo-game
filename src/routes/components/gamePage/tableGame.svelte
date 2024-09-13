<script lang="ts">
	// Lista de palavras para o jogo
	const palavras: string[][] = [
		['P', 'A', 'R', 'T', 'E'],
		['G', 'A', 'T', 'O', 'S'],
		['A', 'T', 'L', 'A', 'S'],
		['R', 'O', 'S', 'T', 'O'],
		['G', 'R', 'U', 'D', 'E']
	];
	let palavraAtual = palavras[Math.floor(Math.random() * palavras.length)]; // Escolhe uma palavra aleatória

	// Limite de tentativas
	const maxAttempts = 6;
	let attemptCount = 0;

	// Estado para armazenar os inputs e os resultados
	let inputs: string[] = Array(5).fill('');
	let rows: { letter: string; class: string }[][] = Array(maxAttempts)
		.fill([])
		.map(() => Array(5).fill({ letter: '', class: '' }));
	let wordGuessed = false; // Flag para verificar se a palavra foi acertada
	let gameOver = false;

	// Função para verificar a palavra e atualizar o estado
	function checkWord() {
		if (inputs.every((input) => input.length > 0)) {
			const result: { letter: string; class: string }[] = inputs.map((input, index) => {
				if (input === palavraAtual[index]) {
					return { letter: input, class: 'right' };
				} else if (palavraAtual.includes(input)) {
					return { letter: input, class: 'wrong' };
				} else {
					return { letter: input, class: 'empty' };
				}
			});

			// Adiciona a linha de resultados
			rows[attemptCount] = result;
			attemptCount++;
			wordGuessed = inputs.every((input, index) => input === palavraAtual[index]); // Verifica se a palavra foi acertada

			if (!wordGuessed && attemptCount >= maxAttempts) {
				gameOver = true;
			}

			// Limpa os inputs para a próxima linha
			inputs = Array(5).fill('');
		}
	}

	// Função para lidar com a entrada do usuário e mover o foco
	function handleInput(event: Event, index: number) {
		const input = event.target as HTMLInputElement;
		inputs[index] = input.value.toUpperCase();

		// Move o foco para o próximo input se o comprimento máximo for atingido
		if (input.value.length === input.maxLength && index < inputs.length - 1) {
			const nextInput = document.querySelectorAll<HTMLInputElement>('.cellInput')[index + 1];
			if (nextInput) nextInput.focus();
		}

		// Verifica se todos os inputs estão preenchidos, se o limite de tentativas não foi alcançado e se a palavra não foi acertada
		if (inputs.every((input) => input.length > 0) && attemptCount < maxAttempts && !wordGuessed) {
			checkWord();
		}
	}

	// Função para verificar se o limite de tentativas foi alcançado
	function isAttemptLimitReached() {
		return attemptCount >= maxAttempts || wordGuessed;
	}

	// Função para reiniciar o jogo com uma nova palavra
	function resetGame() {
		palavraAtual = palavras[Math.floor(Math.random() * palavras.length)];
		attemptCount = 0;
		inputs = Array(5).fill('');
		rows = Array(maxAttempts)
			.fill([])
			.map(() => Array(5).fill({ letter: '', class: '' }));
		wordGuessed = false;
		gameOver = false;
	}
</script>

<table class="tableGame">
	<!-- Linhas de resultados -->
	<tr>
		{#each inputs as input, index}
			<td class="cell">
				<input
					type="text"
					maxlength="1"
					class="cellInput"
					bind:value={inputs[index]}
					on:input={(event) => handleInput(event, index)}
					disabled={isAttemptLimitReached()}
				/>
			</td>
		{/each}
	</tr>
	{#each rows as row}
		<tr>
			{#each row as cell}
				<td class="cell {cell.class}">
					{cell.letter}
				</td>
			{/each}
		</tr>
	{/each}
</table>

{#if wordGuessed}
	<p class="congratsMessage">
		Parabéns, você acertou a palavra em {attemptCount} tentativa(s)!
		<button class="menu" on:click={resetGame}>Jogar novamente</button>
	</p>
{/if}

{#if gameOver}
	<p class="endGame">
		Que pena, você perdeu! A palavra era: {palavraAtual.join('')}
		<button class="menu" on:click={resetGame}>Tentar novamente</button>
	</p>
{/if}

<style>
	.menu {
		display: inline-block;
		width: 120px;
		text-align: center;
		background-color: #651142;
		text-decoration: none;
		color: #fff;
		border-radius: 1rem;
	}
</style>

<script lang="ts">
	// Palavra correta
	const nome: string[] = ['P', 'A', 'R', 'T', 'E'];

	// Limite de tentativas
	const maxAttempts = 6;
	let attemptCount = 0;

	// Estado para armazenar os inputs e os resultados
	let inputs: string[] = Array(5).fill('');
	// let rows: { letter: string; class: string }[][] = [];
	let rows: { letter: string; class: string }[][] = Array(maxAttempts)
		.fill([])
		.map(() => Array(5).fill({ letter: '', class: '' }));
	let wordGuessed = false; // Flag para verificar se a palavra foi acertada
	let gameOver = false;

	// Função para verificar a palavra e atualizar o estado
	function checkWord() {
		if (inputs.every((input) => input.length > 0)) {
			
			const result: { letter: string; class: string }[] = inputs.map((input, index) => {
				if (input === nome[index]) {
					return { letter: input, class: 'characterCorrect' };
				} else if (nome.includes(input)) {
					return { letter: input, class: 'characterWrongPosition' };
				} else {
					return { letter: input, class: 'characterEmpty' };
				}
			});


			// Adiciona a linha de resultados no início da lista

			rows[attemptCount] = result;
			attemptCount++;
			wordGuessed = inputs.every((input, index) => input === nome[index]); // Verifica se a palavra foi acertada

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
</script>

<table class="tableGame">
	<!-- Linha de inputs para a nova tentativa (no topo) -->
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
	<!-- Linhas de resultados -->
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
	<p class="congratsMessage">Parabéns, você acertou a palavra em {attemptCount} tentativa(s)!</p>
{/if}
{#if gameOver}
	<p class="endGame">Que pena, você perdeu! A palavra era: {nome.join('')}</p>
{/if} 
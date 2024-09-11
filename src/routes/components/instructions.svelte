<script lang="ts">
	export let modalClose: boolean = false;
	export let toggleModal: () => void;
</script>

<section class:close={modalClose} class="bg-intructions">
	<section class="game-instructions">
		<h3>How it works:</h3>
		<p>
			Find the right word in 6 (six) tries. After each attempt, The tiles show how close you are to
			the solution.
		</p>

		<p>
			<span class="letter right">t</span>
			<span class="letter">u</span>
			<span class="letter">r</span>
			<span class="letter">m</span>
			<span class="letter">a</span>
		</p>

		<p>
			The letter <span class="letter right alone">t</span> is part of the word and is in the correct
			position.
		</p>

		<p>
			<span class="letter">v</span>
			<span class="letter">i</span>
			<span class="letter wrong">o</span>
			<span class="letter">l</span>
			<span class="letter">a</span>
		</p>

		<p>
			The letter <span class="letter wrong alone">o</span> is part of the word, but, in other position.
		</p>

		<p>
			<span class="letter wrong">g</span>
			<span class="letter">r</span>
			<span class="letter wrong">i</span>
			<span class="letter">l</span>
			<span class="letter right">o</span>
		</p>

		<p>If the letter doesn't be green or yellow, it means that it doesn't be part of word.</p>

		<p>Have fun!</p>
		<button type="button" class="x_icon" on:click={toggleModal}>x</button>
	</section>
</section>

<style>
	.bg-intructions {
		position: absolute;
		top: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100dvw;
		height: 100dvh;
		overflow: hidden;
		background-color: rgba(var(--second-color-rgb), 0.6);
		transition: top 0.8s ease-in-out;
		overflow: hidden;
	}

	.close {
		top: -100%;
		transition: top 0.8s ease-in-out;
	}

	.game-instructions {
		position: relative;
		background-color: var(--light-color);
		border: 1px solid var(--dark-color);
		border-radius: 10px;
		padding: 20px;
		width: 600px;
		box-shadow: 0 2px 4px var(--dark-color);
		text-align: center;
		color: white;

		& h3 {
			margin-bottom: 1rem;
		}

		& p {
			align-content: center;
			margin: 16px;

			&:last-child {
				margin-bottom: 0;
			}
		}

	}

	.letter {
		display: inline-block;
		width: 50px;
		height: 50px;
		align-content: center;
		font-size: 2rem;
		font-weight: bold;
		text-transform: uppercase;
		border: 2px solid var(--dark-color);
		background-color: var(--second-color);
	}

	.right {
		background-color: var(--right);
	}

	.wrong {
		background-color: var(--wrong);
	}

	.alone {
		margin: 0 4px;
	}

	.x_icon {
		position: absolute;
		top: 0%;
		right: 0%;
		transform: translate(50%, -50%);
		display: block;
		height: 40px;
		width: 40px;
		align-content: center;
		background-color: var(--dark-color);
		border-radius: 50%;
		cursor: pointer;
		text-transform: uppercase;
		font-weight: bold;
		border: 2px solid #300820;
		color: white;
	}
</style>

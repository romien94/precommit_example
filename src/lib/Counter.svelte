<script>
	import { counter } from '../store';

	const incrementCounter = () => {
		counter.update((prev) => prev + 1);
	};

	const decrementCounter = () => {
		counter.update((prev) => prev - 1);
	};
</script>

<div class="counter">
	<button class="button indent-right" on:click={decrementCounter} aria-label="decrement_button">
		-
	</button>
	<p class="counter-value indent-right">{$counter}</p>
	<button class="button" on:click={incrementCounter} aria-label="inrecemnt_button">+</button>
</div>

<style lang="scss">
	.counter {
		display: flex;
		font-size: 20px;
		align-items: center;
	}

	.indent-right {
		margin-right: 5px;
	}

	.counter-value {
		color: red;
	}

	.button {
		background: #ccc;
		border: 1px solid transparent;
		border-radius: 2px;
		margin-right: 5px;

		&:last-child {
			margin-right: 0;
		}
	}
</style>

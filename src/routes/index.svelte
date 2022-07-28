<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Counter from '$lib/Counter.svelte';

	let unitTypes  = [
		{ id: 1, text: `meters` },
		{ id: 2, text: `feet` },
	];

	let unit: number;

	let poolWidth: number;
	let poolLenght: number;
	let poolDepth: number;

	let test: string;

</script>

<svelte:head>
	<title>Magic Solar Power</title>
	<meta name="description" content="The best free resource to learn how to build DIY solar pool heating" />
</svelte:head>

<section>
	<h1>
		Build your own solar pool heating
	</h1>

	<h3>
		The best <strong>free</strong> resource to learn how to build DIY solar pool heating.
	</h3>

	<h5>
		Magic Solar Pool will recommend what materials you should get and why, how much material you need and where you could get it. 
		The intention is to help people build solar pool heating the cheapest and the most efficient way possible. 
	</h5>

	<!-- <form class="content">
		<label for="">Units</label>
		<select value={unit}>
			{#each unitTypes as unit}
				<option value={unit.id}>
					{unit.text}
				</option>
			{/each}
		</select>
		<br/>
		<label for="">Nome</label>
		<input type="text" bind:value={test} />
	</form> -->
<h5>Pool Size</h5>
<div style="display: flex; 	align-items: center;">
	<div>
		<Counter title="Length" bind:count={poolLenght} />
	</div>
	<div>
		<Counter title="Width" bind:count={poolWidth}  />
	</div>
	<div>
		<Counter title="Depth" bind:count={poolDepth}  />
	</div>
</div>
<h2>{poolLenght * poolWidth * poolDepth * 1000} liters</h2>

</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	select {
		padding: 2px;
		font-size: 1rem;
	}

</style>

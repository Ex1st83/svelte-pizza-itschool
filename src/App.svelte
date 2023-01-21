<script>
	import Header from "./style/Header.svelte";
	import PizaCard from "./style/PizaCard.svelte";
</script>

<Header />
<PizaCard />
<section id="menu">
	<div class="container">
		{#each arrayPizza as pizza}
			<PizaCard {...pizza} />
		{/each}
	</div>
</section>

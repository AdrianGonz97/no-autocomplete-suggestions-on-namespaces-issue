<script lang="ts">
	import Button from "./CardButton.svelte";
	import Title from "./CardTitle.svelte";
	import Description from "./CardDescription.svelte";

	const Ch = {
		Title,
		Description,
		Button,
	};
</script>

<div class="card">
	<slot {Ch} />
</div>

<style>
	.card {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		width: 300px;
		background-color: #181818;
		color: #ffffff;
		margin: 0px auto;
		border-radius: 8px;
		padding: 2rem;
	}
</style>

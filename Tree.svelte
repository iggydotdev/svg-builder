<script>
	import Group from "./Group.svelte";
	import Item from "./Item.svelte";
	export let shouldExpand;
	export let data;
	let expand = false;

	const toggle = () => {
	  expand = !expand;
	};
</script>

<ul>
	{#if shouldExpand}
		{#each data.items as data}
			{#if !!data.items}
				<li>
					<button on:click={toggle}> <p>{data.name}</p></button>
					<Group bind:expand data={data}/>
				</li>
			{:else}
				<Item data={data}/>
			{/if}
		{/each}
	{/if}
</ul>

<style>
	/* 	ul {
			display: flex;
			flex-flow: column nowrap;
			align-items: flex-start;
			justify-content: center;
			
		}
		li { 
			display: flex;
			flex-flow: row nowrap;
			justify-content: flex-end;
			align-items: space-around;
		} */

	button {
	  margin-right: 16px;
	  /* 		border-radius: 100%; */
	  width: 100%;
	  height: 100%;
	  margin: 0;
	  padding: 0;
	  font-weight: bold;
	  color: white;
	  display: flex;
	  justify-content: center;
	  align-items: center;

	  background-color: royalblue;
	}
</style>
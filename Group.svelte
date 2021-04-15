<script>
	import Tree from "./Tree.svelte";
	export let data;
	export let expand;
</script>
	
<Tree shouldExpand={expand} data={data}/>
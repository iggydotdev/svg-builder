<script>
	import Tree from "./Tree.svelte";
	const data = {
	  name: "Root",
	  items: [
	    {
	      name: "01",
	      items: [
	        {
	          name: "02",
	          items: [
	            {
	              name: "03",
	              items: [
	                {
	                  name: "04"
	                },
	                {
	                  name: "05",
	                  items: [
	                    {
	                      name: "06"
	                    }
	                  ]
	                }
	              ]
	            },
	            {
	              name: "07"
	            }
	          ]
	        },
	        {
	          name: "08"
	        }
	      ]
	    },
	    {
	      name: "09"
	    }
	  ]
	};
</script>

<h1>Svg builder!</h1>
<button>+</button>
<aside>
	<Tree shouldExpand='true' data={data}/>
</aside>
<main>
	<!-- <SVGPlayGround /> -->
</main>

<style>
	aside {
	  width: auto;
	}
</style>
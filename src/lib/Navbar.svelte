<script>
	import {Navlinks, Navlist } from '$lib/index.js'
</script>

<nav>
<ul>
{#each Navlist as ni, index}

	<a href="google.com" >{ni}</a>
	
{/each}
</ul>
</nav>


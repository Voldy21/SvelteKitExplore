<script>
// @ts-nocheck

    /**
	 * @type {{ slug: any; }}
	 */
     export let data;
</script>

<h1>{data.slug}</h1>

<button on:click={handleClick}>Button</button>
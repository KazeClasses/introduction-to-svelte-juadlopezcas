<script>
    let {name} = $props()
    
    let count = $state(0);
    function handleClick() {
    count += 1;
    }
</script>

    {#if name === 'world'}
    <h1>Hello {name}!</h1>
    {:else}
    <h1>I don't say hello to anyone else</h1>
    {/if}

    <button onclick={handleClick}>
        Clicked {count} {count === 1 ? 'time' : 'times'}
    </button>

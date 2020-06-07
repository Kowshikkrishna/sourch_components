<script>
  export let caption;
  export let href;
  export let fn;
</script>


{#if href}
  <a {href}>{caption}</a>
{:else}
  <button on:click={fn}>{caption}</button>
{/if}


<style>
  button,
  a {
    font: 20px;
    border: 2px solid #000000;
    padding: 0.5rem 1rem;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.26);
    cursor: pointer;
    text-decoration: none;
    background: transparent;
    color: #000000;
    box-shadow: none;
  }

  button:hover,
  a:hover {
    background: #cecece;
    box-shadow: none;
  }
</style>
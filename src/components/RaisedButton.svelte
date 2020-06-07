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
    background: #000000;
    padding: 0.5rem 1rem;
    color: rgb(250, 245, 245);
    border-radius: 2px;
    box-shadow: 1px 1px 3px rgba(255, 255, 255, 0.26);
    cursor: pointer;
    text-decoration: none;
  }

  button:focus {
    outline: none;
  }

  button:hover,
  a:hover {
    background: #161616;
    border-color: #161616;
    box-shadow: 1px 1px 8px rgba(59, 59, 59, 0.26);
  }
</style>

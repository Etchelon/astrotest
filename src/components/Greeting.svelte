<script lang="ts">
  export let messages: string[];

  let index = 0;
  $: greeting = messages[index % messages.length];
  $: console.log({ greeting });
</script>

<div>
  <h3>{greeting}! Thank you for visiting!</h3>
  <button on:click={() => (++index)}> New Greeting </button>
</div>

<style>
  h3 {
    color: black;
  }
</style>

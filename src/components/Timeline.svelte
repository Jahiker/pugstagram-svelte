<script>
  import Card from "./Card.svelte";

  export let posts = [];
</script>

<div class="timeline">
  <div class="timeline__container">
    {#each posts as post}
      <Card {...post} />
    {:else}
      <h2>Loading...</h2>
    {/each}
  </div>
</div>

<style>
  .timeline {
    padding: 4em 0 0 0;
  }
</style>

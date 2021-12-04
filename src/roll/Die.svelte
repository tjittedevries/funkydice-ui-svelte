<script>
  export let rolls;
</script>

{#each rolls as roll}
  <div class="die tc mb1 mr1 pa2 dib br2 bg-light-gray black f5">{roll}</div>
{/each}

<style>
  .die {
    min-width: 40px;
  }
</style>

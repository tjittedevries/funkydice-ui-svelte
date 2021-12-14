<script>
  import { rolls } from "./stores";

  import Roll from "./Roll.svelte";
</script>

<div class="pa4 pr0 pt0 overflow-y-auto">
  <!-- rolls-container -->
  <h2 class="f6 b gray">rolls</h2>
  <div class="pr4">
    {#each $rolls as roll}
      <Roll {roll} />
    {/each}
  </div>
</div>

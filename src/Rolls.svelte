<script>
  import { rolls } from "./stores";

  import Roll from "./Roll.svelte";
</script>

<div class="h-100 pa4 pr0 pt0">
  <!-- rolls-container -->
  <h2 class="f6 b gray">rolls</h2>
  <div class="h-100 overflow-y-auto pr4">
    {#each $rolls as roll}
      <Roll {roll} />
    {/each}
  </div>
</div>

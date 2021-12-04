<script>
  export let roll;
  import Die from "./roll/Die.svelte";
  import Modifier from "./roll/Modifier.svelte";
  import Result from "./roll/Result.svelte";
</script>

<div class="pv2 bb b--moon-gray flex items-start">
  <Result value={roll.total} />
  <div class="flex items-center flex-wrap self-center">
    <Die rolls={roll.rolls} />
    {#if roll.modifier !== 0}
      <Modifier value={roll.modifier} />
    {/if}
  </div>
</div>

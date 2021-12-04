<script>
  import { rolls } from "./stores";

  function clearRolls() {
    rolls.set([]);
  }
</script>

<div id="bottom" class="bg-blue pv3 f4 tc">
  <button class="di ml2 bg-white black bn br3 pa2" on:click={clearRolls}
    >clear rolls</button
  >
</div>

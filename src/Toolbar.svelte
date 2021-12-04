<script>
  import { helpOpen } from "./stores";

  function handleHelp() {
    helpOpen.update(state => !state)
  }
</script>

<div class="shadow-1 bg-dark-pink pv3 ph4 flex items-center justify-between">
  <!-- <div class="material-icons f2 white">menu</div> -->
  <h1 class="f4 b white ma0 pa0">Funky Dice</h1>
  <button
    class="btn-toggle-overlay bn bg-transparent pa0 material-icons f2 white"
    on:click={handleHelp}
  >
    help
  </button>
</div>

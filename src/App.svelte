<script>
  import { funkydie } from 'funkydice'

  import Command from "./Command.svelte";
  import Overlay from "./Overlay.svelte";
  import Rolls from "./Rolls.svelte";
  import Toolbar from "./Toolbar.svelte";
  import Bottom from "./Bottom.svelte";

  import { rolls } from './stores'

  console.log("yolo", funkydie('1d6'))
  console.log("rolls", rolls)

</script>

<div
  class="sans-serif h-100 w-100 mw6-ns center flex flex-column justify-center"
>
  <div class="flex flex-column h-100 h-75-l">
    <div id="main" class="flex flex-column h-100 bg-white overflow-hidden">
      <Toolbar />
      <Command />
      <Rolls />
    </div>
  </div>
  <Bottom />
  
  <Overlay />
</div>

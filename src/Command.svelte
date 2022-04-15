<script>
  let command = "";
  import { rolls } from "./stores";
  import { funkydie } from "funkydice";

  function handleRoll(event) {
    event.preventDefault();
    const roll = funkydie(command);
    rolls.update((store) => [roll, ...store]);
  }
</script>

<div class="pa4">
  <h2 class="f6 b gray">type a command</h2>
  <form class="flex f4">
    <input
      bind:value={command}
      type="text"
      class="w-100 input-reset ba b--black pa3"
      placeholder="1d6, 1d66, 4df or 5d20+3"
      title="Enter your command, like 1d6, 1d66, 4df or 5d20+3"
    />
    <button
      class="ml2 bg-green white bn br3 pa2 material-icons f2"
      title="Roll the dice"
      on:click={handleRoll}
    >
      casino
    </button>
  </form>
</div>

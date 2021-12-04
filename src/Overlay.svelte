<script>
  import { helpOpen } from "./stores";

  console.log($helpOpen)

  function handleHelp() {
    helpOpen.update(state => !state)
  }
</script>

<div id="overlay" class="absolute absolute--fill bg-black-80" class:dn={!$helpOpen}>
  <div class="h-100 flex flex-column justify-center">
    <div class="w-80 center bg-white pa4">
      <div class="flex content-end items-end justify-end">
        <button class="btn-toggle-overlay bn bg-white pa0 material-icons f3 black" on:click={handleHelp}>close</button>
      </div>
      <div class="pr4" style="margin-top: -24px">
        <h2 class="f2">Help</h2>
        <p>
          Funky dice supports rolling dice in the follow format:
          <span class="gray">[amount]</span><span class="b">d</span><span
            class="gray">[faces]</span
          ><span class="gray">[modifier]</span>. An example would be 3d6+5, this
          would roll 3 d6 with a +5 modifier.
        </p>
        <p>
          It also supports a few special dice like the Fate dice (<span
            class="gray">[amount]</span
          ><span class="b">df</span><span class="gray">[modifier]</span>,
          results in a -4 to +4) and the d66 (<span class="gray">[amount]</span
          ><span class="b">d66</span><span class="gray">[modifier]</span>,
          results in two d6 combined, a 3 and a 4 will make a 34).
        </p>
        <p class="f5">
          Funky Dice UI & Funky Dice by
          <a href="https://tjittedevries.com" class="link blue underline"
            >Tjitte de Vries</a
          >, powered by
          <a
            href="https://www.npmjs.com/package/funkydice"
            class="link blue underline">funkydice</a
          >
          library and
          <a href="https://tachyons.io/" class="link blue underline"
            >tachyons css toolkit</a
          >.
        </p>
      </div>
    </div>
  </div>
</div>

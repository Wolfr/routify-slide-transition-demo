<script>
  import { isActive, url } from '@sveltech/routify';
  import { writable } from 'svelte/store';
  import Transition from "../../components/Transition.svelte"

  const width = writable();
</script>

<style>

  .relative-wrapper {
    height: 100%;
    display: flex;
    flex-direction: column;
  }

</style>

<div bind:offsetWidth={$width} class="relative-wrapper">
  <slot decorator={Transition} scoped={{ width }} />
</div>

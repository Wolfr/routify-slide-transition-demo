<script>
  import { scale, fly } from 'svelte/transition'
  import { BaseTransition } from "@sveltech/routify/decorators"

  export let scoped
  const { width } = scoped

  const configs = [
    {
      // New and old route are identical, do nothing
      condition: ({ routes }) => routes[0] === routes[1],
      transition: () => {},
    },
    {
      // This is the transition into a child
      condition: c => c.toDescendant,
      transition: fly,
      inParams: { x: $width, duration: 500, opacity: 1 },
      outParams: { x: -$width, duration: 500, opacity: 1 },
    },
    {
      // This is the transition back into the parent
      condition: c => c.toAncestor,
      transition: fly,
      inParams: { x: -$width, duration: 500, opacity: 1 },
      outParams: { x: $width, duration: 500, opacity: 1 },
    },
    {
      // No matching config. We don't want a transition
      condition: (c) => {
        console.log(c);
        return true
      },
      transition: (t) => {
        console.log(t);
      },
    },
  ]
</script>

<style>

  :global(.transition) {
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 100%;
  }

</style>

<BaseTransition {configs}>
  <slot />
</BaseTransition>

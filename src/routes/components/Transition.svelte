<script>
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";

  let show = false;

  onMount(() => (show = true));
</script>

{#if show}
  <div in:fade={{ delay: 400 }} out:fade={{ delay: 0, duration: 100 }}>
    <slot />
  </div>
{/if}

<style>
  div {
    position: relative;
  }
</style>

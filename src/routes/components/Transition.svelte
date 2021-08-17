<script>
  import { onMount } from "svelte";
  import { fly } from "svelte/transition";

  let show = false;

  onMount(() => (show = true));
</script>

{#if show}
  <div in:fly={{ x: 1000, delay: 450 }} out:fly={{ x: -1000 }}>
    <slot />
  </div>
{/if}

<style>
  div {
    position: relative;
  }
</style>

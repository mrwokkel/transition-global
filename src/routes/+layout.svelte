<script lang="ts">
  import type { Snippet } from 'svelte';
  import { fade } from 'svelte/transition';

  let show = $state(true)

  const { children } = $props<{
		children: Snippet<void>
	}>()


</script>

<div>
  <button onclick={() => show = !show}>
    Toggle
  </button>

  {#if show}
    <div transition:fade|global>HELLO</div>
  {/if}
</div>

{@render children()}


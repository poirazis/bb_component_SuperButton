<script>
  import Component from "../src/Component.svelte";

  // Capture all incoming props directly into a standard object
  let props = $props();
</script>

<!-- Using standard object distribution bypasses the broken $.rest_props engine -->
<Component {...props}>
  {@render props.children?.()}
</Component>

{#snippet failedFallback(error, reset)}
  <div class="plugin-error">Component failed to render: {error?.message}</div>
{/snippet}

<style>
  .plugin-error {
    color: var(--spectrum-global-color-red-500);
    font-size: 0.9em;
  }
  .plugin-error:empty {
    display: none;
  }
</style>

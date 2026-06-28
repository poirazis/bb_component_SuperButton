<script>
  import { getContext } from "svelte";
  import { SuperButton } from "@poirazis/superlib";

  let props = $props();

  const { styleable } = getContext("sdk");
  const component = getContext("component");

  let effectiveStyles = $derived({
    ...$component.styles,
    normal: {
      ...$component.styles?.normal,
      width: "fit-content",
    },
  });
</script>

<div use:styleable={effectiveStyles}>
  <SuperButton {...props} />
</div>

<style>
</style>

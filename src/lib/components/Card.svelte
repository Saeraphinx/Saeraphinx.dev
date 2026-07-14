<script lang="ts">
  import type { Snippet } from "svelte";
  import type { ClassValue, HTMLAttributes } from "svelte/elements";

  let { 
    children, 
    size = `fit`,
    class: className, 
    ...restProps 
  }: { 
    size?: `fit` | `big`
    class?: ClassValue; 
    children: Snippet 
  } & HTMLAttributes<HTMLDivElement> = $props();

  let sizeClasses : ClassValue = $derived.by(() => {
    switch (size) {
      default:
      case "fit":
        return ``;
      case "big":
        return `max-w-4xl m-5 rounded-2xl`;
    }
  })
</script>

<div {...restProps} class="{sizeClasses} p-4 text-center backdrop-blur-lg shadow-lg bg-black/50 {className}">
  {@render children()}
</div>

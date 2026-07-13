<script lang="ts">
  import type { Snippet } from "svelte";
  import type { ClassValue, HTMLAttributes } from "svelte/elements";

    let { children, class: className,  ...restProps } : { class?: ClassValue, children: Snippet } & HTMLAttributes<HTMLDivElement> = $props();
</script>

<div {...restProps} class="p-4 text-center max-w-4xl m-5 rounded-2xl backdrop-blur-lg shadow-lg bg-black/50 {className}">
   {@render children()}
</div>
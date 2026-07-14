<script lang="ts">
  import type { Snippet } from "svelte";
  import type { ClassValue, HTMLAnchorAttributes } from "svelte/elements";
  import { cn } from "../scripts/utils";

  let { 
    class: className,
    discrete = false,
    children,
    ...restProps
  } : { 
    class?: ClassValue,
    discrete?: boolean,
    children: Snippet,
  } & HTMLAnchorAttributes = $props();
</script>

<a {...restProps} class={cn(discrete ? `text-white` : `text-blue-300`, `transition-colors duration-300 hover:text-blue-400 no-underline`, className)}>
  {@render children()}
</a>


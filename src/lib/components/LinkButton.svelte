<script lang="ts">
  import type { ClassValue, HTMLAnchorAttributes } from "svelte/elements";
  import { cn } from "../scripts/utils";

  let { 
    class: className,
    iconUrl,
    text = "Website",
    ...restProps
  } : { 
    class?: ClassValue,
    iconUrl?: string,
    text?: string,
  } & HTMLAnchorAttributes = $props()
  
  function getDefaultIconUrl(url: string = ""): string {
    if (url.includes("github.com")) {
      return "images/github.svg";
    } else if (url.includes("discord")) {
      return "images/discord.svg";
    } else if (url.includes("youtube.com")) {
      return "images/youtube.svg";
    } else {
      return "images/web.svg";
    }
  }

  let altText = $derived.by(() => {
    if (iconUrl) {
      if (iconUrl === "images/web.svg") {
        return `Globe Icon`;
      } else {
        return `${text} Icon`;
      }
    } else {
      if (getDefaultIconUrl(restProps.href ?? '') === "images/web.svg") {
        return `Globe Icon`;
      } else {
        return `${text} Icon`;
      }
    }
  });
</script>

<a class={cn(`flex flex-row bg-black/20 rounded-xl items-center align-middle gap-2 px-2 py-1`, className)} {...restProps}>
  <img class="h-6 w-6 rounded-md" src={iconUrl && iconUrl.trim() !== "" ? iconUrl : getDefaultIconUrl(restProps.href ?? '')} alt={altText} />
  <p class="text-base">{text}</p>
</a>
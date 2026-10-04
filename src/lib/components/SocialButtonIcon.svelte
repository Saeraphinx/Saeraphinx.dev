<script lang="ts">
  let {
    name,
    url,
    iconUrl,
    color,
    size
  } : {
    name: string,
    url: string,
    iconUrl?: string,
    color: `#${string}`,
    size?: `h-8 w-8` | `h-6 w-6` | `h-4 w-4`
  } = $props()

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
        return `${name} Icon`;
      }
    } else {
      if (getDefaultIconUrl(url ?? '') === "images/web.svg") {
        return `Globe Icon`;
      } else {
        return `${name} Icon`;
      }
    }
  });

  let iconFilter = $derived.by(() => {
    if (url.includes("scoresaber")) {
      return `brightness-100 grayscale`;
    } else if (url.includes("cube.community")) {
      return `brightness-300 grayscale`;
    } else {
      return `brightness-0 invert grayscale`
    }
  });
</script>

<a class="flex flex-row items-center align-middle z-1 rounded-2xl shadow-none {iconFilter} opacity-50 hover:brightness-100 hover:invert-0 hover:grayscale-0 hover:opacity-100" href={url} target="_blank" rel="noopener noreferrer">
  <img class={size ?? "h-8 w-8"} src={iconUrl && iconUrl.trim() !== "" ? iconUrl : getDefaultIconUrl(url ?? '')} alt={altText} />
</a>
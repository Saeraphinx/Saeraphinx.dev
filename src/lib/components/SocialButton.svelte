<script lang="ts">
  let {
    name,
    url,
    iconUrl,
    color
  } : {
    name: string,
    url: string,
    iconUrl: string,
    color: `#${string}`,
  } = $props()
</script>

<div class="relative flex border-2 rounded-2xl" style="border-color: {color};">
  <div class="absolute top-0 left-0 min-h-full w-full h-full rounded-2xl border-transparent opacity-0 hover:opacity-100 transition-all duration-300"></div>
  <a class="flex flex-row items-center align-middle gap-2 px-4 py-2 z-1 rounded-2xl transition-all duration-300 hover:bg-black shadow-none hover:shadow-[0_0_10px_var(--glow-color)]" style="--glow-color: {color}" href={url} target="_blank" rel="noopener noreferrer">
    <img class="h-8 w-8" src={iconUrl} alt={`${name} Logo`} />
    <p class="text-lg">{name}</p>
  </a>
</div>

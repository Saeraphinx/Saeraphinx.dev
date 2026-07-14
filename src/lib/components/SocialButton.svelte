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

<div class="flex border-2 rounded-2xl" style="border-color: {color};">
  <a class="flex flex-row items-center align-middle gap-2 px-2 my-2 pr-4" href={url}>
    <img class="h-8 w-8" src={iconUrl} alt={`${name} Logo`} />
    <p class="text-lg">{name}</p>
  </a>
</div>

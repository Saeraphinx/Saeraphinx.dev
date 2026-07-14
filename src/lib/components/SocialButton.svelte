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

<div class="flex border border-[{color}] rounded-2xl">
  <a class="flex flex-row items-center align-middle gap-1 p-2" href={url}>
    <img class="h-4 w-4" src={iconUrl} alt={`${name} Logo`} />
    <p class="text-lg">{name}</p>
  </a>
</div>

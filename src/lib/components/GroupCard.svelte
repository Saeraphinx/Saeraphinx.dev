<script lang="ts">
  import Card from "./Card.svelte";
  import LinkButton from "./LinkButton.svelte";

  let { group } : { group: {
    name: string,
    description: string,
    iconUrl: string,
    timeframe?: string,
    roles?: string,
    links: {
      name?: string,
      url?: string,
      iconUrl?: string,
    }[]
  }} = $props();
</script>

<Card size="fit" class="flex flex-row not-sm:flex-col items-center justify-center gap-2 p-4">
  <img class="h-32 w-32 rounded-2xl" src={group.iconUrl} alt={`${group.name} Icon`} />
  <div class="flex flex-col justify-items-evenly max-w-sm gap-2">
    <div class="h-full">
      <h1 class="text-3xl font-bold">{group.name}</h1>
      <p class="text-base text-wrap text-white/80">{group.description}</p>
    </div>
    <div class="flex flex-col justify-center">
      <div class="flex flex-row flex-wrap gap-2 justify-center">
        {#each group.links as link}
          <LinkButton text={link.name} href={link.url} iconUrl={link.iconUrl} />
        {/each}
      </div>
      <p class="text-sm text-white/50">{group.timeframe} • {group.roles}</p>
    </div>
  </div>
</Card>
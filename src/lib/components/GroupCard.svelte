<script lang="ts">
  import Card from "./Card.svelte";
  import LinkButton from "./LinkButton.svelte";
  import SocialButtonIcon from "./SocialButtonIcon.svelte";

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

<Card size="fit" class="flex flex-row not-sm:flex-col items-center justify-center gap-4 p-4">
    <img class="h-24 w-24 rounded-2xl" src={group.iconUrl} alt={`${group.name} Icon`} />
    <div class="flex flex-col text-left justify-items-evenly max-w-sm gap-2">
      <div class="h-full">
        <div class="flex flex-row gap-2 justify-between">
          <h1 class="text-2xl font-bold">{group.name}</h1>
          <div class="flex flex-row gap-2">
            {#each group.links as link}
              <SocialButtonIcon iconUrl={link.iconUrl} name={link.name ?? `Website`} url={link.url!} color="#FFF" size="h-6 w-6" />
            {/each}
          </div>
        </div>
        <p class="text-base/snug text-wrap text-white/80">{group.description}</p>
        <p class="text-sm/snug text-white/50">{group.timeframe} • {group.roles}</p>
      </div>
      <!--  -->
    </div>
</Card>
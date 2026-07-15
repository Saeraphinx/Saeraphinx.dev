<script lang="ts">
  import Card from "./Card.svelte";
  import LinkButton from "./LinkButton.svelte";

  let {
    project,
  }: {
    project: {
      name: string;
      description: string;
      iconUrl?: string;
      timeframe?: string;
      roles?: string;
      links: {
        name?: string;
        url?: string;
        iconUrl?: string;
      }[];
    };
  } = $props();
</script>

<Card size="fit" class="flex flex-row not-sm:flex-col items-center justify-center gap-2 p-4">
  {#if project.iconUrl}
    <img class="h-24 w-24 rounded-2xl" src={project.iconUrl} alt={`${project.name} Icon`} />
  {/if}
  <div class="flex flex-col justify-items-evenly h-full gap-2 {project.iconUrl ? `max-w-md w-md not-sm:max-w-sm not-sm:w-auto` : `max-w-sm w-sm not-sm:max-w-xs not-sm:w-auto`}">
    <div class="h-full">
      <h1 class="text-3xl font-bold">{project.name}</h1>
      <p class="text-base/snug text-wrap text-white/80">{project.description}</p>
    </div>
    <div class="flex flex-col justify-center">
      <div class="flex flex-row gap-2 justify-center">
        {#each project.links as link}
          <LinkButton text={link.name} href={link.url} iconUrl={link.iconUrl} />
        {/each}
      </div>
      <p class="text-sm text-white/50">{project.timeframe}{project.roles && project.timeframe ? ` • ` : ``}{project.roles}</p>
    </div>
  </div>
</Card>
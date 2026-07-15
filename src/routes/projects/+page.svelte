<script lang="ts">
  import Card from "../../lib/components/Card.svelte";
  import ProjectCard from "../../lib/components/ProjectCard.svelte";
</script>

<div class="flex flex-col items-center justify-center gap-4">
  <Card>
    <h2 class="text-3xl">Recent & Notable Projects</h2>
  </Card>
  <div class="flex flex-row flex-wrap justify-center gap-4">
    <ProjectCard
      project={{
        name: "BadBeatMods",
        description: "Mod hosting platform in use by the Beat Saber Modding Group.",
        timeframe: "Released New Years 2025",
        links: [
          {
            name: "Website",
            url: "https://beatmods.com",
          },
          {
            name: "GitHub",
            url: "https://github.com/Saeraphinx/BadBeatMods",
          },
        ],
      }} />
    <ProjectCard
      project={{
        name: "The Beasties",
        description: "a.k.a. The BeastSaber Mapping Awards: A yearly mapping awards event hosted by BeastSaber.",
        timeframe: "Since 2023",
        roles: "Developer, Editor (2023-24)",
        //iconUrl: "images/beasties.png",
        links: [
          {
            name: "Awards Website",
            url: "https://bsaber.com/the-beastsaber-mapping-awards",
            iconUrl: "images/beasties.png",
          },
          {
            name: "Voting Form",
            url: "https://mappingawards.saeraphinx.dev/",
            iconUrl: "images/beasties.png",
          },
        ],
      }} />
    <ProjectCard
      project={{
        name: "Anti-Scam OCR",
        description: "Discord bot that uses optical character recognition to detect scams within images.",
        timeframe: "Since Early 2026",
        links: [
          {
            name: "GitHub",
            url: "https://github.com/Saeraphinx/anti-scam-ocr",
          },
        ],
      }} />
  </div>
  <Card class="mt-8">
    <h2 class="text-3xl">Other Projects</h2>
  </Card>
  <div class="flex flex-row flex-wrap justify-center gap-4">
    <ProjectCard
      project={{
        name: "Saeraphinx.dev",
        description: "This website!",
        timeframe: "Released August 2023, revamped July 2026.",
        links: [
          {
            name: "Website",
            url: "https://saeraphinx.dev",
            iconUrl: "images/favicon.ico",
          },
          {
            name: "GitHub",
            url: "https://github.com/Saeraphinx/Saeraphinx.dev",
          },
        ],
      }} />
    <ProjectCard
      project={{
        name: "Extra Sensory II",
        description: "Beat Saber's first ever live event. The sequel to the immensely popular Extra Sensory event. ",
        timeframe: "Released Janurary 2025",
        links: [
          {
            name: "Event Website",
            url: "https://exsii.totalbs.dev/",
          },
          {
            name: "Stream VOD",
            url: "https://www.youtube.com/watch?v=dt_OoYx-N6c",
          },
        ],
      }} />
    <ProjectCard
      project={{
        name: "CC 2023 Rewind",
        description: "One of the many editors behind the 2023 Cube Community Rewind video.",
        timeframe: "Released January 2024",
        links: [
          {
            name: "Video",
            url: "https://www.youtube.com/watch?v=bbwJkCF4xp0",
          },
        ],
      }} />

    <ProjectCard
      project={{
        name: "CustomMenuText",
        description: "Beat Saber mod that allows for custom text in the main menu.",
        timeframe: "First released in early 2024",
        roles: "Originally by artemiswkearney",
        links: [
          {
            name: "GitHub",
            url: "https://github.com/Saeraphinx/CustomMenuText",
          },
        ],
      }} />

    <ProjectCard
      project={{
        name: "NotOutYet",
        description: "Beat Saber mod that replaces all instances of your username with text of your choice.",
        timeframe: "Released Janurary 2024",
        links: [
          {
            name: "GitHub",
            url: "https://github.com/Saeraphinx/NotOutYet",
          },
        ],
      }} />
    <ProjectCard
      project={{
        name: "NewMapBot",
        description: "Discord bot that tracks new maps on BeatSaver and posts them to a Discord server.",
        timeframe: "Since late 2023",
        links: [],
      }} />
    <ProjectCard
      project={{
        name: "Ranking Overseer",
        description: "Discord bot made to help manage and oversee the ranking process for BeatLeader.",
        timeframe: "Released August 2023",
        links: [],
      }} />
    <ProjectCard
      project={{
        name: "NullSearchFix",
        description: "Beat Saber mod for 1.34.2 that fixes a base game crash when a song with no title is loaded.",
        timeframe: "Released December 2023",
        links: [
          {
            name: "GitHub",
            url: "https://github.com/Saeraphinx/NullSearchFix",
          },
        ],
      }} />
    <ProjectCard
      project={{
        name: "Luma",
        description: "A private Discord made originally as a replacement for MEE6, but now does much more.",
        timeframe: "Since late 2022",
        links: [
          {
            name: "TOS & Privacy",
            url: "https://saeraphinx.dev/projects/tos",
            iconUrl: "images/favicon.ico",
          }
        ],
      }} />
  </div>
</div>

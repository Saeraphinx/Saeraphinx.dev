<script>
  import Card from "../lib/components/Card.svelte";
  import GroupCard from "../lib/components/GroupCard.svelte";
  import Link from "../lib/components/Link.svelte";
  import ProjectCard from "../lib/components/ProjectCard.svelte";
  import SocialButton from "../lib/components/SocialButton.svelte";
</script>

<div class="flex flex-col items-center justify-center gap-8">
  <Card size="big" class="max-w-xl">
    <h1 class="text-4xl font-bold mb-2">Hi, I'm Saera.</h1>
    <p class="text-base">
        I'm a software developer & computer creature that creates and operates various services for online communities, primarially focusing on Beat Saber. 
    </p>
  </Card>
  <Card size="big" class="max-w-5xl">
    <h2 class="text-3xl font-bold mb-2">Links & Socials</h2>
    <div class="flex flex-row flex-wrap justify-evenly gap-3">
      <SocialButton name="GitHub" url="https://github.com/Saeraphinx" iconUrl="images/github.svg" color="#FFF" />
      <SocialButton name="BlueSky" url="https://bsky.app/profile/saeraphinx.dev" iconUrl="images/bluesky.svg" color="#0285FF" />
      <SocialButton name="Twitter" url="https://twitter.com/Saeraphinx" iconUrl="images/twitter.svg" color="#1DA1F2" />
      <SocialButton name="Twitch" url="https://twitch.tv/Saeraphinx" iconUrl="images/twitch.svg" color="#9146FF" />
      <SocialButton name="YouTube" url="https://www.youtube.com/@Saeraphinx" iconUrl="images/youtube.svg" color="#F00" />
      <SocialButton name="Discord" url="discord://discord.com/users/213074932458979330" iconUrl="images/discord.svg" color="#5865F2" />
    </div>
    <div class="flex flex-row flex-wrap justify-center gap-4 mt-4">
      <SocialButton name="BeatSaver" url="https://beatsaver.com/profile/4284987" iconUrl="images/bs.png" color="#FFF" />
      <SocialButton name="BeatLeader" url="https://beatleader.com/u/saeraphinx" iconUrl="images/bl.png" color="#E0F" />
      <SocialButton name="ScoreSaber" url="https://scoresaber.com/u/76561198323656813" iconUrl="images/ss.png" color="#FF0" />
    </div>
  </Card>
  <div class="flex flex-col items-center justify-center">
    <Card>
      <h2 class="text-3xl font-bold">Groups</h2>
    </Card>
    <div class="flex flex-row flex-wrap justify-center gap-4 mt-2">
      <GroupCard group={{
        name: "Beat Saber Modding Group",
        description: "The hub for all things modding Beat Saber, from how to mod the game to creating custom content!",
        iconUrl: "https://github.com/bsmg.png",
        timeframe: "Since 2024",
        roles: "Staff, Modder",
        links: [
          {
            name: "Website",
            url: "https://bsmg.wiki",
          },
          {
            name: "Discord",
            url: "https://discord.gg/beatsabermods",
          }
        ]
      }} />
      <GroupCard group={{
        name: "Cube Community",
        description: "A group that hosts tournaments and uploads videos of top plays, community highlights, and more!",
        iconUrl: "images/cc.png",
        timeframe: "Since 2021",
        roles: "Staff, Editor, (Former) Lead Editor",
        links: [
          {
            name: "YouTube",
            url: "https://www.youtube.com/c/CubeCommunity",
          },
          {
            name: "Discord",
            url: "https://discord.gg/dwe8mbC",
          }, 
          {
            name: "Website",
            url: "https://cube.community",
            iconUrl: "images/cc.png",
          }
        ]
      }} />
      <GroupCard group={{
        name: "Beat Saber World Cup",
        description: "A yearly country-based Beat Saber tournament featuring the very best players of each country.",
        iconUrl: "images/bswc-2024.png",
        timeframe: "Since 2024",
        roles: "Staff, Production",
        links: [
          {
            name: "Current Tournament",
            url: `https://cube.community/tournaments/bswc-${new Date(new Date().setDate(-130)).getFullYear()}`,
            iconUrl: "images/cc.png",
          },
          {
            name: "Discord",
            url: "https://discord.gg/Tu5zkZ9wsw",
          }
        ]
      }} />
    </div>
  </div>
  <div class="flex flex-col items-center justify-center">
    <Card>
      <h2 class="text-3xl font-bold">Recent Projects</h2>
    </Card>
    <div class="flex flex-row flex-wrap justify-center gap-4 mt-2">
      <ProjectCard project={{
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
          }
        ]
      }} />
      <ProjectCard project={{
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
          }
        ]
      }} />
      <ProjectCard project={{
        name: "Anti-Scam OCR",
        description: "Discord bot that uses optical character recognition to detect scams within images.",
        timeframe: "Early 2026",
        links: [
          {
            name: "GitHub",
            url: "https://github.com/Saeraphinx/anti-scam-ocr",
          }
        ]
      }} />
    </div>
  </div>
</div>

<!-- I'm a software developer & computer creature that creates and operates various services for the Beat Saber community and other communities.
      <br /><br />
      I am a staff member and former lead editor for <a href="https://www.youtube.com/c/CubeCommunity">Cube Community</a>, where we upload videos of top plays, community highlights, and more. As part of my time there, I managed the
      <a href="https://www.youtube.com/playlist?list=PLwx5EB8PdMNeuygkTEeowY-bXj5F-2SCU">Noodle Map Monday</a>
      series, where we showcase the fun and cool stuff the community has put together with Heck's suite of mods. If you want to play the maps yourself, you can find the link to each map in the video description, or you can find
      <a href="https://beatsaver.com/playlists/4197">a playlist with every map on BeatSaver</a>.
      <br /><br />
      I've also been involved with managing & developing for projects & events. I developed the voting form & judge's panel for the <Link discrete href="https://bsaber.com/the-beastsaber-mapping-awards">2025 BeastSaber Mapping Awards</Link>,
      hosted some matches for the <Link discrete href="https://cube.community/tournaments/bswc-2026">Beat Saber World Cup</Link>, and developed a backend that is in use by the
      <Link discrete href="https://bsmg.wiki">Beat Saber Modding Group</Link>
      for hosting Beat Saber mods. Links to these projects can be found below, or on the <a href="/projects">projects tab</a>.
      <br /><br />
      If you'd like to get in contact with me, please see my <a href="contact">contact page</a>. -->
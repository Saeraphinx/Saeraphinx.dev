<script>
  import Card from "$lib/components/Card.svelte";
  import GroupCard from "$lib/components/GroupCard.svelte";
  import Link from "$lib/components/Link.svelte";
  import ProjectCard from "$lib/components/ProjectCard.svelte";
  import SocialButtonIcon from "$lib/components/SocialButtonIcon.svelte";
  import pfp from "$lib/media/profile/feb-2025 iyumei.png";
  import pride from "$lib/media/profile/pride-flag.svg";

  const interests = [`programming`, `event production`, `video editing`, `linux`, `server hosting`, `systems integration`, `diy hardware`, `vr`, `3d printing`, `music`, `rhythm games`];
  const tools = [`obs`, `atem`, `photoshop`, `premiere`, `q-sys`, `audacity`, `bitfocus companion`, `proxmox`, `debian`, `docker`, `node.js`, `sveltekit`, `express`, `discord.js`, `arduino`];
</script>

<div class="flex flex-col items-center justify-center gap-4 m-auto">
  <!-- top bar -->
  <div class="flex flex-row items-center justify-between w-full gap-4 max-w-6xl not-sm:flex-col">
    <Card size="fit" class="flex flex-row justify-center items-center gap-4">
      <img class="h-16 w-16 rounded-full" src={pfp} alt="Saeraphinx" />
      <div class="flex-1 flex flex-col text-left">
        <p class="text-3xl font-bold">Saeraphinx</p>
        <div class="flex flex-row items-center gap-2">
          <img class="inline h-6 w-6" src={pride} alt="Pride" />
          <p class="text-base text-gray-500">she/her</p>
        </div>
      </div>
    </Card>
    <Card size="fit" class="flex flex-row flex-wrap justify-center h-fit gap-2">
      <SocialButtonIcon name="GitHub" url="https://github.com/Saeraphinx" iconUrl="images/github.svg" color="#FFF" />
      <SocialButtonIcon name="BlueSky" url="https://bsky.app/profile/saeraphinx.dev" iconUrl="images/bluesky.svg" color="#0285FF" />
      <SocialButtonIcon name="Twitter" url="https://twitter.com/Saeraphinx" iconUrl="images/twitter.svg" color="#1DA1F2" />
      <SocialButtonIcon name="Twitch" url="https://twitch.tv/Saeraphinx" iconUrl="images/twitch.svg" color="#9146FF" />
      <SocialButtonIcon name="YouTube" url="https://www.youtube.com/@Saeraphinx" iconUrl="images/youtube.svg" color="#F00" />
      <SocialButtonIcon name="Discord" url="discord://discord.com/users/213074932458979330" iconUrl="images/discord.svg" color="#5865F2" />
      <span></span>
      <SocialButtonIcon name="BeatSaver" url="https://beatsaver.com/profile/4284987" iconUrl="images/bs.png" color="#FFF" />
      <SocialButtonIcon name="BeatLeader" url="https://beatleader.com/u/saeraphinx" iconUrl="images/bl.png" color="#E0F" />
      <SocialButtonIcon name="ScoreSaber" url="https://scoresaber.com/u/76561198323656813" iconUrl="images/ss.png" color="#FF0" />
    </Card>
  </div>

  <Card size="big" class="flex flex-row max-w-2xl gap-3">
    <div class="flex flex-col justify-center items-center gap-4">
      <p class="text-base/snug">
          I'm a software developer & computer creature who has been creating media and operating services for various online communities for over {new Date().getFullYear() - 2018} years.
        </p>
        <p class="text-base">
          You can find some of my recent projects and groups I've been involved with below, or you can check out my <Link discrete href="/projects">projects tab</Link> for a more complete list of my public work.
      </p>
    </div>
  </Card>
  <div class="flex flex-row not-md:flex-col items-start not-md:items-center justify-center gap-4">
    <div class="flex flex-col flex-wrap justify-center gap-4">
      <Card>
        <h2 class="text-3xl font-bold">Interests & Tools</h2>
      </Card>
      <Card>
        <div class="flex flex-row flex-wrap justify-center gap-2 max-w-lg">
          {#each interests as interest}
            <p class="text-sm px-2 bg-blue-800 rounded">{interest}</p>
          {/each}
          {#each tools as tool}
            <p class="text-sm px-2 bg-purple-500/50 rounded">{tool}</p>
          {/each}
        </div>
      </Card>
      <Card>
        <h2 class="text-3xl font-bold">Communities</h2>
      </Card>
      <GroupCard group={{
        name: "Beat Saber Modding Group",
        description: "The hub for all things Beat Saber, from how to mod the game to creating custom content!",
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
        description: "A French non-profit association that creates videos and hosts events for the Beat Saber community.",
        iconUrl: "images/cc.png",
        timeframe: "Since 2021",
        roles: "Staff, Editor, (Former) Lead Editor",
        links: [
          {
            name: "Website",
            url: "https://cube.community",
            iconUrl: "images/cc.png",
          },
          {
            name: "YouTube",
            url: "https://www.youtube.com/c/CubeCommunity",
          },
          {
            name: "Discord",
            url: "https://discord.gg/dwe8mbC",
          }
        ]
      }} />
      <GroupCard group={{
        name: "Beat Saber World Cup",
        description: "A yearly country-based Beat Saber tournament hosted by Cube Community.",
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
    <div class="flex flex-col flex-wrap justify-center gap-4">
      <Card>
        <h2 class="text-3xl font-bold">Recent Projects</h2>
        <!-- <a href="/projects">See all projects</a> -->
      </Card>
      <ProjectCard project={{
        name: "BadBeatMods",
        description: "Mod hosting platform in use by the Beat Saber Modding Group.",
        timeframe: "Released New Years 2025",
        roles: "Developer",
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
        roles: "Developer",
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
<script lang="ts">
  import Card from "$lib/components/Card.svelte";
  import Link from "$lib/components/Link.svelte";
</script>

<div class="flex flex-col items-center justify-center">
  <Card size="big" class="flex flex-col gap-4">
    <h1 class="text-4xl font-bold">Contact</h1>
    <p>
      If you are looking to get into contact with me via direct messaging (such as Discord DMs), there are a few things to keep in mind. I keep my Discord somewhat locked down, so you will need to be in one of the servers I'm in in order to
      message me without a friend request. <b>I do not accept unsolicited friend requets from people I do not know.</b> I have DMs on in the
      <Link discrete href="https://discord.gg/beatsabermods" target="_blank">Beat Saber Modding Group discord server</Link>, <Link discrete href="https://discord.gg/dwe8mbC" target="_blank">Cube Community discord server</Link>, and in
      <Link discrete href="https://discord.gg/Tu5zkZ9wsw" target="_blank">Grazzy's discord server</Link>.
    </p>
    <p>
      Additionally, I tend not to reply to messages sent out of the blue that only start with "Hi" or "Hello", or "How are you". Since these are usually indications of scams, I will ignore them. See <Link href="https://nohello.net"
        >nohello.net</Link>
      and <Link href="https://dontasktoask.com">dontasktoask.com</Link> for more information as to why this is a bad practice in general.
    </p>
    <span>
      <p>Available methods of contact include:</p>
      <ul style="list-style-type: none;">
        <li>Discord: <Link href="discord://discord.com/users/213074932458979330">@saeraphinx</Link></li>
        <li>Bluesky: <Link href="https://bsky.app/profile/saeraphinx.dev" target="_blank">@saeraphinx.dev</Link></li>
        <li>Tumblr: <Link href="https://saeraphinx.tumblr.com/" target="_blank">@saeraphinx</Link></li>
        <li>Email: <Link href="mailto:contact@saeraphinx.dev">contact@saeraphinx.dev</Link></li>
      </ul>
      <p class="text-xs text-white/50">Other forms of contact may be available, but these are best for me.</p>
    </span>
    <p>
      I am most active on my Discord. All other methods of contact are checked less frequently. If you have a question about a project I'm working on, there is high chance that the project has a discord server that you can join to ask
      questions. Feel free to ping me in those servers if you have questions.
    </p>
  </Card>
</div>

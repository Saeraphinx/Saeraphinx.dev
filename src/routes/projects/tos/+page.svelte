<script>
  import Card from "../../../lib/components/Card.svelte";
  import Link from "../../../lib/components/Link.svelte";
</script>

<div class="flex flex-col items-center justify-center gap-4">
  <Card size="big" class="flex flex-col gap-4">
    <h1 class="text-3xl font-bold">Luma Terms of Service</h1>
    <p class="text-base">Luma does not have very many distict rules, as it is a private bot. However, there are some things that have the ability to get your ID banned from the bot. These include:</p>
    <ul class="self-center text-left list-disc list-inside text-base">
      <li>Abusing the bot in any way (e.g. spamming the FAQ reader)</li>
      <li>Attempting to exploit the bot</li>
      <li>Attempting to use the bot to break Discord's TOS</li>
      <li>Attempting to use the bot to break the server's rules</li>
    </ul>
    <p class="rext-base">
      The gist of the rules is: don't be a jerk, don't try to break things, and don't try to get around the rules/safeguards put in place. If you have any questions or concerns, you can contact me using the links on my homepage or at <Link
        href="discord://discord.com/users/213074932458979330">Saeraphinx</Link> on Discord. (Messages that look like scams and/or spam will be ignored. For tips on how to get a response, see <Link href="httos://nohello.net"
        >nohello.net</Link
      >.)
    </p>
  </Card>
  <Card size="big" class="flex flex-col gap-4">
    <h1 class="text-3xl font-bold">Luma Privacy Policy</h1>
    <p class="text-base">
      Luma only passively records data required for its operation, such as <b>user IDs, username, message IDs, and server IDs</b> within it's database for use with it's various modules. This data is not shared with any third parties, and is
      only used for the operation of the bot. This bot does has the ability to access message contents and server members. This is only used for moderation, and is not stored or logged within the Database. This data is stored indefinitely, but
      can be deleted upon request. This data is not used for any other purposes, and is not used to track users outside of the bot's operation.
    </p>
    <div class="flex flex-col">
      <p class="text-base">A breakdown of identifiable & non-passively recorded data, by database table, is stored as follows:</p>
      <ul class="self-center text-left list-disc list-inside text-base">
        <li>User ID (Levels, Birthdays, BoopBot, Starboard, GrazCoin)</li>
        <li>Guild ID (Levels, Birthdays, BoopBot, Starboard)</li>
        <li>Username (Levels, BoopBot)</li>
        <li>XP (Levels)</li>
        <li>Birthday (Birthdays)</li>
        <li>Command Executions (BoopBot)</li>
        <li>Message ID (Starboard)</li>
        <li>Author ID (Starboard)</li>
        <li>Channel ID (Starboard)</li>
        <li>Pinner ID (Starboard)</li>
      </ul>
    </div>
    <p class="text-base">
      The module that collects the most data is the Starboard module, which collects, message ID, author ID, channel ID, and pinner ID. This data is only used for the operation of the Starboard module. This data is stored indefinitely, but
      can be deleted upon request. This data is not used for any other purposes, and is not used to track users outside of the bot's operation.
    </p>
    <p class="text-base">
      In addition to identifiable data stored within the database, the bot also records statistics on its operation, such as the number of messages processed, the number of commands executed, and the number of events received. This data is
      visible through the bot's /status command. This data does not have any link to and users. This data is stored indefinitely. This data is not used for any other purposes, and is not used to track users outside of the bot's operation.
    </p>
    <p class="text-base">
      If you have any questions or concerns, you can contact me using the links on my homepage or at <Link href="discord://discord.com/users/213074932458979330" target="_blank">Saeraphinx</Link> on Discord. (Messages that look like scams and/or
      spam will be ignored. Please see the contact page for more info.)
    </p>
    <p class="text-base">
      If you would like to request a copy of the data stored on you, you can contact me using the same methods. If you would like to request the deletion of the data stored on you, you can contact me on Discord with the account you would
      like the data deleted from. If you are unable to contact me through Discord, you can contact me using one of the alternative links on my homepage. You must supply the Discord ID of the account you would like the data deleted from.
    </p>
  </Card>
</div>

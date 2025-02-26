<script lang="ts">
    import Badge from "../components/badge.svelte";
    import Center from "../components/center.svelte";
    import Status from "../components/status.svelte";
    import Social from "../components/social.svelte";
    import Space from "../components/space.svelte";
    import Time from "../components/time.svelte";
</script>

<svelte:head>
    <title>vercte.net</title>
    <meta name="author" content="Vercte" />
    <meta name="description" content="Hello Gamers. this is my website" />
    <meta name="keywords" content="personal, linkpage, linktree, vercte" />

    <meta name="theme-color" content="#008cff" />
    <meta name="color-scheme" content="only light" />
</svelte:head>

<main> 
    <header>
        <hgroup>
            <h1 id="my-name">vercte dot net</h1>
            <p id="pronunciation">rhymes with "birthday"</p>
        </hgroup>
    </header>

    <article>
        <p>
            Hey! I'm Vercte. I play Minecraft too much, along with rhythm games. I pixel
            art, and program in TypeScript, Lua, and Java too. 
        </p>
    
        <p>
            I like to make things. I make Minecraft Mods, Datapacks, and Resource Packs,
            Minecraft Player Models, Websites, ADOFAI charts, Pixel Arts,
            and Videos (very rarely)
        </p>
    </article>
    
    <article>
        <Center>
            <Status />
            <Time />
        </Center>
    
        <h2 style="margin-bottom: 0.3em">places where I am</h2>
    
        <Center direction="row">
            <Social name="vercte on Github" social="github" link="https://github.com/vercte" color="#111"/>
            <Social name="vercte on Modrinth" social="modrinth" link="https://modrinth.com/user/Vercte" color="#00af5c"/>
            <Social name="vercte on Discord" social="discord" link="https://discord.com/users/829853860289970236" color="#5865f2"/>
            <Social name="vercte.net on Bluesky" social="bluesky" link="https://bsky.app/profile/vercte.net" color="#1185fe"/>
            <Social name="lolecksdeehaha on Scratch" social="scratch" link="https://scratch.mit.edu/users/lolecksdeehaha" color="#f8aa36"/>
            <Social name="vercte on Youtube" social="youtube" link="https://youtube.com/@Vercte" color="#f00"/>
            <Social name="verctebutreal on Roblox" social="roblox" link="https://roblox.com/users/1756620403/profile" color="#191b1d"/>
        </Center>
    
        <Space amount="0.7em" />
    
        <h2 style="margin-bottom: 0.3em">some buttons and badges</h2>
        <Center direction="row" padding="0 2em">
            <Badge name="eighty eight thirty one (88x31)" badge="eeto.png" link="https://eightyeightthirty.one"/>
            <Badge name="chitin dot link" badge="chitinlink.gif" link="https://chitin.link"/>
            <Badge name="xan now!" badge="xanlol.png" link="https://xan.lol"/>
            <Badge name="dimden" badge="dimdendev.gif" link="https://dimden.dev"/>
            <Badge name="think with portals" badge="portal.png" link="https://www.thinkwithportals.com/" />
            <Badge name="forumoji now!" badge="forumojinow.gif" link="https://gh.vercte.net/forumoji" />
            <Badge name="best viewed with firefox" badge="firefox.png" />
        </Center>
    </article>
</main>
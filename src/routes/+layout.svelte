<script lang="ts">
  import "./layout.css";
  import { page } from "$app/state";
  import { onMount } from "svelte";
  import { prefersReducedMotion } from "svelte/motion";

  let { children } = $props();

  let subpages = [
    {
      label: "HOME",
      href: "/",
    },
    {
      label: "PROJECTS",
      href: "/projects",
    },
    {
      label: "CONTACT",
      href: "/contact",
    },
  ];

  onMount(() => {
    let introCover = document.getElementById("intro-cover")!;
    if (document.body.style.opacity === `0`) {
      window.scrollTo(0, 0);
      runIntro();
      document.body.style.opacity = `1`;
      setTimeout(() => {
        introCover.style.display = `none`;
      }, 4800);
    } else {
      introCover.style.display = `none`;
    }
  })

  function runIntro() {
    let introText = document.getElementById("introText")!; //assert that this exists
    introText.innerText = ``;
    let text = "SAERAPHINX";
    let elements = [];

    let beginningElement = document.createElement(`span`);
    beginningElement.innerText = `[`;

    for (let i = 0; i < text.length; i++) {
      let p = document.createElement(`span`);
      p.innerText = text[i];
      p.animate([{ opacity: 0 }, { opacity: 1 }], {
        duration: 250,
        easing: `ease-in-out`,
        delay: i * 100 + 1500,
        fill: `both`,
      });
      p.style.opacity = `0`;
      elements.push(p);
    }

    let endElement = document.createElement(`span`);
    endElement.innerText = `]`;

    let blinkKeyframes = [{ opacity: 0 }, { opacity: 1 }, { opacity: 1 }, { opacity: 0 }, { opacity: 0 }, { opacity: 1 }, { opacity: 1 }, { opacity: 0 }, { opacity: 0 }, { opacity: 0 }, { opacity: 1 }, { opacity: 1 }];
    let blinkOptions = {
      duration: 1800,
      easing: `ease`,
      delay: 0,
      iterations: 1,
    };
    beginningElement.animate(blinkKeyframes, blinkOptions);
    endElement.animate(blinkKeyframes, blinkOptions);
    /*beginningElement.animate([
        {  },
        { color: `#FFFFFF00` }
    ], {
        duration: 1000,
        easing: `ease-in-out`,
        delay: 2800,
        fill: `both`
    });
    endElement.animate([
        {  },
        { color: `#FFFFFF00` }
    ], {
        duration: 1000,
        easing: `ease-in-out`,
        delay: 2800,
        fill: `both`
    });*/
    introText.animate([{ fontSize: window.innerWidth < 500 ? `48px` : `64px`, paddingTop: `45vh` }, {}], {
      duration: 750,
      easing: `ease-in-out`,
      delay: 2800,
      fill: `both`,
    });

    introText.appendChild(beginningElement);
    introText.append(...elements);
    introText.appendChild(endElement);

    let refBar = document.getElementById("refBar")!; //assert that this exists
    let fadeKeyframes = [{ backgroundColor: `#000` }, { backgroundColor: `initial` }];
    let fadeOptions = {
      duration: 1000,
      easing: `ease-in-out`,
      delay: 3000,
      fill: `both`,
    } as const;
    introText.animate(fadeKeyframes, fadeOptions);
    refBar.animate(fadeKeyframes, fadeOptions);
    //refBar.style.backgroundColor = `rgba(0, 0, 0, 1)`;

    for (let child of refBar.children) {
      child.animate([{ opacity: 0 }, { opacity: 1 }], {
        duration: 2000,
        easing: `ease-in-out`,
        delay: 2800,
        fill: `both`,
      });
    }

    let mainContent = document.getElementById("intro-cover")!;
    mainContent.animate([{ opacity: 1 }, { opacity: 0, display: "none" }], {
      duration: 2000,
      easing: `ease-in-out`,
      delay: 2800,
      fill: `both`,
    });

    document.body.animate([{overflow: `hidden`}, {overflow: `initial`}], { 
      duration: 10,
      delay: 4000,
      fill: `both`
    });
  }
</script>

<svelte:head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Saeraphinx</title>
  <!-- General -->
  <meta name="description" content="Hi, I'm Saera. I write software, edit videos, run productions and more." />
  <!-- Discord -->
  <meta content="Saeraphinx" property="og:title" />
  <meta content="Hi, I'm Saera. I write software, edit videos, run productions and more." property="og:description" />
  <meta content="https://saeraphinx.dev" property="og:url" />
  <!-- <meta content="https://embed.com/embedimage.png" property="og:image" /> -->
  <meta content="#ff25af" data-react-helmet="true" name="theme-color" />

  <link rel="icon" href="/images/favicon.ico" type="image/x-icon" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
  <link href="https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet" />
</svelte:head>

<div class="sticky top-[-55px] z-10 h-full bg-[url('/images/bannerbg.png')] bg-cover bg-center bg-no-repeat text-white" id="header">
  <div class="bg-[linear-gradient(to_right,rgba(0,0,0,0),rgba(0,0,0,0.3),rgba(0,0,0,0.8),rgba(0,0,0,0.8),rgba(0,0,0,0.3),rgba(0,0,0,0))]" id="headerContent">
    <div class="text-center">
      <span>
        <p class="text-4xl p-3 font-extralight text-white drop-shadow-[0_0_8px_#000000]" id="introText">[SAERAPHINX]</p>
        <!--<script src="scripts/intro.js"></script>!-->
      </span>
    </div>
    <div class="text-center text-white" id="refBar">
      <div>
        {#each subpages as subpage}
          <a
            href={subpage.href}
            class="backdrop-blur-sm bg-black/50 p-1.5 m-1.5 rounded-sm no-underline text-base font-light {page.url.pathname === subpage.href ? `text-teal-400` : ``} hover:text-teal-500"
            aria-current={page.url.pathname === subpage.href}>{subpage.label}</a>
        {/each}
      </div>
      <div class="mt-2 h-0.5 bg-[linear-gradient(to_left,violet,rgb(137,18,223),rgb(0,162,255),green,yellow,orange,red)]"></div>
    </div>
  </div>
</div>

<div class="relative flex flex-col items-center justify-start overflow-x-hidden" id="content">
  <div class="fixed -top-12.5 -z-10 block h-[130vh] w-[130vw] opacity-100 blur-md">
    {#if prefersReducedMotion.current}
      <img loading="lazy" class="h-full w-full max-w-none object-cover opacity-50" src="/images/bannerbg.png" alt="Screenshot of Saeraphinx's map Tokyo Machine - FLY with all of the map's custom visual effects on" />
    {:else}
      <img loading="lazy" class="h-full w-full max-w-none object-cover opacity-50" src="/images/bg2.webp" alt="Looping Beat Saber gameplay for Saeraphinx's map of Lil Revive & Josh A - Darkness" />
    {/if}
  </div>
  <div class="w-full px-4 py-8">
    <span id="intro-cover" class="absolute top-0 left-0 h-full w-full z-100 bg-black opacity-0 overflow-hidden pointer-events-none"></span>
    {@render children()}
  </div>
</div>

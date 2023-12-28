<script>
  import "../styles/globals.scss";
  import { MetaTags } from 'svelte-meta-tags'
</script>

<head>
  <title>Ethan Yim</title>
  <MetaTags
    title="Ethan Yim"
    description="Crappy website"
    canonical="https://ethany.im"
    openGraph={{
      url: 'https://ethany.im',
      title: 'Ethan Yim',
      description: 'Transit enthusiast & hobbyist web developer.',
      images: [
        {
          url: 'https://ethany.im/og-screenshot.png',
          width: 1280,
          height: 720,
          alt: 'homepage screenshot',
        },
      ],
      site_name: 'Ethan Yim',
    }}
  />
</head>
<main>
  <nav>
    <div class="nav-left">
      <a href="https://status.ethany.im">Status</a>
      <a href="https://github.com/literaiiy">
        <img src="/images/github-mark.svg" alt="GitHub logo">
      </a>
    </div>
    <div class="nav-right">
      <a class="nav-contact" href="mailto:contact@ethany.im">Contact me!</a>
    </div>
  </nav>
  <section class="hero">
    <div class="focus">
      <a class="logo" href="/">
        <span class="first">
          ethan
        </span>
        <span class="last">
          yim
        </span>
      </a>
      <span class='tagline'>Transit enthusiast <b>&</b> hobbyist web developer</span>
    </div>
    <div class="scroll-indicator">
      <span>scroll...</span>
      <span>▼</span>
    </div>
  </section>
  <slot></slot>
</main>
<footer>
  <span>© {new Date().getFullYear()} Ethan Yim.</span>
  <span>
    quinta v2.0.0 built with <a class="styled-a" href="https://kit.svelte.dev">SvelteKit</a> and powered by <a href="https://vercel.com" class="styled-a">Vercel</a>. Heavily inspired by <a href="https://www.jay-clark.co.uk/" class="styled-a">Jay Clark's</a> website.
  </span>
</footer>

<!-- //// -->

<style lang="scss">
  $main-color: #292F36;
  $near-white: #f3f3f3;

  // Mobile
  @media screen and (max-width: 600px) {
    main {
      width: 100%;
      box-sizing: border-box;
    }

    main > a {
      width: 100%;
    }

    .logo {
      flex-direction: column;
    }
  }

  main {
    min-height: 100vh;
    width: 100%;
  }

  nav {
    width: 100%;
    position: fixed;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 1rem;
    // height: 3rem;
    box-sizing: border-box;
    & > .nav-left {
      // font-style: italic;
      font-weight: 600;
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 1rem;
      & img {
        width: 2rem;
        height: 2rem;
      }
    }
    & > .nav-right {
      // margin-left: auto;
      & > a.nav-contact {
        background-color: $main-color;
        color: $near-white;
        border-radius: .75rem;
        padding: .75rem 1rem;
      }
    }
    & > a {
      text-decoration: none;
      color: inherit;
      font-weight: 600;
    }
  }

  section.hero {
    // padding: 1rem 0;
    // gap: 1rem;
    height: 100vh;
  }
  
  .focus {
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .links {
    text-align: center;
    font-weight: 600;
  }

  .logo {
    font-size: 6rem;
    text-decoration: none;
    display: flex;
    flex-wrap: wrap;
    line-height: 3.5rem;
    justify-content: center;
    text-align: center;
    padding-bottom: 2rem;
    gap: 1rem;
    & > .first {
      font-family: "Nagbuloe-SB";
      letter-spacing: -.2rem;
    }
    & > .last {
      font-family: "Nagbuloe";
      filter: drop-shadow(0.25rem 0.25rem 0 #C8D5B9);
    }
  }

  .tagline {
    font-family: "Castoro";
    font-style: italic;
    font-size: 1.5rem;
    font-weight: 400;
    text-align: center;
  }
  
  .scroll-indicator {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    line-height: 1.5rem;
    font-style: italic;
    position: absolute;
    bottom: 15%;
    left: 50%;
    transform: translateX(-50%);
    font-size: 1.25rem;
  }

  .styled-a {
    color: inherit;
    text-decoration: none;
    font-style: italic;
  }

  footer {
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 1rem 0;
    gap: 0.25rem;
    // background-color: rgba(0, 0, 0, 0.15);
    & > span {
      text-align: center;
    }
  }

</style>
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
      description: 'Crappy website',
      images: [
        {
          url: 'https://ethany.im/favicon.png',
          width: 512,
          height: 512,
          alt: 'Ethan Yim logo',
        },
      ],
      site_name: 'Ethan Yim',
    }}
  />
</head>
<main>
  <nav class="header">
    <a class="logo" href="/">
      <span class='ethan'>ETHAN</span>
      <span class='yim'>YIM</span>
    </a>
    <span class='tagline'>Freeway enthusiast, Bay Area native, & professional React hater</span>
  </nav>
  <slot></slot>
</main>
<footer>
  <div class="links">
    <a href="https://status.ethany.im">
      <span>Status</span>
    </a>
    <span>·</span>
    <a href="mailto:contact@ethany.im">
      <span>Contact</span>
    </a>
    <span>·</span>
    <a href="https://github.com/literaiiy">
      <span>GitHub</span>
    </a>
    <span>·</span>
    <a href="https://cara.literaiiy.me">
      <span>v4</span>
    </a>
    <span>·</span>
    <a href="https://v3.literaiiy.me">
      <span>v3</span>
    </a>
  </div>
  <span>© {new Date().getFullYear()} Ethan Yim. Built with SvelteKit and powered by Vercel.</span>
</footer>

<!-- //// -->

<style lang="scss">

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

    .tagline {
      // font-size: min(1rem, 7.5vw) !important;
    }
  }

main {
  flex: 1;
  margin: auto;
  max-width: min(90vw, 80rem);
}

.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1rem 0;
  gap: 1rem;
}

.links {
  text-align: center;
  font-weight: 500;
}

.logo {
  font-size: min(12rem, 16vw);
  text-transform: uppercase;
  text-decoration: none;
  font-style: italic;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  text-align: center;
}

.tagline {
  font-family: "Shidorton";
  font-size: min(2rem, 3.5vw);
  font-weight: 400;
  text-align: center;
}

.ethan {
  font-family: "Pleatures OL";
  line-height: min(10rem, 15vw);
}

.yim {
  font-family: "Pleatures";
  line-height: min(10rem, 15vw);
}

footer {
  width: 100%;
  display: flex;
  flex-direction: column;
  padding: 1rem 0;
  gap: 0.25rem;
  & > span {
    text-align: center;
  }
}

</style>
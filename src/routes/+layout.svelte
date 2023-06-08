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
      padding: 1rem;
    }

    main > a {
      width: 100%;
    }

    .logo {
      flex-direction: column;
      & > span {
        font-size: min(8rem, 15vw);
        line-height: 5rem;
      }
    }
  }

main {
  flex: 1;
}

.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  gap: 1rem;
}

.links {
  /* font-family: system-ui, sans-serif; */
  // font-size: 1.5rem;
  text-align: center;
  font-weight: 500;
}

.logo {
  font-size: min(12rem, 15vw);
  text-transform: uppercase;
  text-decoration: none;
  /* font-weight: 600; */
  font-style: italic;
  display: flex;
  /* flex-direction: column; */
  flex-wrap: wrap;
  justify-content: center;
  text-align: center;
  /* -webkit-text-stroke: 0.1875rem black; */
  /* text-shadow: 0.25rem 0.25rem black; */
}

.tagline {
  font-family: "Shidorton";
  font-size: 2rem;
  font-weight: 400;
  text-align: center;
}

.ethan {
  font-family: "Pleatures OL";
  line-height: 10rem;
  /* color: #d2f8ff; */
}

.yim {
  font-family: "Pleatures";
  line-height: 10rem;
  /* margin-bottom: 5rem; */
  /* color: rgb(255, 221, 111); */
}

.logo .dot {
  color: gray !important;
}

.lastName {
  display: flex;
  flex-direction: row;
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
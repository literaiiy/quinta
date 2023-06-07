<script>
  import "../styles/globals.scss";
  import { MetaTags } from 'svelte-meta-tags'
</script>

<head>
  <title>Ethan Yim</title>
  <MetaTags
    title="Ethan Yim"
    titleTemplate="%s | Ethan Yim"
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
    <span class='tagline'>Freeway enthusiast & developer of mediocrity</span>
    <div class="links">
      <a href="https://status.ethany.im">
        <span>Status</span>
      </a>
      <span>/</span>
      <a href="mailto:contact@ethany.im">
        <span>Contact</span>
      </a>
      <span>/</span>
      <a href="https://github.com/literaiiy">
        <span>GitHub</span>
      </a>
    </div>
  </nav>
  <slot></slot>
</main>
<footer>
  <span>Copyright {new Date().getFullYear()} Ethan Yim.</span>
</footer>

<!-- //// -->

<style>
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
  font-size: 1.5rem;
}

.logo {
  font-size: 12rem;
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
  font-size: 2rem;
  font-weight: 600;
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
  & > span {
    text-align: center;
    font-size: 1.5rem;
  }
}

</style>
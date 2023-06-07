<script>
  import "../styles/globals.scss"
</script>

<head>
  <title>Ethan Yim</title>
</head>
<nav class="header">
  <a class="logo" href="/">
    <span class='ethan'>ETHAN</span>
    <span class='yim'>YIM</span>
  </a>
  <span class='tagline'>Web development if it sucked</span>
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

<style>
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
  flex-direction: column;
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

</style>

<slot></slot>
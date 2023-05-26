<script>
  import "../styles/globals.scss"
</script>

<head>
  <title>Ethan Yim</title>
</head>
<nav class="header">
  <a class="logo" href="/">
    <span>Ethan Y</span>
    <span class="dot">.</span>
    <span>im</span>
  </a>
  <div class="links">
    <a href="https://status.ethany.im">
      <span>Status</span>
    </a>
    <span>|</span>
    <a href="mailto:contact@ethany.im">
      <span>Contact</span>
    </a>
    <span>|</span>
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
}

.links {
  font-family: system-ui, sans-serif;
}

.logo {
  font-size: 5rem;
  text-transform: lowercase;
  text-decoration: none;
  color: black;
  font-weight: 600;
  font-style: italic;
  display: flex;
  flex-direction: row;
}

.logo .dot {
  color: gray !important;
}
</style>

<slot></slot>
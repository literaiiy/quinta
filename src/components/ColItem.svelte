<script lang='ts'>
  export let id: string;
  export let name: string;
  export let desc: string;
  export let url: string;
</script>

<a class="item" href={url}>
  <div class="text">
    <h2 class="name">{name}</h2>
    <span class="desc">{desc}</span>
  </div>
  <object
    class="icon"
    data={`/images/${id}.svg`}
    title={name}
  >
</a>

<style>
  .item {
    /* width:100%; */
    display: flex;
    flex: 1 20rem;
    flex-direction: row;
    justify-content: space-between;
    background-color: rgba(0,0,0,0.04);
    padding: 1rem;
    height: 15rem;
  }

  .name {
    font-size: 1.5rem;
    font-weight: 400;
    font-family: "Shidorton";
  }

  .icon {
    max-width: 16rem;
    & svg {
      stroke-width: 1px;
      fill: red;
    }
  }

</style>
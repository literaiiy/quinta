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

<style lang='scss'>
  .item {
    /* width:100%; */
    display: flex;
    flex: 1 20rem;
    flex-direction: row;
    justify-content: space-between;
    background-color: rgba(0,0,0,0.04);
    padding: 1rem;
    min-height: 15rem;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .name {
    font-size: 2rem;
    line-height: 3rem;
    font-weight: 400;
    margin: 0;
    font-family: "Youth Action";
  }
  
  .text {
    text-break: break-word;
    flex: 1 1 10rem;
  }
  
  .icon {
    z-index: -1;
    flex: 1 2 10rem;
    margin: auto;
    flex-shrink: 1;
    max-width: 16rem;
    max-height: 15rem;
    min-width: 0;
    filter: invert(18%) sepia(30%) saturate(1145%) hue-rotate(145deg) brightness(93%) contrast(99%);
  }


</style>
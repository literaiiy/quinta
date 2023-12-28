<script lang='ts'>
  export let id: string;
  export let name: string;
  export let desc: string;
  export let url: string;
</script>

<a class="item" href={url}>
  <!-- <div class="text"> -->
    <h2 class="name">{name}</h2>
    <!-- </div> -->
    <object
      class="icon"
      data={`/images/${id}.svg`}
      title={name}
    />
    <span class="desc">{desc}</span>
</a>

<style lang='scss'>
  $main-color: #292F36;
  $accent-color: #C8D5B9;
  $accent-color-50: rgba(200, 213, 185, 0.5);
  $near-white: #f3f3f3;

  .item {
    /* width:100%; */
    display: flex;
    flex: 1 20rem;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: $near-white;
    box-shadow: 0.5rem 0.5rem 0rem $accent-color-50;
    border: 4px solid $main-color;
    padding: 1rem;
    min-height: 15rem;
    flex-wrap: wrap;
    gap: 1rem;
    transition: 0.5s ease-in-out;
  }
  .item:hover {
    background-color: $accent-color;
    box-shadow: 0.75rem 0.75rem 0rem $main-color;
  }

  .name {
    font-size: 2rem;
    line-height: 2rem;
    padding: 0.5rem 0;
    font-weight: 400;
    margin: 0;
    // font-family: "Youth Action";
  }
  
  .text {
    text-break: break-word;
    flex: 1 1 10rem;
  }
  
  .icon {
    z-index: 41;
    flex: 1 2 10rem;
    margin: auto;
    flex-shrink: 1;
    max-width: 16rem;
    max-height: 10rem;
    min-width: 0;
    filter: invert(18%) sepia(30%) saturate(1145%) hue-rotate(145deg) brightness(93%) contrast(99%);
  }


</style>
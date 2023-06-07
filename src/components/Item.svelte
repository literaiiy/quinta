<script lang='ts'>
  export let id: string;
  export let name: string;
  export let desc: string;
  export let url: string;
  export let imageUrl: string;
</script>

<a 
  href={url}
  style={`background-image: 
            linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
            url('${imageUrl}')
        `}
>
  <span class="name">{name}</span>
  <span class="desc">{desc}</span>
  <img
    src={`/images/${id}.svg`}
    alt={name}
    draggable={false}
  >
</a>

<style lang='scss'>
  a {
    position: relative;
    /* border: 1px solid black; */
    border-radius: 0.125rem;
    height: 16rem;
    width: 16rem;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background-size: cover;
    box-shadow: 0 0 0.5rem #073642ab;
  }
  
  .name {
    position: absolute;
    width: 100%;
    height: 100%;
    padding: 0.5rem;
    /* background-color: #7c4343; */
    border-radius: 0.125rem;
    color: white;
    font-weight: bold;
    font-size: 3rem;
    text-shadow: 0 0 0.5rem #073642;
    text-align: center;
    margin-top: 1rem;
  }
  
  .desc {
    display: flex;
    transition: 0.35s ease-in-out;
    width: 100%;
    height: 100%;
    opacity: 0;
    background-color: rgba(0, 0, 0, 0.5);
    box-sizing: border-box;
    padding: 1rem;
    color: white;
    font-size: 1.5rem;
    position: absolute;
    align-items: end;
    z-index: 500;
    &:hover {
      opacity: 1;
    }
  }
  
  img {
    max-height: calc(100% - 0rem);
    max-width: 100%;
    margin-top: 4rem;
    color: red;
    filter: invert(98%) sepia(1%) saturate(312%) hue-rotate(53deg) brightness(118%) contrast(90%);
    &:hover {
      filter: invert(98%) sepia(1%) saturate(312%) hue-rotate(53deg) brightness(200%) contrast(90%) blur(0.125rem);
    }
  }
</style>
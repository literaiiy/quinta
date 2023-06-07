<script lang='ts'>
  export let id: string;
  export let name: string;
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
    background-color: #7c4343;
    border-radius: 0.125rem;
    height: 18rem;
    width: 18rem;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background-size: cover;

  }

  .name {
    transition: 0.35s ease-in-out;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    padding: 0.5rem;
    /* background-color: #7c4343; */
    border-radius: 0.125rem;
    color: white;
    font-weight: bold;
    font-size: 3cqw;
    text-shadow: 0 0 0.5rem black;
    opacity: 0;
    &:hover {
      opacity: 1;
    }
    z-index: 500;
  }
  
  img {
    transition: 0.25s ease-in-out;
    max-height: 100%;
    max-width: 100%;
    filter: invert(98%) sepia(1%) saturate(312%) hue-rotate(53deg) brightness(118%) contrast(90%);
    &:hover {
      /* transform: scale(2); */
      filter: invert(98%) sepia(1%) saturate(312%) hue-rotate(53deg) brightness(200%) contrast(90%) blur(0.125rem);
    }
  }
</style>
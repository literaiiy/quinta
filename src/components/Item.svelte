<script lang='ts'>
  export let id: string;
  export let name: string;
  export let url: string;

  // const decidePos = (id: string): string => {
  //   let style = {};

  //   if (id === 'campanula') {
  //     return "top: 0; right: 0;"
  //   }

  // }
</script>

<a href={url}>
  <img
    src={`/images/${id}.svg`}
    alt={name}
    draggable={false}
  >
</a>

<style>
  img {
    /* height: auto; */
    transition: 0.25s ease-in-out;
    &:hover {
      /* transform: scale(2); */
      filter: blur(0.25rem);
    }
  }
</style>
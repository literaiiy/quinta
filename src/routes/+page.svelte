<script lang='ts'>
  import Item from '../components/Item.svelte'

  // Each "item" on the shelf
  // 0: id, 1: name, 2: url
  const items: string[][] = [
    ['campanula', 'Campanula', 'https://campanula.literaiiy.me'],
    ['passiflora', 'Passiflora', 'https://passiflora.literaiiy.me'],
    ['dahlia', 'dah.li/a', 'https://dah.li/a'],
    ['ibahm', 'IBAHM', 'https://ibahm.org'],
    ['tiramisu', 'tiramisu', 'https://tiramisu.vip'],
    ['toolbox', 'literaiiy Toolbox', 'https://toolbox.literaiiy.me'],
    ['yieldbread', 'YieldBread', 'https://yieldbread.com'],
  ]
</script>

<main>
  {#each items as [id, name, url]}
    <Item id={id} name={name} url={url} />
  {/each}
</main>

<style lang='scss'>
  main {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    padding: 1rem;
    // @for $i from 1 through 7 {
    //   img:nth-child(#{$i}) {
    //     top: random(1000) + px;
    //     left: random(1000) + px;
    //   }
    // }
  }

</style>
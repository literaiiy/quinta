<script lang='ts'>
  import Item from '../components/Item.svelte'

  // Each "item" on the shelf
  // 0: id, 1: name, 2: url, 3: imageUrl
  // TODO: save images locally
  const items: string[][] = [
    ['campanula', 'Campanula', 'https://campanula.literaiiy.me', 'https://images.unsplash.com/photo-1470621178165-f1fb40c4401f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80'],
    ['passiflora', 'Passiflora', 'https://passiflora.literaiiy.me', 'https://images.unsplash.com/photo-1648605052635-07df296ece6b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=735&q=80'],
    ['dahlia', 'dah.li/a', 'https://dah.li/a', 'https://plus.unsplash.com/premium_photo-1672336396196-4bddb597a379?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80'],
    ['ibahm', 'IBAHM', 'https://ibahm.org', 'https://live.staticflickr.com/8472/8098468925_e2ecd56065_b.jpg'],
    ['tiramisu', 'tiramisu', 'https://tiramisu.vip', 'https://i.ibb.co/JtSvgvk/2020-07-09-12-04-02-2021-02-07-02-44-48-UTC.png'],
    ['toolbox', 'literaiiy Toolbox', 'https://toolbox.literaiiy.me', 'https://images.unsplash.com/photo-1618403005656-a1a4d8fec365?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=627&q=80'],
    ['yieldbread', 'YieldBread', 'https://yieldbread.com', 'https://images.unsplash.com/photo-1491975474562-1f4e30bc9468?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80'],
  ]
</script>

<main>
  {#each items as [id, name, url, imageUrl]}
    <Item id={id} name={name} url={url} imageUrl={imageUrl}/>
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
    gap: 1rem;
  }

</style>
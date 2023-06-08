<script lang='ts'>
  import Item from '../components/Item.svelte'
  import ColItem from '../components/ColItem.svelte';

  interface IItem {
    id: string;
    name: string;
    desc: string;
    url: string;
    imageUrl: string;
  }

  // TODO: save images locally
  const items: IItem[] = [
    {
      id: "campanula",
      name: "Campanula",
      desc: "Customizable & sleek pomodoro timer",
      url: "https://campanula.literaiiy.me",
      imageUrl: "https://images.unsplash.com/photo-1470621178165-f1fb40c4401f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80"
    },
    {
      id: "passiflora",
      name: "Passiflora",
      desc: "Customizable schedule creation web app",
      url: "https://passiflora.literaiiy.me",
      imageUrl: "https://images.unsplash.com/photo-1648605052635-07df296ece6b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=735&q=80",
    },
    {
      id: "dahlia",
      name: "dah.li/a",
      desc: "My rarely-contributed-to personal blog",
      url: "https://dah.li/a",
      imageUrl: "https://plus.unsplash.com/premium_photo-1672336396196-4bddb597a379?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80"
    },
    {
      id: "ibahm",
      name: "IBAHM",
      desc: "A free resource for SF Bay Area highways, exits, and locations",
      url: "https://ibahm.org",
      imageUrl: "https://live.staticflickr.com/8472/8098468925_e2ecd56065_b.jpg"
    },
    {
      id: "tiramisu",
      name: "tiramisu",
      desc: "Old Hypixel player stats site",
      url: "https://tiramisu.vip",
      imageUrl: "https://i.ibb.co/JtSvgvk/2020-07-09-12-04-02-2021-02-07-02-44-48-UTC.png" 
    },
    {
      id: "toolbox",
      name: "literaiiy Toolbox",
      desc: "Crusty old web tools",
      url: "https://toolbox.literaiiy.me",
      imageUrl: "https://images.unsplash.com/photo-1618403005656-a1a4d8fec365?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=627&q=80"
    },
    {
      id: "yieldbread",
      name: "YieldBread",
      desc: "Student blog about online moneymaking",
      url: "https://yieldbread.com",
      imageUrl: "https://images.unsplash.com/photo-1491975474562-1f4e30bc9468?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80"
    }
  ]
</script>

<div class='container'>
  {#each items as i}
    <ColItem id={i.id} name={i.name} url={i.url} desc={i.desc} imageUrl={i.imageUrl}/>
  {/each}
</div>

<style lang='scss'>
  .container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: stretch;
    justify-content: center;
    padding: 1rem;
    gap: 1rem;
  }

</style>
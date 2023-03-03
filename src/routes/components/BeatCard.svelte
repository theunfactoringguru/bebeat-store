<script>
  export let artistName = '4tydev';
  export let beatPlaylistName = '8 bit Sound Elements';
  export let beatList = ['Laser Tag', 'Battle Music', 'Intro Music'];

  export let setArtistName = true;

  const handleEvent = () => {
    console.log('clicked');
  }
</script>

<button on:click={handleEvent}>
  {#if setArtistName}
    <h2>{ artistName }</h2>
  {/if}
  <h3>{ beatPlaylistName }</h3>
  <ol>
    {#each beatList as beat}
      <li>{beat}</li>
    {/each}
  </ol>
</button>

<style>
  button {
    border: 1px solid black;
    box-shadow: -5px 5px 3px black;
    margin-left: 10rem;
    margin-right: 5rem;
    padding-right: 20px;
    padding-left: 20px;
    width: fit-content;
    background-color: #e1e6e4;
    color: darkslateblue;
    font-size: medium;
  }

  button:hover {
    cursor: pointer;
  }
</style>
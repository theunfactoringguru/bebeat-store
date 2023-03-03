<script>
  import BeatCard from "./components/BeatCard.svelte";
  import BeatUploadModal from "./components/BeatUploadModal.svelte";

  let user = {
    artistName: 'John Doe',
    email: 'johndoe@exampl.com',
    password: 'password123',
    beats: [
      {name: "Video-game beats", beatNames: ["Name 1", "Name 2", "Name 3"]},
      {name: "Rap beats", beatNames: ["Name 1", "Name 2","Name 3"]},
    ]
  }

  let showBeatsUploadModal = false;
  let songAmount = 0;
</script>

<div class="parent">
  <img src="profile.jpg" width="8%" alt="Profile Image"/>
  <div>
    <h3>{user.artistName}</h3>
    <button on:click={() => showBeatsUploadModal = true}>+ New Beat</button>
    {#each user.beats as beat}
      <BeatCard
        artistName={user.artistName}
        beatPlaylistName={beat.name}
        beatList={beat.beatNames}
        setArtistName={false}
      />
    {/each}
  </div>

  <BeatUploadModal bind:showBeatsUploadModal>
    <h2 slot="header">Upload Beats</h2>
    <div class="info-form">
      <form>
        <input type="text" placeholder="Beat Playlist Name"/>
        <br>
        <input type="number" placeholder="Song Quantity" bind:value={songAmount}/>
        <br>
        {#each Array(songAmount) as _, i}
          <input type="text" placeholder="Song name..."/>
        {/each}
      </form>
    </div>
  </BeatUploadModal>
</div>

<style>
  .parent {
    margin-top: 5rem;
    padding-left: 10rem;
    padding-right: 10rem;
  }

  img {
    border-radius: 10px;
  }

  div > button {
    width: fit-content;
    padding: 30px 10px;
    font-family: 'Ubuntu', 'Courier New', Courier, monospace;
    color: aliceblue;
    background-color: darkblue;
  }
</style>
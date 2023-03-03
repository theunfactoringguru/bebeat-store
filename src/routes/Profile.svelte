<script>
  import BeatCard from "./components/BeatCard.svelte";

  let user = {
    artistName: 'John Doe',
    email: 'johndoe@exampl.com',
    password: 'password123',
    beats: [
      {name: "Video-game beats", beatNames: ["Name 1", "Name 2", "Name 3"]},
      {name: "Rap beats", beatNames: ["Name 1", "Name 2","Name 3"]},
    ]
  }
</script>

<img src="profile.jpg" width="8%" alt="Profile Image">
<div>
  <h3>{user.artistName}</h3>
  {#each user.beats as beat}
    <BeatCard
      artistName={user.artistName}
      beatPlaylistName={beat.name}
      beatList={beat.beatNames}
      setArtistName={false}
    />
  {/each}
</div>

<style>
  * {
    padding-left: 10rem;
    padding-right: 10rem;
  }
</style>
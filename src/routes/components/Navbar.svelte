<script>
  import LogInModal from "./LogInModal.svelte";
  import SignUpModal from "./SignUpModal.svelte";

  let showLoginModal = false;
  let showSignupModal = false;
</script>
<nav>
  <div class="navbar">
    <h2>Bebeat Store</h2>
    <form>
      <input type="text" placeholder="Search for artist or kit name..." />
      <input type="submit" value="Search" />
    </form>
    <div class="action-buttons">
      <button on:click={() => {showSignupModal = true}}>
        Sign Up
      </button>
      <span> | </span>
      <button on:click={() => {showLoginModal = true}}>
        Log In
      </button>
      <span> | </span>
      <button>
        Cart
      </button>
    </div>
  </div>
</nav>

<LogInModal bind:showLoginModal>
  <h2 slot="header">Log In</h2>
  <div class="info-form">
    <form>
      <input type="text" placeholder="E-mail"/>
      <br>
      <input type="password" placeholder="Password"/>
      <br>
      <input type="submit" value="Log In"/>
    </form>
  </div>
</LogInModal>

<SignUpModal bind:showSignupModal>
  <h2 slot="header">Sign Up</h2>
  <div class="info-form">
    <form>
      <input type="text" placeholder="E-mail"/>
      <br>
      <input type="text" placeholder="Artistic Name"/>
      <br>
      <input type="password" placeholder="Password"/>
      <br>
      <input type="submit" value="Sign Up"/>
    </form>
  </div>
</SignUpModal>

<style>
  * {
    padding: 0;
    margin: 0;
  }
  .navbar {
    margin: 0;
    display: flex;
    justify-content: space-between;
    background-color: darkblue;
    padding: 1.5rem 10rem;
  }

  .navbar > form input[type="text"] {
    width: 400px;
    line-height: 0;
  }

  .navbar > form input {
    height: 40px;
    width: 100px;
  }
  form {
    align-self: center;
  }

  .account-buttons {
    align-self: center;
  }

  .navbar > h2 {
    color: white;
  }

  [slot="header"] {
    color: black;
  }

  nav{
    margin: 0;
    padding: 0;
  }
  
  .action-buttons > button{
    background-color: transparent;
    border: 0;
    font-size: 1em;
    color: aliceblue;
  }
  
  .action-buttons > button:hover {
    cursor: pointer;
  }

  .info-form > form > input{
    margin-bottom: 10px;
    width: 200px;
    height: 30px;
  }
</style>
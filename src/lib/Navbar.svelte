<nav>
  <h2>Bebeat Store</h2>
  <form>
    <input type="text" placeholder="Search for artist or kit name..." />
    <input type="submit" value="Search" />
  </form>
  <div class="account-buttons">    
    <button>Sign Up</button>
    <button>Log In</button>
  </div>
</nav>

<style>
  * {
    padding: 0;
    margin: 0;
  }
  nav {
    display: flex;
    justify-content: space-between;
    background-color: darkblue;
    padding: 2rem;
  }

  form {
    align-self: center;
  }

  .account-buttons {
    align-self: center;
  }

  h2 {
    color: white;
  }
</style>
<nav>
  <div class="navbar">
    <h2>Bebeat Store</h2>
    <form>
      <input type="text" placeholder="Search for artist or kit name..." />
      <input type="submit" value="Search" />
    </form>
    <div class="account-buttons">    
      <a href="/">Sign Up</a>
      <span> | </span>
      <a href="/">Log In</a>
    </div>
  </div>
</nav>

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
    padding: 1.5rem;
    padding-left: 10rem;
    padding-right: 10rem;
  }

  div > form input[type="text"] {
    width: 400px;
    line-height: 0;
  }

  div > form input {
    height: 40px;
    width: 100px;
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

  nav{
    margin: 0;
    padding: 0;
  }
  a {
    color: aliceblue;
  }
</style>
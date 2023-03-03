<script>
  import Navbar from "./routes/Navbar.svelte";
  import {Route, Router} from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import Profile from "./routes/Profile.svelte";
</script>


<Router>
  <Navbar/>
  <Route path="/"><Home/></Route>
  <Route path="profile"><Profile/></Route>
</Router>
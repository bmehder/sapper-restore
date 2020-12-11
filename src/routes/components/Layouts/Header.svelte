<script>
  import { createEventDispatcher } from "svelte";
  import Logo from "../UI/Logo.svelte";
  export let sticky = false;
  export let uppercase = false;
  export let background = "darkorange";
  export let color = "white";
  export let linkColor = "white";

  const dispatch = createEventDispatcher();
</script>

<header class:sticky style="background:{background};color:{color};">
  <nav>
    <Logo
      logo="<img style='width:100%;' src='/logo-restore-medical-group.jpg' />"
      width="150px" />
    <ul class:uppercase>
      <li><a style="color:{linkColor};" href="/">Home</a></li>
      <li>
        <a style="color:{linkColor};" href="case-studies">Case Studies</a>
      </li>
      <li><a style="color:{linkColor};" href="contact">Contact</a></li>
    </ul>
  </nav>
</header>

<style>
  header {
    /* width: 100%; */
    padding: 1em;
    background: darkorange;
    color: white;
    text-align: center;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.25);
  }
  .sticky {
    position: fixed;
    z-index: 100;
  }
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 960px;
    margin: 0 auto;
  }
  nav ul {
    display: flex;
    justify-content: space-between;
  }
  nav ul li {
    list-style-type: none;
    padding: 0 1rem;
    font-weight: 600;
  }
  nav ul li:last-child {
    padding-right: 0;
  }
  nav ul li a {
    height: auto;
    color: #f3f3f3;
    text-decoration: none;
  }
  nav ul li a:hover {
    padding-bottom: 1em;
    border-bottom: 4px solid white;
  }
  .uppercase {
    text-transform: uppercase;
  }
</style>

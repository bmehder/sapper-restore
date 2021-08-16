<script>
  import { slide } from "svelte/transition";
  import Logo from "../UI/Logo.svelte";
  export let sticky = false;
  export let uppercase = false;
  export let background = "darkorange";
  export let color = "white";
  export let linkColor = "white";

  let mobile = false;
  const showMobile = () => {
    mobile = !mobile;
  };
</script>

<header class:sticky style="background:{background};color:{color};">
  <nav class="main">
    <Logo
      logo="<img style='width:100%;' src='/images/restore-medical-group-logo.png' alt='logo' />"
      width="150px"
    />
    <ul class:uppercase>
      <li><a style="color:{linkColor};" href="/">Home</a></li>
      <li><a style="color:{linkColor};" href="patients">Patients</a></li>
      <li><a style="color:{linkColor};" href="providers">Providers</a></li>
      <!-- <li><a style="color:{linkColor};" href="process">Process</a></li> -->
      <li>
        <a style="color:{linkColor};" href="case-studies">Case Studies</a>
      </li>
      <li>
        <a style="color:{linkColor};" href="testimonials">Testimonials</a>
      </li>
      <li><a style="color:{linkColor};" href="contact">Contact</a></li>
    </ul>
  </nav>
  <nav class="mobile">
    <div class="bun">
      <Logo
        logo="<img style='width:100%;' src='/images/restore-medical-group-logo.png' alt='logo' />"
        width="150px"
      />
      <div on:click={showMobile} class="hamburger">&#9776;</div>
    </div>
    {#if mobile}
      <ul transition:slide class:uppercase class="mobile">
        <li>
          <a style="color:{linkColor};" on:click={showMobile} href="/">Home</a>
        </li>
        <li><a style="color:{linkColor};" href="patients">Patients</a></li>
        <li><a style="color:{linkColor};" href="providers">Providers</a></li>
        <li>
          <a
            style="color:{linkColor};"
            on:click={showMobile}
            href="case-studies">Case Studies</a
          >
        </li>
        <li>
          <a style="color:{linkColor};" href="testimonials">Testimonials</a>
        </li>
        <li>
          <a style="color:{linkColor};" on:click={showMobile} href="contact"
            >Contact</a
          >
        </li>
      </ul>
    {/if}
  </nav>
</header>

<style>
  header {
    /* width: 100%; */
    padding: 1em 0;
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
    padding: 0 1em;
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
  ul.mobile {
    width: 100%;
    flex-direction: column;
    margin: 0;
    text-align: center;
  }
  nav div {
    display: flex;
    justify-content: space-between;
  }
  ul.mobile li {
    padding: 1em 0;
  }
  .bun {
    align-items: center;
  }
  .hamburger {
    font-size: 3em;
    /* padding-right: 0.5em; */
  }
  .hamburger,
  nav.mobile {
    display: none;
  }
  @media screen and (max-width: 640px) {
    nav.main {
      display: none;
    }
    nav.mobile {
      display: block;
    }
    .hamburger {
      display: block;
    }
  }
</style>

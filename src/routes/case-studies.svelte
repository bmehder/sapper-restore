<script>
  import { fade } from "svelte/transition";
  import { quintOut } from "svelte/easing";
  import Section from "./components/Layouts/Section.svelte";
  import Grid from "./components/Layouts/Grid.svelte";
  import Flex from "./components/Layouts/Flex.svelte";

  let access = false;
  let showError = false;
  let value = "";
  let pw = "123456";

  const handleSubmit = () => {
    if (value === "123456") {
      showError = false;
      access = true;
    } else {
      showError = true;
      access = false;
    }
  };
</script>

<svelte:head>
  <title>Case Studies | Restore Medical Group | Golden, CO</title>
  <!-- Global site tag (gtag.js) - Google Analytics -->
  <script async src="https://www.googletagmanager.com/gtag/js?id=G-E6GC694DG4">
  </script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag() {
      dataLayer.push(arguments);
    }
    gtag("js", new Date());

    gtag("config", "G-E6GC694DG4");
  </script>
</svelte:head>

{#if access}
  <div transition:fade={{ easing: quintOut }}>
    <Section boxed background="white" padding="0.5em 2em 4em">
      <h3 style="text-align:center;">Case Studies</h3>
      <Grid columns="1fr 1fr" gap="2em">
        <div>
          <h5 class="before-after">Before</h5>
          <div>
            <img src="/images/image4.jpg" alt="before" />
            <aside>
              6.5CM wide persistent wound unable to be healed with traditional
              treatments.
            </aside>
          </div>
        </div>
        <div>
          <h5 class="before-after">After</h5>
          <div>
            <img src="/images/image9.jpg" alt="after" />
            <aside>
              After 7 weeks of treatment using Restore’s Wound Care Protocol.
            </aside>
          </div>
        </div>
      </Grid>
      <Grid columns="1fr 1fr" gap="2em">
        <div>
          <h5 class="before-after">Before</h5>
          <div>
            <img src="/images/image1.jpg" alt="before" />
            <aside>Picture taken 2 weeks into treatment</aside>
          </div>
        </div>
        <div>
          <h5 class="before-after">After</h5>
          <div>
            <img src="/images/image7.jpg" alt="after" />
            <aside>Picture taken 3-4 weeks into treatment</aside>
          </div>
        </div>
      </Grid>
      <Grid columns="1fr 1fr" gap="2em">
        <div>
          <h5 class="before-after">Before</h5>
          <div>
            <img src="/images/image11.jpg" alt="before" />
            <aside>Two year old sacrum wound starting at 5.5CM</aside>
          </div>
        </div>
        <div>
          <h5 class="before-after">After</h5>
          <div>
            <img src="/images/image3.jpg" alt="after" />
            <aside>Reduced to 3.5CM in 4 weeks. Still in treatment.</aside>
          </div>
        </div>
      </Grid>
      <Grid columns="1fr 1fr" gap="2em">
        <div>
          <h5 class="before-after">Before</h5>
          <div>
            <img src="/images/image6.jpg" alt="before" />
            <aside>
              Two wounds being simultaneously treated on the left gluteus.
              Persistent wound for nearly 6 months unable to be treated with
              conventional treatment. In this first picture the little arrow is
              pointing to a tunnel wound that is 6 centimeters deep and 1CM wide
              at entry.. The second wound is roughly 15CM square.
            </aside>
          </div>
        </div>
        <div>
          <h5 class="before-after">After</h5>
          <div>
            <img src="/images/image12.jpg" alt="after" />
            <aside>
              The second picture shows the arrow is pointing to that same wound
              within several weeks of treatment. Estimated to be nearly closed
              to 60%. The second wound has an obvious big change and progressing
              nicely towards full healing.
            </aside>
          </div>
        </div>
      </Grid>
    </Section>
  </div>
{:else}
  <Flex direction="column" justify="center" align="center">
    <form on:submit|preventDefault={handleSubmit}>
      <input type="text" bind:value placeholder="Enter Password..." />
      <button>Submit</button>
      {#if showError}
        <p>Incorrect password.</p>
      {/if}
    </form>
  </Flex>
{/if}

<style>
  .before-after {
    margin-top: 2em;
    text-align: center;
    font-size: 150%;
  }
  aside {
    display: block;
    background: #eee;
    text-align: center;
    padding: 2em;
  }
  img {
    width: 100%;
    height: 400px;
    object-fit: cover;
    border-radius: 2px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.24);
  }
  form {
    margin-top: 4em;
    width: 300px;
  }
</style>

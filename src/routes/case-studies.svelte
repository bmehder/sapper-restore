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

{#if access}
  <div transition:fade={{ easing: quintOut }}>
    <Section boxed background="white" padding="0.5em 2em 4em">
      <h3 style="text-align:center;">Case Studies</h3>
      <Grid columns="1fr 1fr" gap="2em">
        <div>
          <h5 class="before-after">Before</h5>
          <div>
            <img
              src="https://source.unsplash.com/random/400x400?4"
              alt="before" />
            <aside>
              6.5CM wide persistent wound unable to be healed with traditional
              treatments.
            </aside>
          </div>
        </div>
        <div>
          <h5 class="before-after">After</h5>
          <div>
            <img
              src="https://source.unsplash.com/random/400x400?5"
              alt="after" />
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
            <img
              src="https://source.unsplash.com/random/400x400?6"
              alt="before" />
            <aside>Picture taken 2 weeks into treatment</aside>
          </div>
        </div>
        <div>
          <h5 class="before-after">After</h5>
          <div>
            <img
              src="https://source.unsplash.com/random/400x400?7"
              alt="after" />
            <aside>Picture taken 3-4 weeks into treatment</aside>
          </div>
        </div>
      </Grid>
      <Grid columns="1fr 1fr" gap="2em">
        <div>
          <h5 class="before-after">Before</h5>
          <div>
            <img
              src="https://source.unsplash.com/random/400x400?8"
              alt="before" />
            <aside>Two year old sacrum wound starting at 5.5CM</aside>
          </div>
        </div>
        <div>
          <h5 class="before-after">After</h5>
          <div>
            <img
              src="https://source.unsplash.com/random/400x400?9"
              alt="after" />
            <aside>Reduced to 3.5CM in 4 weeks. Still in treatment.</aside>
          </div>
        </div>
      </Grid>
      <Grid columns="1fr 1fr" gap="2em">
        <div>
          <h5 class="before-after">Before</h5>
          <div>
            <img
              src="https://source.unsplash.com/random/400x400?9"
              alt="before" />
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
            <img
              src="https://source.unsplash.com/random/400x400?10"
              alt="after" />
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
      <p><em>The password is "123456"</em></p>
      <input type="text" bind:value placeholder="Enter Password..." />
      <button>Submit</button>
      {#if showError}
        <p>
          Oi! That's not the right password. What are you trying to pull here,
          buddy?
        </p>
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
    height: auto;
    object-fit: cover;
    border-radius: 2px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.24);
  }
  form {
    margin-top: 4em;
    width: 400px;
  }
</style>

<script>
  import Flex from "./Flex.svelte";
  export let background = "darkorange";
  export let color = "white";
  export let height = "";
</script>

<footer style="height:{height};background:{background};color:{color};">
  <h4>We offer multiple locations for in-clinic treatments.</h4>
  <div>
    <Flex justify="center" gap="4em">
      <p style="margin-top: 1em;text-align:center;">
        <big><strong>Golden, CO</strong></big><br />
        400 Indian Street, Suite 280<br />
        Golden, CO 80401
      </p>

      <p style="margin-top: 1em;text-align:center;">
        <big><strong>Thornton, CO</strong></big><br />
        9195 Grant Street, Suite 305<br />
        Thornton, CO 80229
      </p>

      <p style="margin-top: 1em;text-align:center;">
        <big><strong>Aurora, CO</strong></big><br />
        1421 S. Potomac Street, Suite 330<br />
        Aurora, CO 80012
      </p>
    </Flex>
  </div>
  <slot />
</footer>

<style>
  footer {
    padding: 1.5rem;
    background: darkorange;
    color: white;
    text-align: center;
  }
  h4 {
    color: gold;
  }
  div {
    max-width: 960px;
    margin: 0 auto 2em;
  }
</style>

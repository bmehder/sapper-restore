<script>
  import Section from "./components/Layouts/Section.svelte";
  import { fade } from "svelte/transition";
  import { quintOut } from "svelte/easing";
  import Flex from "./components/Layouts/Flex.svelte";
  import CTA from "./components/UI/CTA.svelte";
  import Form from "./components/UI/Form.svelte";
</script>

<svelte:head>
  <title>Contact Us | Restore Medical Group | Golden, CO</title>
</svelte:head>

<div transition:fade={{ easing: quintOut }}>
  <Section boxed background="white" padding="0.5em 0em 0em">
    <Flex direction="column" justify="center" align="center">
      <CTA
        heading="Schedule an Appointment"
        subtitle="<big><strong>(303) 216-2661</strong></big>"
        href="tel:3032162661"
        buttonText="Call Today!"
        src="https://source.unsplash.com/random/400x400?10" />

      <p style="text-align:center;">
        <big><strong>Restore Medical Group</strong></big><br />
        is a DBA of<br />
        Restore Osteo of Colorado, LLC<br />
        400 Indian Street, Suite 280<br />
        Golden, CO 80401
      </p>

      <h3>Send Us A Message</h3>

      <Form
        buttonColor="dodgerblue"
        buttonText="Send Message"
        buttonTextColor="white" />
    </Flex>
  </Section>
</div>

<script>
  import Transition from "./components/Transition.svelte";
  import Section from "./components/Layouts/Section.svelte";
  import Flex from "./components/Layouts/Flex.svelte";
  import CTA from "./components/UI/CTA.svelte";
  import Form from "./components/UI/Form.svelte";
</script>

<svelte:head>
  <meta
    name="description"
    content="Contact Restore Medical Group - 400 Indian Street, Suite 280
Golden, CO 80401 - Schedule An Appointment at (720) 678-9868"
  />
  <title>Contact Us | Restore Medical Group | Golden, CO</title>

  <script
    async
    src="https://www.googletagmanager.com/gtag/js?id=UA-185413763-1"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag() {
      dataLayer.push(arguments);
    }
    gtag("js", new Date());

    gtag("config", "UA-185413763-1");
  </script>
</svelte:head>

<Transition>
  <Section boxed background="white" padding="0.5em 0em 0em">
    <Flex direction="column" justify="center" align="center">
      <CTA
        heading="Schedule an Appointment"
        subtitle="Phone: (720) 678-9868<br />Fax: (720) 678-9860"
        href="tel:7206789868"
        buttonText="Call Today!"
        src="/images/schedule-an-appointment-restore-medical-group.jpg"
      />

      <h3>Three Metro Denver clinics for your convenience:</h3>

      <p style="margin-top: 1em;text-align:center;">
        <big><strong>Golden, CO</strong></big><br />
        400 Indian Street, Suite 280<br />
        Golden, CO 80401
      </p>

      <p style="margin-top: 1em;text-align:center;">
        <big><strong>Thornton, CO</strong></big><br />
        9195 Grant Street, Suite 305<br />
        Thornton, CO. 80229
      </p>

      <p style="margin-top: 1em;text-align:center;">
        <big><strong>Aurora, CO</strong></big><br />
        1421 S. Potomac Street, Suite 330<br />
        Aurora, CO 80012
      </p>

      <p>
        We also realize a wound may make it hard or impossible to visit a
        clinic, so we can also visit a facility or home.
      </p>

      <h3>Send Us A Message</h3>

      <Form
        buttonColor="dodgerblue"
        buttonText="Send Message"
        buttonTextColor="white"
      />
    </Flex>
  </Section>
</Transition>

<style>
  h3 {
    padding: 0 2em;
  }

  p {
    margin-top: 1em;
    text-align: center;
  }
</style>

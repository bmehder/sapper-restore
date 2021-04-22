<script>
  import { fade } from "svelte/transition";
  import { quintOut } from "svelte/easing";
  import Section from "./components/Layouts/Section.svelte";
  import Grid from "./components/Layouts/Grid.svelte";
  import Flex from "./components/Layouts/Flex.svelte";
  import Hero from "./components/UI/Hero.svelte";
  import CTA from "./components/UI/CTA.svelte";
  import Address from "./components/UI/Address.svelte";
</script>

<svelte:head>
  <meta
    name="description"
    content="Restore Medical Group has developed an insurance backed protocol for treating recalcitrant wounds that prove difficult to heal using conventional wound care methods."
  />
  <title>Restore Medical Group | Golden, CO</title>

  <!-- Global site tag (gtag.js) - Google Analytics -->
  <script
    async
    src="https://www.googletagmanager.com/gtag/js?id=G-9T6ZFWHCTY"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag() {
      dataLayer.push(arguments);
    }
    gtag("js", new Date());

    gtag("config", "G-9T6ZFWHCTY");
  </script>
</svelte:head>

<div class="wrapper">
  <main>
    <div transition:fade={{ easing: quintOut }}>
      <Section boxed background="white">
        <img
          class="no-shadow"
          src="/images/header-restore-medical-group.jpg"
          alt="Header - Restore Medical Group"
        />
      </Section>
      <Section background="white" padding="0.5em 2em 0em" boxed>
        <h3>Welcome to a revolution in chronic wound care.</h3>
        <Grid columns="1fr 1fr" gap="2em">
          <article>
            <p>
              Welcome to the
              <strong>Restore Medical Group</strong>
              Wound Care division - a truly unique health care practice. Restore
              Medical Group has developed an insurance backed protocol for treating
              recalcitrant wounds that prove difficult to heal using conventional
              wound care methods.
            </p>

            <p>
              Our treatment protocol incorporates a combination of therapies
              including our exclusively sourced amnio products that rapidly
              promote healing in wound areas.
            </p>

            <p>
              Our approach can provide either in-clinic or on-location care
              options.
            </p>

            <p><strong>Insurance Accepted:</strong> Medicare Part B</p>
          </article>
          <figure>
            <img
              src="/images/wound-care-restore-medical-group.jpg"
              alt="Wound Care - Restore Medical Group"
            />
          </figure>
        </Grid>
      </Section>

      <Section boxed background="white" padding="2em">
        <hr />
      </Section>

      <Section background="white" padding="0.5em 2em" boxed>
        <h4>Identifying Patients</h4>
        <Grid columns="1fr 1fr" gap="2em">
          <div>
            <p>
              When evaluating patients for this protocol please consider the
              following before recommending care.
            </p>
            <figure>
              <img
                src="/images/qualified-patients.jpg"
                alt="Qualified Patients - Restore Medical Group"
              />
            </figure>
          </div>
          <article>
            <p>
              When evaluating patients referral please consider the following
              contraindications:
            </p>
            <ul>
              <li>infected wound,</li>
              <li>active cancer treatment,</li>
              <li>and/or immunosuppressive treatment.</li>
            </ul>

            <h5>Pre-Assessment</h5>
            <p>
              Restore Medical will conduct assessment and amnio products
              preauthorization on all patients prior to treatment to ensure the
              protocol is applicable and insurance is confirmed for the
              treatment.
            </p>

            <h5>Transport</h5>
            <p>
              Transport to our clinical locations can be arranged on behalf of
              the patient if not provided with their current facility or home
              care provider.
            </p>
          </article>
        </Grid>
      </Section>

      <Section boxed background="white" padding="2em">
        <hr />
      </Section>

      <Section background="white" padding="0.5em 2em" boxed>
        <h4>Patient Testimonial</h4>
        <div style="padding:56.25% 0 0 0;position:relative;">
          <iframe
            src="https://player.vimeo.com/video/540318619?title=0&byline=0&portrait=0"
            style="position:absolute;top:0;left:0;width:100%;height:100%;"
            frameborder="0"
            allow="autoplay; fullscreen; picture-in-picture"
            allowfullscreen
            title="Restore Osteo Testimonial Video"
          />
        </div>
        <script src="https://player.vimeo.com/api/player.js"></script>
        <p style="padding: 2em;">
          Richard has wounds on both legs. In this video, he talks about his
          experience at Restore Medical Group, and we share some before and
          after pictures.
        </p>
      </Section>

      <Section boxed>
        <Hero background="/images/snow.jpg" height="400px">
          <Flex align="center" gap="2em">
            <CTA
              heading="We travel to you!"
              subtitle="To schedule an on-site patient evaluation appointment, please call (720) 678-9868."
              href="tel:7206789868"
              buttonText="Call Today!"
              src="/images/transportation-restore-medical-group.jpg"
            />
            <Address />
          </Flex>
        </Hero>
      </Section>
    </div>
  </main>
</div>

<style>
  h4 {
    margin: 0 0 1em 0;
  }
  img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 2px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.24);
  }
  figure {
    width: 400px;
    height: auto;
    margin-bottom: 1em;
  }
  .no-shadow {
    box-shadow: none;
  }
  @media (max-width: 640px) {
    figure {
      width: 300px;
    }
  }
</style>

<script>
  import Transition from "./components/Transition.svelte";
  import Section from "./components/Layouts/Section.svelte";
  import Grid from "./components/Layouts/Grid.svelte";
  import Flex from "./components/Layouts/Flex.svelte";
  import Hero from "./components/UI/Hero.svelte";
  import CTA from "./components/UI/CTA.svelte";
  import Address from "./components/UI/Address.svelte";
  import Button from "./components/UI/Button.svelte";
</script>

<svelte:head>
  <meta
    name="description"
    content="Restore Medical Group has developed an insurance backed protocol for treating recalcitrant wounds that prove difficult to heal using conventional wound care methods."
  />
  <title>Restore Medical Group | Golden, CO</title>

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
  <div class="wrapper">
    <main>
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

            <p>
              <strong>Most insurance accepted, including Medicare Part B</strong
              >
            </p>
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

      <Section background="white" padding="0.5em 2em 3em" boxed>
        <div style="text-align:center;">
          <h4>Testimonials</h4>
          <blockquote>
            "Restore Medical Group was the last chance for me."
            <cite>-Maxine (Patient)</cite>
          </blockquote>
          <p>Check out the testimonials from previous patients.</p>
          <Button
            background="#79a10a"
            url="/testimonials"
            color="white"
            rounded
            shadow
            uppercase>Watch The Videos</Button
          >
        </div>
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
            <!-- <Address /> -->
          </Flex>
        </Hero>
      </Section>
    </main>
  </div>
</Transition>

<style>
  h4 {
    margin: 0 0 1em 0;
  }
  img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 2px;
    /* box-shadow: 0 2px 4px rgba(0, 0, 0, 0.24); */
  }
  figure {
    width: 400px;
    height: auto;
    margin-bottom: 1em;
  }
  .no-shadow {
    box-shadow: none;
  }
  blockquote {
    display: inline-block;
    padding: 2rem;
    color: dodgerblue;
    font-style: italic;
    font-size: 1.5rem;
  }
  cite {
    display: block;
    font-size: 1.2rem;
  }
  @media (max-width: 640px) {
    figure {
      width: 300px;
    }
  }
</style>

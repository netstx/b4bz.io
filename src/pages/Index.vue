<template>
  <Layout>
    <section class="section">
      <div class="container">
        <h1 class="title is-2">Hi.</h1>
        <p class="subtitle">
          I'm <span class="highlight">Rafael</span>. Welcome to my static website.
          <br />This runs on DigitalOcean Apps for now.
          <span class="location"
            ><font-awesome :icon="['fas', 'map-marker-alt']" />
            <strong>$HOME</strong> - sitting on the dock of the bay.</span
          >
        </p>
        <SafeEmail class="button is-primary is-inline-block">
          Say hello!
        </SafeEmail>

        <div class="social-contacts">
          <a
            href="https://github.com/netstx"
            target="_blank"
            rel="noopener"
            aria-label="Follow me on Github"
            ><font-awesome :icon="['fab', 'github']"
          /></a>
          <a
            href="https://twitter.com/rafaelpossamai"
            target="_blank"
            rel="noopener"
            aria-label="Follow me on Twitter, or not... I don't care lol"
            ><font-awesome :icon="['fab', 'twitter']"
          /></a>
          <a
            href="https://www.linkedin.com/in/rafaelpossamai/?locale=en_US"
            target="_blank"
            rel="noopener"
            aria-label="Linkedin"
            ><font-awesome :icon="['fab', 'linkedin-in']"
          /></a>
        </div>
      </div>
    </section>
    <script
      type="application/ld+json"
      v-html="{
        '@context': 'http://schema.org',
        '@type': 'Person',
        name: 'Rafael Possamai',
        jobTitle: 'Engineer',
        url: 'https://thinkpad.io',
      }"
    ></script>
  </Layout>
</template>

<script>
  import SafeEmail from "~/components/SafeEmail";

  export default {
    metaInfo: {
      title: "thinkpad.io",
    },
    components: {
      SafeEmail,
    },
    mounted: function () {
      console.info(
        "\n",
        " ██████╗ ██╗  ██╗██████╗ ███████╗\n",
        " ██╔══██╗██║  ██║██╔══██╗╚══███╔╝\n",
        " ██████╔╝███████║██████╔╝  ███╔╝ \n",
        " ██╔══██╗╚════██║██╔══██╗ ███╔╝  \n",
        " ██████╔╝     ██║██████╔╝███████╗\n",
        " ╚═════╝      ╚═╝╚═════╝ ╚══════╝\n\n",
        "Hey stranger! This source code was forked from Bastien Wirtz, find it here: https://github.com/bastienwirtz/b4bz.io"
      );
    },
  };
</script>

<style lang="scss" scoped>
  .subtitle {
    padding-top: 0.5rem;
  }
  .location {
    display: block;
    margin: 0.8rem 0 1.5rem 0;
    font-size: 0.8rem;
    color: #878b8f;
    svg {
      margin-right: 3px;
    }
  }

  .emoji {
    margin-left: 3px;
    font-size: 2.2rem;
  }

  .social-contacts {
    display: inline-block;
    a {
      font-size: 1.4rem;
      padding: 1rem 0.5rem;

      &:first-child {
        padding-left: 1.3rem;
      }
    }
  }
</style>

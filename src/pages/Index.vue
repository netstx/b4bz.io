<template>
  <Layout>
    <section class="section">
      <div class="container">
        <h1 class="title is-2">Hi.</h1>
        <p class="subtitle">
          I'm <span class="highlight">Rafael</span>. Welcome to my temporary page, not much here for now.
          <br />This runs on DO Apps for now...
          <span class="location"
            ><font-awesome :icon="['fas', 'map-marker-alt']" />
            <strong>$HOME</strong> - sitting on the dock of the bay.</span
          >
        </p>
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
        "Howdy, this source code was forked from Bastien Wirtz, find it here: https://github.com/bastienwirtz/b4bz.io"
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

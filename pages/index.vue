<template>
  <b-row style="margin-left: 0; margin-right: 0">
    <b-col md="4">
      <b-img src="../assets/sufrida.jpeg" id="frida-img" alt="Frida SuFrida" />
    </b-col>

    <b-col md="8">
      <h2 class="intro animate__animated animate__fadeInUp animate__fast">
        Hi!
        <br />I<span>'m Frida</span>.
      </h2>

      <div class="col-md-10 info">
        A <b>Front End</b> Developer and <b>Web</b> Designer from Mexico, ready
        to help you join the digital world!
        <br />
        <b-button
          class="
            action-btn
            animate__animated animate__wobble animate__delay-4s animate__fast
          "
          to="/projects"
        >
          Explore >
        </b-button>

        <b-button class="action-btn" variant="primary" to="/contact">
          Get In Touch
        </b-button>

        <!-- .SOCIAL LINKS SECTION -->
        <div
          class="
            social-icons
            animate__animated animate__fadeInUp animate__delay-1s
          "
        >
          <social-link :to="socialLinks.github">
            <GithubIcon />
          </social-link>

          <social-link :to="socialLinks.mail">
            <MailIcon />
          </social-link>

          <social-link :to="socialLinks.linkedin">
            <LinkedinIcon />
          </social-link>
        </div>
      </div>
    </b-col>
  </b-row>
</template>

<script>
import GithubIcon from "vue-ionicons/dist/logo-github.vue";
import LinkedinIcon from "vue-ionicons/dist/logo-linkedin.vue";
import TwitterIcon from "vue-ionicons/dist/logo-twitter.vue";
import FacebookIcon from "vue-ionicons/dist/logo-facebook.vue";
import YoutubeIcon from "vue-ionicons/dist/logo-youtube.vue";
import MailIcon from "vue-ionicons/dist/md-mail.vue";

export default {
  components: {
    GithubIcon,
    LinkedinIcon,
    TwitterIcon,
    FacebookIcon,
    YoutubeIcon,
    MailIcon,
  },

  data() {
    return {
      avatar: require("@/assets/sufrida.jpeg"),
      // ADD YOUR SOCIAL LINKS HERE 👇
      socialLinks: {
        github: "https://github.com/SuFrida",
        youtube: "https://1intan99.my.id/youtube",
        mail: "mailto:frida.b.v1021@gmail.com",
        linkedin: "https://linkedin.com/in/fridabv ",
      },
    };
  },

  head: {
    title: "Frida SuFrida",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "A Front End developer and Web Designer from Mexico, ready to help you join the digital world!",
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "Frida SuFrida",
      },
      {
        property: "og:description",
        content:
          "A Front End developer and Web Designer from Mexico, ready to help you join the digital world!",
      },
      {
        hid: "og:image",
        name: "og:image",
        content: "",
      },
    ],
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start();

      setTimeout(() => this.$nuxt.$loading.finish(), 500);
    });
  },
};
</script>

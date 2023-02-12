<template>
  <div class="about page animate__animated animate__fadeIn">
    <h2>Recent Project</h2>
    <div class="container">
      <div class="row" v-for="(project, index) in projects" :key="index">
        <div class="col-md-5">
          <img
            :src="project.image_cover"
            :alt="project.title"
            class="project-cover"
          />
        </div>
        <div class="col-md-5">
          <h2 class="mt-3" style="text-align: left">
            {{ project.title }}
            <hr class="dope" />
          </h2>
          <b-card class="mt-3 mb-3 text-left text-dark">
            <p>{{ project.description }}</p>
            <b-link :href="project.link"
              >Check it out! <LinkIcon style="color: #000"
            /></b-link>
            <hr />
          </b-card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import LinkIcon from "vue-ionicons/dist/md-link.vue";

export default {
  components: {
    LinkIcon,
  },
  data() {
    return {
      projects: [
        {
          title: "PowerClean BC",
          tag: "Website Redesign and deployment",
          description:
            "A Canadian Cleaning Company with the need to redesign their website.",
          image_cover: require("@/assets/powerclean.png"),
          link: "https://www.powercleanbc.ca/",
        },
        {
          title: "Wheelers Yard",
          tag: "Wordpress Website",
          description:
            "A Bicycle Rental Company in need for a Wordpress Website",
          image_cover: require("@/assets/wy.png"),
          github_url: "",
          link: "https://wheelersyard.ca/",
        },
        {
          title: "Pedido Fácil",
          tag: "Web and Mobile Mockup Design",
          description:
            "A delivery company needing a web and mobile mockup design.",
          image_cover: require("@/assets/pedidofacil.png"),
          link: "https://www.figma.com/file/60TQ53gnObXPTOWRamz9Nx/Pedido-Facil-Mockup?node-id=1%3A2",
        },
        {
          title: "Eklipse Joyería",
          tag: "Web and Mobile Mockup Design",
          description:
            "A jewelry company with a Shopify E-commerce in need for a redesign for Web and Mobile.",
          image_cover: require("@/assets/eklipse.png"),
          link: "https://www.figma.com/proto/mT6fGu2vQjRxzj6UOvhKr5/Eklipse-Joyer%C3%ADa?node-id=1260%3A27621&scaling=min-zoom&page-id=1106%3A22286&starting-point-node-id=1260%3A27621",
        },
        {
          title: "Doble Veta",
          tag: "VueJS Front End Development",
          description: "VueJS implementation to a website prototype.",
          image_cover: require("@/assets/dobleveta.png"),
          link: "https://dobleveta-proj.netlify.app/project/",
        },
        {
          title: "Studio D04",
          tag: "VueJS Front End Development",
          description: "VueJS implementation for a construction company.",
          image_cover: require("@/assets/studio04.png"),
          link: "https://studiod04.com/",
        },
        {
          title: "Tec Audio Coders",
          tag: "Wordpress Website with Download Option",
          description:
            "Wordpress website for the student group Tec Audio Coders to download audio plugins.",
          image_cover: require("@/assets/tac.png"),
          link: "https://www.tecaudiocoders.com/",
        },
      ],
    };
  },
  methods: {
    isEven(n) {
      if (n % 2 == 0) {
        return true;
      } else {
        return false;
      }
    },
  },
  head: {
    title: "Recent Projects 💻 - Frida SuFrida",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "View all the recents open-sourced projects built with ♥ by Frida SuFrida",
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "Recent Projects 💻 - Frida SuFrida",
      },
      {
        property: "og:description",
        content:
          "View all the recents open-sourced projects built with ♥ by Frida SuFrida",
      },
      {
        hid: "og:image",
        name: "og:image",
        content: require("@/assets/man-computer.png"),
      },
    ],
  },
};
</script>
<style scoped>
.row {
  margin-top: 70px;
}
.project-cover {
  width: inherit;
  border-radius: 3px;
}
hr.dope {
  border: 0;
  width: 90px;
  border-top: 2px solid #dc3545;
  text-align: left;
  margin: initial;
  margin-top: 7px;
  margin-left: 5px;
}
</style>

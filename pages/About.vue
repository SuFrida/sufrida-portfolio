<template>
  <div class="container animate__animated animate__fadeIn">
    <div class="row">
      <div class="col-md-6">
        <div class="about">
          <h1 class="line-after">About Me</h1>
          <h4 class="mt-4">Hey 👋</h4>
          <p>
            My name is Frida Bonilla, I am a <b>Front End </b> Developer and
            <b>Web </b> Designer.
          </p>
          <p>
            I believe web development and UX/UI design are two powerful tools in
            the modern world, where digitalization is key for businesss success.
            <br />
            A successful web code also needs to be accessible and friendly to
            the environment (by been fast and eficient) 😎.
          </p>
          <h3 class="mt-5">Tech & Skills</h3>
          <p>Here are some of my strengths:</p>
          <div class="row mt-4 animate__animated animate__fadeInUp">
            <div class="col">
              <h5>Programming Languages</h5>
              <ul style="list-style-type: circle">
                <li>Javascript</li>
                <li>Java</li>
                <li>PHP</li>
                <li>C/C++, C#</li>
                <li>Python</li>
              </ul>
              <h5>Languages</h5>
              <ul style="list-style-type: circle">
                <li>Spanish</li>
                <li>English</li>
                <li>French</li>
                <li>Finnish</li>
              </ul>
            </div>
            <div class="col">
              <h5>Technologies</h5>
              <ul style="list-style-type: circle">
                <li>HTML</li>
                <li>CSS</li>
                <li>Bootstrap5</li>
                <li>Sass</li>
                <li>Wordpress</li>
                <li>Elementor</li>
                <li>Node.js</li>
                <li>NPM</li>
                <li>Git</li>
                <li>React</li>
                <li>NextJS</li>
                <li>VueJS</li>
              </ul>
            </div>
            <div class="col">
              <ul style="list-style-type: circle">
                <li>Nuxt</li>
                <li>Prismic</li>
                <li>Angular</li>
                <li>Photoshop</li>
                <li>Illustrator</li>
                <li>InDesign</li>
                <li>Premiere Pro</li>
                <li>Figma</li>
                <li>Adobe XD</li>
                <li>Shopify</li>
                <li>MySQL</li>
                <li>PostgreSQL</li>
                <li>MongoDB</li>
                <li>Reaper</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <img
          src="../assets/frida-formal.jpeg"
          alt="Frida Formal"
          class="abt-img"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      startYear: 2021,
      currYear: new Date().getFullYear(),
      stacks: [
        {
          language: "HTML",
          experience: "3+ Years",
          variant: "secondary",
          breif: "lorem...",
        },
        {
          language: "CSS",
          experience: "3+ Years",
          variant: "primary",
          breif: "lorem...",
        },
        {
          language: "Javascript",
          experience: "2+ Years",
          variant: "warning",
          breif: "lorem...",
        },
        {
          language: "VUE.JS",
          experience: "2+ Years",
          variant: "success",
          breif: "lorem...",
        },
        {
          language: "Node.js",
          experience: "2+ Years",
          variant: "dark",
          breif: "lorem...",
        },
      ],
    };
  },
  head: {
    title: "About - Frida",
    meta: [
      {
        hid: "description",
        name: "description",
        // currYear - startYear
        content: ``,
      },
    ],
  },
};
</script>
<style scoped>
.container {
  margin-top: 140px;
  text-align: left;
}
.line-after {
  overflow: hidden;
}
.line-after::after {
  content: "";
  display: inline-block;
  height: 0.5em;
  vertical-align: bottom;
  width: 100%;
  margin-right: -100%;
  margin-left: 10px;
  border-top: 2px solid rgb(211, 46, 46);
}
.abt-img {
  width: inherit;
  height: inherit;
  border-radius: 5px;
}
/* .abt-img:hover {
  animation: swing;
  animation-duration: 2s;
} */
</style>

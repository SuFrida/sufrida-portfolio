<template>
  <b-container class="page animate__animated animate__fadeIn">
    <b-row class="justify-content-center">
      <b-col cols="md-6">
        <h2>Get in touch 💌</h2>

        <p class="text-left">
          If you have any question or just want to say hi, i'll try my best to
          get back to you.
        </p>

        <b-alert show variant="success" v-if="showAlert">
          <strong>All done 🎉</strong><br />
          Thanks for reaching out {{ this.formData.name }}, I'll reply as soon
          as i can.
        </b-alert>
        <form
          action="https://formspree.io/f/xzbqekdb"
          method="POST"
          class="mb-5"
        >
          <fieldset id="input-group-1" class="form-group">
            <legend
              id="input-group-1__BV_label_"
              tabindex="-1"
              class="bv-no-focus-ring col-form-label pt-0"
            >
              Your Name:
            </legend>
            <div tabindex="-1" role="group" class="bv-no-focus-ring">
              <input
                type="text"
                name="name"
                placeholder="Your name..."
                required="required"
                aria-required="true"
                class="form-control"
                id="__BVID__45"
              />
            </div>
          </fieldset>
          <fieldset id="input-group-2" class="form-group">
            <legend
              id="input-group-2__BV_label_"
              tabindex="-1"
              class="bv-no-focus-ring col-form-label pt-0"
            >
              Your Email:
            </legend>
            <div tabindex="-1" role="group" class="bv-no-focus-ring">
              <input
                type="email"
                name="email"
                placeholder="you@email.com"
                required="required"
                aria-required="true"
                class="form-control"
                id="__BVID__47"
              />
            </div>
          </fieldset>
          <fieldset id="input-group-3" class="form-group">
            <legend
              id="input-group-3__BV_label_"
              tabindex="-1"
              class="bv-no-focus-ring col-form-label pt-0"
            >
              Your Message:
            </legend>
            <div tabindex="-1" role="group" class="bv-no-focus-ring">
              <textarea
                name="message"
                placeholder="Watsup Frida, are you available for.."
                required="required"
                rows="3"
                wrap="soft"
                aria-required="true"
                class="form-control"
                id="__BVID__49"
                style="resize: none"
              ></textarea
              ><!----><!----><!---->
            </div>
          </fieldset>
          <button type="submit" class="btn btn-primary">Submit</button>
        </form>
      </b-col>
    </b-row>
  </b-container>
</template>
<script>
export default {
  data() {
    return {
      showAlert: false,
      formData: {
        name: "Frida SuFrida",
        email: "",
        message: "",
      },
    };
  },
  methods: {
    async sendMessage(e) {
      const self = this;
      var data = new FormData();

      data.append("Name", self.formData.name);
      data.append("Email", self.formData.email);
      data.append("Message", self.formData.message);

      fetch("https://formspree.io/f/xzbqekdb", {
        method: "POST",
        body: data,
        headers: {
          Accept: "application/json",
        },
      }).then((response) => {
        if (response.ok) {
          this.showAlert = true;
          form.reset();
        } else {
          alert("Sending message failed, please try again");
        }
      });
      // .catch(error => {
      //   alert("Sending message failed, please try again");
      // });
    },
  },
  head: {
    title: "Contact - Frida",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Do you have any enquires? Send a message now!",
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "Contact - Frida",
      },
      {
        property: "og:description",
        content: "Do you have any enquires? Send a message now!",
      },
      {
        hid: "og:image",
        name: "og:image",
        content: require("@/assets/contact.jpg"),
      },
    ],
  },
};
</script>
<style scoped>
.container {
  margin-top: 120px;
}
form {
  margin-top: 40px;
  text-align: left;
}
</style>

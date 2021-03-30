<template>
  <div class="webcam-container">
    <img src="/assets/sheldonBotlogo.svg.jpg" class="webcam">
    <div class="text-bar">
      <h3 class="title">{{ name }}</h3>
      <h3 class="status" ref="last-update-text">{{ lastUpdate }}</h3>
    </div>
  </div>
</template>

<script>

export default {
  name: "WebCamSend",
  props: {
    name: {
      type: String,
      required: true
    },
    url: {
      type: String,
      required: true
    },
  },
  components: {
    //'vue-web-cam': WebCam
  },


  async refresh(){
    if (process.client) {
      const imagePost = await this.$http.$post(this.url, { img: 'test' })
      }
  }
}
</script>

<style scoped>

.webcam {
  border-radius: 0.5em;
  padding: 0.5em;
  max-width: 20em;
}
.title,.status {
  display: inline;
  padding: 0.5em;
}
.title {
  float: left;
}
.status {
  float: right;
}
.webcam-container {
  background-color: #353535;
  border-radius: 0.5em;
}

</style>

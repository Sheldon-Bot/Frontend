<template>
  <div class="camera-container">
    <img ref="camera-out" class="camera" v-bind:src="url">
    <div class="text-bar">
      <h3 class="title">{{ name }}</h3>
      <h3 class="status" ref="last-update-text">{{ lastUpdate }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "CameraView",
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
  data() {
    return {
      lastUpdate: 0,
      interval: null,
      refreshRate: 150
    }
  },
  methods: {
    refresh() {
      if (process.client) {
        const imgElement = this.$refs["camera-out"];
        imgElement.setAttribute("src", this.url + "?" + Math.random());
        const textElement = this.$refs["last-update-text"];
        textElement.innerText = "Last frame: " + (Date.now() - this.lastUpdate) + "ms";
        this.lastUpdate = Date.now();
      }
    }
  },
  created() {
    this.interval = setInterval(this.refresh, this.refreshRate);
  },
  destroyed() {
    clearInterval(this.interval);
  }
}
</script>

<style scoped>
.camera {
  border-radius: 0.5em;
  padding: 0.5em;
  max-width: 40em;
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
.camera-container {
  background-color: #353535;
  border-radius: 0.5em;
}
</style>

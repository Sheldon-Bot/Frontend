<template>
  <div class="camera-container">
    <img ref="camera-out" class="camera">
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
    async refresh() {
      if (process.client) {
        const imgElement = this.$refs["camera-out"];
        const textElement = this.$refs["last-update-text"];

        const authToken = localStorage.getItem('authToken')

        if (!authToken) {
          console.log("No auth token present")
          return
        }

        const imageResponse = await this.$http.$post(this.url+"?"+Math.random(), {token: authToken})

        const url = 'data:image/jpeg;base64,' + imageResponse

        console.log(url)

        imgElement.setAttribute("src", url);
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

function hexToBase64(str) {
  return btoa(String.fromCharCode.apply(null, str.replace(/\r|\n/g, "").replace(/([\da-fA-F]{2}) ?/g, "0x$1 ").replace(/ +$/, "").split(" ")));
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

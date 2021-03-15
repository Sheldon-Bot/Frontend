<template>
  <v-row justify="center" align="center">
    <div class="camera-row">
      <h1>Control</h1>
      <br><hr><br>
      <CameraView class="camera-view" name="Front camera" url="http://158.69.116.172:5001/api/image"></CameraView>
      <CameraView class="camera-view" name="Back camera" url="http://158.69.116.172:5001/api/imageBack"></CameraView>
    </div>
    <div id="joystick" class="joystick"></div>
  </v-row>
</template>

<script>
import CameraView from "~/components/CameraView";
import nipplejs from 'nipplejs';
export default {
  components: {
    CameraView
  },
  data() {
    return {
      joy: null
    }
  },
  mounted() {
    const staticGamepad = nipplejs.create({
      zone: document.querySelector('#joystick'),
      mode: 'static',
      position: { left: '50%', top: '50%' },
      color: '#d77373',
      threshold: 0.25,
      fadeTime: 400,
      maxNumberOfNipples: 1
    })
     this.joy = nipplejs.create({
       zone: document.getElementById('joystick'),
       color: 'blue'
     });
  }
}
</script>

<style scoped>
@media screen and (max-width: 992px) {
  .camera-row {
    flex-direction: column;
  }
}
.camera-row {
  display: flex;
  flex-direction: row;
}
.camera-view {
  margin: 0.4em;
}
.joystick {
  min-width: 10em;
  min-height: 10em;
}
</style>

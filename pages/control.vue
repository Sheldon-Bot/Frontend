<template>
    <div class="camera-row">
      <h1>Control</h1>
      <br><hr><br>
      <CameraView class="camera-view" name="Front camera" url="http://localhost:5001/image/front"></CameraView>
      <CameraView class="camera-view" name="Back camera" url="http://localhost:5001/image/back"></CameraView>
    </div>
</template>

<script>
import CameraView from "~/components/CameraView";

export default {
  components: {
    CameraView
  },
  data() {
    return {}
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

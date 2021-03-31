<template>
    <div class="control-container">
      <PageHeader title="Control"/>
      <div class ="camera-row">
        <CameraView class="camera-view" name="Front camera" url="http://localhost:5001/image/front"></CameraView>
        <CameraView class="camera-view" name="Back camera" url="http://localhost:5001/image/back"></CameraView>
        <WebCamSend class="camera-view" name="Web camera" url="http://localhost:5001/webcam"></WebCamSend>
      </div>
    </div>
</template>

<script>
import CameraView from "~/components/CameraView";

export default {
  head: {
    title: 'Ribit Control',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Control page of the Ribit Bot'
      }
    ]
  },
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
    flex-direction: row;
  }
}
.camera-row {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  padding-bottom: 0.5em;
}
.camera-view {
  margin: 0.4em;
}
.joystick {
  min-width: 10em;
  min-height: 10em;
}
</style>

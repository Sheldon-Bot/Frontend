<template>
  <div>
    <div id="joystick"></div>
  </div>
</template>

<script>
import nipplejs from "nipplejs"

export default {
  name: "Nipple",
  created() {
    const options = {
      zone: document.getElementById('joystick'),
      color: 'blue',
      size: 2,
      position: {left: '50%', top: '50%'},    // preset position for 'static' mode
      mode: 'static',                         // 'dynamic', 'static' or 'semi'
      restJoystick: true,
      shape: 'circle',                        // 'circle' or 'square'
      dynamicPage: true,                      // Enable if the page has dynamically visible elements
      follow: true,                           // Makes the joystick follow the thumbstick
    };

    const manager = nipplejs.create(options);
  }
}

</script>


<style scoped>

</style>

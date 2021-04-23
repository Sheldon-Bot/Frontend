<template>
  <div>
    <div id="joystick"></div>
  </div>
</template>

<script>
const nipplejs = require("nipplejs");
import nipplejs from 'nipplejs';

var options = {
  zone: document.getElementById('joystick'),
  color: 'blue',
  size: 2,
  threshold: Float,               // before triggering a directional event
  fadeTime: Integer,              // transition time
  multitouch: Boolean,
  maxNumberOfNipples: Number,     // when multitouch, what is too many?
  dataOnly: Boolean,              // no dom element whatsoever
  position: 'static',               // preset position for 'static' mode
  mode: 'static',                   // 'dynamic', 'static' or 'semi'
  restJoystick: Boolean,
  restOpacity: Number,            // opacity when not 'dynamic' and rested
  lockX: Boolean,                 // only move on the X axis
  lockY: Boolean,                 // only move on the Y axis
  catchDistance: Number,          // distance to recycle previous joystick in
                                  // 'semi' mode
  shape: 'circle',                  // 'circle' or 'square'
  dynamicPage: Boolean,           // Enable if the page has dynamically visible elements
  follow: Boolean,                // Makes the joystick follow the thumbstick


};
var manager = nipplejs.create(options);

export default {
name: "Nipple"

}

</script>


<style scoped>

</style>

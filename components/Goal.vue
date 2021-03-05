<template>
  <div>
    <div class="box">
      <p class="initial"><span class="big-text">Our goal</span> was to build a robot that would allow for students online to have a physical presence within the classroom. It was roughly inspired by the robot made by Sheldon in "The Big Bang Theory".</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Goal"
}
</script>

<style scoped>
.box {
  max-width: 75vh;
  background-color: #559B81;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.initial {
  max-width: 70vh;
  padding: 1em;
  background-color: #243742;
  color: aliceblue;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.big-text {
  float: left;
  font-size: 4em;
}
</style>

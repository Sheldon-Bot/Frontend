<template>
  <div class="box">
    <div class="text-container">
      <h1 class="title">{{title}}</h1>
      <p class="text">{{body}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "OurStory",
  props: {
    title: {
      type: String,
      required: true
    },
    body: {
      type: String,
      required: true
    },
  }
}
</script>

<style scoped>
.box {
  max-width: 60%;
  background-color: #559B81;
}

.text-container {
  margin-top: 1em;
  margin-bottom: 1em;
  background-color: #243742;
  color: aliceblue;
  padding: 0.3em 1em;
}

.title {
  font-style: italic;
  margin-top: 0.1em;
  margin-bottom: 0.1em;
  padding: 0;
}
@media all and (max-width: 1100px) {
  .box {
    max-width: 80%;
  }
}
</style>

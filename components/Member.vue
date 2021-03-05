<template>
  <div class="portrait-container">
    <img class="portrait" :src="image">
    <div class="text-container">
      <p class="text name">{{name}}</p>
      <p class="text role">{{role}}</p>
    </div>
    <div ref="dropdown-container" class="dropdown-container"></div>
  </div>
</template>

<script>
export default {
  name: "Member",
  props: {
    name: {
      type: String,
      required: true
    },
    role: {
      type: String,
      required: true
    },
    image: {
      type: String,
      required: true
    }
  },
  data() {
    return {

    }
  },
  beforeMount() {

  }
}
</script>

<style scoped>
  .portrait-container {
    display: flex;
    flex-direction: column;
    text-align: center;
    background-color: #3f5167;
    margin: 1em;
    border-radius: 0.5em;
  }
  .portrait {
    width: 20em;
    border-top-left-radius: 0.5em;
    border-top-right-radius: 0.5em;
  }

  .text {
    font-size: 1.3em;
    padding-top: 0.3em;
    padding-bottom: 0.3em;
  }

  .name {
    margin: 0;
    padding-bottom: 0;
    padding-top: 0;
    color: #70c4a6;
    font-size: 1.45em;
  }

  .role {
    color: aliceblue;
    font-size: 1.2em;
  }

  .text-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
</style>

<template>
  <div>
    <h1>{{title}}</h1>
    <br><hr><br>
  </div>
</template>

<script>
export default {
  name: "PageHeader",
  props: {
    title: {
      type: String,
    }
  }
}
</script>

<style scoped>
  h1 {
    text-align: center;
    padding-top: 1em;
    font-size: 36px;
    color: aliceblue;
    letter-spacing: 4px;
  }
  hr {
    width: 60%;
    display: block;
    margin-left: auto;
    margin-right: auto;
    border: none;
    height: 3px;
    border-radius: 2px;
    background-color: #35495e;
  }
</style>

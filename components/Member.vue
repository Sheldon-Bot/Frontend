<template>
  <div class="potraits">
    <h1>{{name}}</h1>
    <img class="portait-tag" src="~/assets/MathewBorg.jpg">
  </div>
</template>

<script>
export default {
name: "Member"
}
</script>

<style scoped>
  .potraits {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  .portait-tag{
    width: 20em;
    padding: 1em;
  }
</style>

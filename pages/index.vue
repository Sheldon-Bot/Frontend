<template>
  <div class="home">
    <h1>Sheldon Bot</h1>
    <br><hr><br>
    <img class="image" src ="~/assets/sheldonBotlogo.svg">
  </div>
</template>

<script>
export default {}
</script>

<style>
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
  .home {
    background-color: #2b3c47;
    width: 70%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .image{
    width: 20em;
    padding-top: 1em;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
</style>

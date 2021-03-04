<template>
  <div>
    <h1>Sheldon Bot</h1>
    <br><hr><br>
    <img class="image" src ="~/assets/sheldonBotlogo.svg">
    <div class="box">
      <p class="initial">Our Goal</p>
      <p class="initial">was to build a robot that would allow for students online to have a physical presence within the classroom. It was roughly inspired by the robot made by Sheldon in "The Big Bang Theory".</p>
    </div>
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
  .image{
    width: 20em;
    padding-top: 1em;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .box {
    max-width: 75vh;
    background-color: #559B81;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .box:hover {
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
</style>

<template>
  <div class="page-container">
    <PageHeader title="Sheldon Bot"/>
    <img class="image" src ="~/assets/sheldonBotlogo.svg">
    <div class="goal-container">
      <Goal class="goal"></Goal>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
  .image {
    width: 20em;
    padding: 1em;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .goal-container {
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding-bottom: 3em;
  }
</style>

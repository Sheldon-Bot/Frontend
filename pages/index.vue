<template>
  <div class="page-container">
    <PageHeader title="Sheldon Bot"/>

    <div class="goal-container">
      <img class="image" src ="~/assets/sheldonBotlogo.svg">
      <Goal class="goal"></Goal>
    </div>
    <div class="our-story-container">
      <img class="image" src ="~/assets/Untitled-1.png">
      <OurStory class="our-story"></OurStory>
    </div>

  </div>
</template>

<script>
export default {}
</script>

<style>
.image {
  width: 20em;
  display: block;
  padding: 3em;

}
.goal-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-bottom: 3em;
}
  .our-story-container{
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding-bottom: 3em;
    flex-wrap: wrap;
    padding: 3em;

  }

</style>

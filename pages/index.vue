<template>
  <div class="page-container">
    <PageHeader title="Sheldon Bot"/>

    <div class="goal-container">
      <img class="image" src ="~/assets/sheldonBotlogo.svg">
      <text-box1 title="The Goal" body="We set out to build a robot that would allow for students online to have a physical presence within the classroom. It was roughly inspired by the robot made by Sheldon in The Big Bang Theory."></text-box1>
    </div>

    <div class="background-container">
      <img class="image" src ="~/assets/OCSketch.svg">
      <text-box2 title="Background" body="We set out to build a robot that would allow for students online to have a physical presence within the classroom. It was roughly inspired by the robot made by Sheldon in The Big Bang Theory."></text-box2>
    </div>

    <div class="story-container">
      <text-box2 title="Our Story" body="We set out to build a robot that would allow for students online to have a physical presence within the classroom. It was roughly inspired by the robot made by Sheldon in The Big Bang Theory."></text-box2>
      <img class="image" src ="~/assets/OCSketch.svg">
    </div>

    <div class="final-container">
      <text-box1 title="Final Product" body="We set out to build a robot that would allow for students online to have a physical presence within the classroom. It was roughly inspired by the robot made by Sheldon in The Big Bang Theory."></text-box1>
      <img class="image" src ="~/assets/sheldonBotlogo.svg">
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
  padding-bottom: 0.5em;
}
.background-container{
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  padding-bottom: 0.5em;
}

.story-container{
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}

.final-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-bottom: 3em;
}

</style>

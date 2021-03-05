<template>
  <div class="team">
    <PageHeader title="Our Team"/>
    <div class="rowAlignment">
      <Member name="Mr. Haas" role="Instructor" :image="require(`~/assets/MathewBorg.jpg`)"></Member>
      <Member name="Mathew Borg" role="Project Manager" :image="require(`~/assets/MathewBorg.jpg`)"></Member>
      <Member name="Mason Chopik" role="Engineer" :image="require(`~/assets/MathewBorg.jpg`)"></Member>
      <Member name="Kaden Scott" role="Software Developer" :image="require(`~/assets/MathewBorg.jpg`)"></Member>
      <Member name="Alex Schulz" role="Engineer" :image="require(`~/assets/MathewBorg.jpg`)"></Member>
      <Member name="Ethan Kennedy Munsterman" role="Assistant" :image="require(`~/assets/MathewBorg.jpg`)"></Member>
      <Member name="Jordan" role="Assistant" :image="require(`~/assets/MathewBorg.jpg`)"></Member>
    </div>
  </div>
</template>

<script>
export default {
  name: "About"
}
</script>

<style scoped>
  .rowAlignment {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    padding-bottom: 3em;
  }
</style>

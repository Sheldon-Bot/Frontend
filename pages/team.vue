<template>
  <div class="team">
    <PageHeader title="Our Team"/>
    <div class="rowAlignment">
      <Member name="Mr. Haas" role="Instructor" :image="require(`~/assets/Mr. Haas.JPG`)"></Member>
      <Member name="Mathew Borg" role="Project Manager" :image="require(`~/assets/Mathew Borg.JPG`)"></Member>
      <Member name="Mason Chopik" role="Engineer" :image="require(`~/assets/Mason Chopik.JPG`)"></Member>
      <Member name="Kaden Scott" role="Software Engineer" :image="require(`~/assets/Kaden Scott.JPG`)"></Member>
      <Member name="Alex Schulz" role="Mechanical Engineer" :image="require(`~/assets/Alex Schulz.jpg`)"></Member>
      <Member name="Ethan Kennedy Munsterman" role="Electrical Intern" :image="require(`~/assets/Ethan Kennedy Munsterman.JPG`)"></Member>
      <Member name="Jordan Dolson" role="Co-Op Student" :image="require(`~/assets/Jordan Dolson.JPG`)"></Member>
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

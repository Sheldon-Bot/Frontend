<template>
  <div class="team">
    <PageHeader title="Our Team"/>
    <div class="rowAlignment">
      <Member name="Mr. Haas" role="Director of Operations" :image="require(`~/assets/Mr. Haas.JPG`)"></Member>
      <Member name="Mathew Borg" role="General Engineer" :image="require(`~/assets/Mathew Borg.JPG`)"></Member>
      <Member name="Mason Chopik" role="General Engineer" :image="require(`~/assets/Mason Chopik.JPG`)"></Member>
      <Member name="Kaden Scott" role="Software Developer" :image="require(`~/assets/Kaden Scott.JPG`)"></Member>
      <Member name="Alex Schulz" role="Mechanical Engineer" :image="require(`~/assets/Alex Schulz.jpg`)"></Member>
      <Member name="Ethan Kennedy Munsterman" role="Technical Staff" :image="require(`~/assets/Ethan Kennedy Munsterman.JPG`)"></Member>
      <Member name="Jordan Dolson" role="Technical Staff" :image="require(`~/assets/Jordan Dolson.JPG`)"></Member>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Ribit Team',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'The team members who contributed to the creation and esign of the Ribit'
      }
    ]
  },
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

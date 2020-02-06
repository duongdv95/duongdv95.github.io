<template>
  <div class="technologies">
    <div class="technologies-images">
      <img :src="require(`@/assets/` + item + `.png`)" v-for="(item, index) in techUsed" v-bind:key="index"/>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Technologies',
  props: {
    techUsed: {
      type: Array
    }
  }
}

</script>

<style scoped lang="scss">
.technologies {
  margin: 1em 0;
}
.technologies .technologies-images {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  img {
    height: 50px;
    padding: 0.5em;
  }
}
</style>
